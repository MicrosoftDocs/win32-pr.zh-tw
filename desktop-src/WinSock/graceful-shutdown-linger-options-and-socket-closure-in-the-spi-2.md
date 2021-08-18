---
description: 請務必區分關閉通訊端連線和關閉通訊端。
ms.assetid: f076b1ec-6b96-4386-8519-4728e0a2b1ff
title: SPI 中的正常關機、延遲選項和通訊端關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5791732404948fe59d3f5c15c2ac46cdbba8d8327fb3dc5f794be1f070a9eeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132131"
---
# <a name="graceful-shutdown-linger-options-and-socket-closure-in-the-spi"></a>SPI 中的正常關機、延遲選項和通訊端關閉

請務必區分關閉通訊端連線和關閉通訊端。 關閉通訊端連線時，會在這兩個端點之間交換通訊協定訊息，而這也稱為關機順序。 系統會定義關機順序的兩個一般類別： [正常] 和 [abortive]。 在正常關機順序中，任何已排入佇列但尚未傳送的資料，都可以在關閉連接之前傳送。 在 abortive 關機中，任何未傳送的資料都會遺失。  (正常或 abortive) 出現的關機順序，也可以用來提供 FD \_ 關閉指示給關聯的應用程式，表示正在進行關機。 另一方面，關閉通訊端會導致通訊端控制碼被解除配置，讓應用程式無法再以任何方式參考或使用通訊端。

在 Windows 通訊端中，可以使用 [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))函式和 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))函式來起始關機順序，而 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))函式則可用來解除配置通訊端控制碼，並釋出任何相關聯的資源。 不過， **WSPCloseSocket** 函式會隱含地導致關閉順序發生（如果尚未發生），因此會產生一些混淆。 事實上，它已經成為依賴這項功能的一般程式設計實務，並且使用 **WSPCloseSocket** 來起始關機順序並解除配置通訊端控制碼。

為了促進這種使用方式，通訊端介面會透過通訊端選項機制提供控制項，讓程式設計人員能夠指出隱含關機順序是否應該是正常的或 abortive，以及函式是否應該停止運作，而不是) 立即完成，以允許正常關機順序完成的時間。

藉由為通訊端選項建立適當的值以進行 \_ 延遲和 \_ DONTLINGER，您可以使用 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) 函數來取得下列類型的行為。

-   Abortive 關機順序，從 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))立即返回。
-   正常關機，延遲會在關閉順序完成或經過指定的時間間隔後傳回。 如果時間間隔在正常關機順序完成之前過期，則會發生 abortive 關機順序，而 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) 會傳回。
-   正常關機、立即傳回，並允許關機順序在背景中完成。 這是預設行為。 不過，請注意，應用程式無法得知何時 (或) 正常關機順序是否完成。

可以用來將連接卸載期間發生之問題的機率降至最低的其中一種技術，就不會依賴 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))所起始的隱含關機。 相反地，會使用兩個明確關機函式的其中一個 ([**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) 或 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))) 。 這會導致 \_ 對等應用程式收到 FD 關閉指示，指出已收到所有擱置中的資料。 為了說明這一點，下表顯示應用程式用戶端和伺服器元件所叫用的函式，用戶端會負責起始正常關機。

| 用戶端                                                                                                                         | 伺服器端                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
|  (1) 叫用 [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*、SD \_ 傳送) 以通知會話結束，且該用戶端不再有要傳送的資料。 |                                                                                                              |
|                                                                                                                                     |  (2) 接收 FD \_ 關閉，表示正常關機進行中，而且已收到所有資料。        |
|                                                                                                                                     |  (3) 傳送任何剩餘的回應資料。                                                                       |
|  (5 ' ) 會取得 FD \_ READ 和 invoke 接收，以取得伺服器所傳送的任何回應資料。                                                         |  (4) 叫用 [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (*s*，SD \_ 傳送) 表示伺服器沒有其他要傳送的資料。 |
|  (5) 收到 FD \_ 關閉指示。                                                                                                  |  (4 ' ) 叫用 [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                      |
|  (6) 叫用 [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                              |                                                                                                              |



 

時間序列是從步驟 (1) 至用戶端與伺服器之間的步驟 (6) 進行維護。除了步驟 (4 ' ) 和 (5 ' ) 這種情況下，只有本機計時重要性的意義是，步驟 (5) 在用戶端上執行步驟 (5」，而步驟 ) 4」 (則是在伺服器端執行步驟 ) 4 (，與遠端方沒有時間關聯性。

 

 
