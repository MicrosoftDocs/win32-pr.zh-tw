---
description: 以下是針對關閉通訊端的關閉通訊端連線主體所提供的詳細資料。 請務必區分關機通訊端連線和關閉通訊端之間的差異。
ms.assetid: 383747c3-dd3d-4a18-b4e8-2815d5e5c0c7
title: 正常關機、延遲選項和通訊端關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f6791eaa803da561fc9f3c175b5270950cbec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191340"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure"></a>正常關機、延遲選項和通訊端關閉

以下是針對關閉通訊端的關閉通訊端連線主體所提供的詳細資料。 請務必區分關機通訊端連線和關閉通訊端之間的差異。

關閉通訊端連線時，會在這兩個端點之間交換通訊協定訊息，而這兩個端點又稱為關機順序。 系統會定義關機順序的兩個一般類別：「正常」和「abortive (也稱為「硬) 」。 在正常關機順序中，任何已排入佇列但尚未傳送的資料，都可以在關閉連接之前傳送。 在 abortive 關機中，任何未傳送的資料都會遺失。  (正常或 abortive) 出現的關機順序，也可以用來提供 FD \_ 關閉指示給關聯的應用程式，表示正在進行關機。

另一方面，關閉通訊端會導致通訊端控制碼被解除配置，讓應用程式無法再以任何方式參考或使用通訊端。

在 Windows 通訊端中， [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 函式和 [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect) 函式都可以用來起始關機順序，而 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式則可用來解除配置通訊端控制碼，並釋出任何相關聯的資源。 不過， **導致 closesocket** 函式會隱含地導致關閉順序發生（如果尚未發生），因此會產生一些混淆。 事實上，它已經成為依賴這項功能的一般程式設計實務，並且使用 **導致 closesocket** 來起始關機順序並解除配置通訊端控制碼。

為了促進這種使用方式，通訊端介面會透過通訊端選項機制來提供控制項，讓程式設計人員能夠指出隱含關機順序是否應該是正常的或 abortive，以及 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式是否應該停止 (不會立即完成) 以允許時間正常關機順序完成。 這些重要的差異和以這種方式使用 **導致 closesocket** 的後果仍不會被廣泛瞭解。

藉由為通訊端選項建立適當的值以進行 \_ 延遲和 \_ DONTLINGER，您可以使用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函數來取得下列類型的行為：

-   Abortive 關機順序，從 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)立即返回。
-   正常關機，延遲傳回直到關閉順序完成或經過指定的時間間隔為止。 如果時間間隔在正常關機順序完成之前過期，則會發生 abortive 關機順序，而 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 會傳回。
-   正常關機、立即返回，讓關機順序在背景中完成。 雖然這是預設行為，但應用程式無法得知何時 (或) 正常關機順序是否真的完成。

使用「 \_ 延遲」和「 \_ DONTLINGER 通訊端」選項以及相關聯的 [**延遲**](/windows/desktop/api/winsock/ns-winsock-linger) 結構，會在 [**SOL \_ 通訊端通訊端選項**](sol-socket-socket-options.md) 和 **延遲** 結構的參考章節中更詳細地討論。

可以用來將連接卸載期間發生之問題的機率降至最低的其中一種技術，就是避免依賴 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)所起始的隱含關機。 相反地，請使用兩個明確關機函式的其中一個： [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 或 [**WSASendDisconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsasenddisconnect)。 這接著會導致 \_ 對等應用程式收到 FD 關閉指示，指出已收到所有擱置中的資料。 為了說明這一點，下表顯示應用程式用戶端和伺服器元件所叫用的函式，用戶端會負責起始正常關機。

| 用戶端                                                                                                                | 伺服器端                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
|  (1) 叫用 [**關機**](/windows/desktop/api/winsock/nf-winsock-shutdown) (s，SD \_ 傳送) 表示會話結束，且該用戶端不再有要傳送的資料。 |                                                                                                       |
|                                                                                                                            |  (2) 接收 FD \_ 關閉，表示正常關機進行中，而且已收到所有資料。 |
|                                                                                                                            |  (3) 傳送任何剩餘的回應資料。                                                                |
|  (本機計時的重要性，) 會取得 FD \_ READ，並呼叫 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv) 以取得伺服器所傳送的任何回應資料。  |  (4) 叫用 [**關機**](/windows/desktop/api/winsock/nf-winsock-shutdown) (s，SD \_ 傳送) 表示伺服器沒有其他要傳送的資料。  |
|  (5) 收到 FD \_ 關閉指示。                                                                                         | 只有) 叫用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 時，才 (本機計時精確度。                       |
|  (6) 叫用 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)。                                                                          |                                                                                                       |



 

 

 



