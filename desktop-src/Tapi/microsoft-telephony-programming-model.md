---
description: Microsoft 電話語音程式設計模型將通訊控制項從裝置控制抽象化，釋出使用者的應用程式和裝置製造商，從密集建置到三月的需要。
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Microsoft 電話語音程式設計模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986285"
---
# <a name="microsoft-telephony-programming-model"></a>Microsoft 電話語音程式設計模型

Microsoft 電話語音程式設計模型將通訊控制項從裝置控制抽象化，釋出使用者的應用程式和裝置製造商，從密集建置到三月的需要。 使用此模型時，使用者或伺服器應用程式不需要裝置控制的詳細資訊，且裝置不需要針對應用程式量身打造。 應用程式和裝置可以進行創新和變更，而不會對客戶呈現彼此的效用。

下圖說明如何完成此抽象概念。

![tapi 如何從裝置控制將通訊控制抽象化](images/tapicomp.png)

您可以將這些元件視為專門知識的儲存機制。 電話語音應用程式開發介面 (TAPI) 應用程式知道使用者需求、TAPI DLL 和 TAPISRV 瞭解一般電話語音，而服務提供者 (TSP 和 MSP) 瞭解詳細的裝置控制項。 應用程式撰寫者和裝置製造商只需要對彼此需求的一般知識。

-   應用程式會將 TAPI DLL 載入其進程空間，並使用 TAPI 來溝通需求。
-   TAPI 會建立與 TAPI 伺服器的 RPC 連結通訊。
-   此外，TAPI 3.x 會建立 MSP 物件，並使用一組已定義的命令、媒體服務提供者介面 (MSPI) 來與其通訊。
-   當應用程式呼叫 TAPI 操作時，TAPI 動態連結程式庫會驗證並封送處理參數，然後將資訊轉送至 TAPISRV。
-   TAPISRV 會使用電話語音服務提供者 (TSPI)  (Tsp) ，追蹤本機電腦可用的通訊資源，以及與電話語音服務提供者的介面。
-   TSP 和 MSP 之間的通訊會使用透過 TAPI DLL 和 TAPISRV 傳遞的虛擬連線進行。
-   TSP/MSP 組會提供裝置狀態和功能的相關資訊，並執行所需回應所需的特定命令。

使用此程式設計模型的結果是應用程式可以忽略或調整裝置變更，而新的裝置可以立即使用，而不是等候程式碼基底變更。 應用程式撰寫者和裝置製造商都能擴展潛在的市場佔有率。

下列主題會更詳細地說明 Microsoft 電話語音元件：

-   [TAPI 應用程式](tapi-applications.md)
-   [TAPI DLL](tapi-dll.md)
-   [TAPI 伺服器](tapi-server.md)
-   [服務提供者](service-providers.md)
-   [同步/非同步模型](synchronous-asynchronous-model.md)
-   [TAPI 資料結構](tapi-data-structures.md)
-   [服務的 TAPI 等級](tapi-levels-of-service.md)

 

 



