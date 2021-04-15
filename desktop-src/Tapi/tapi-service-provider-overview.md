---
description: TAPI 應用程式位於自己的進程空間中。
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: TAPI 服務提供者總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554298"
---
# <a name="tapi-service-provider-overview"></a>TAPI 服務提供者總覽

TAPI 應用程式位於自己的進程空間中。 TAPI 應用程式會載入 Tapi32.dll 或 Tapi3.dll 至其進程，而 TAPI 會透過私用 RPC 介面與 TAPISRV 通訊。 TSP 會在 TAPISRV 的內容中執行。 給定的 TSP 可能位於使用者電腦以外的電腦上，並使用遠端 TSP 存取。 TAPISRV 會實作為 SVCHOST 內的服務進程。 MSP 存在於應用程式的進程空間內，一律為本機。

TSP/MSP 組可以視為具有虛擬私人通訊路徑。 您可以使用不透明的緩衝區（不是由 TAPISRV 或 TAPI DLL 來解讀），在這兩者之間傳送資訊。

某些服務提供者會執行涉及硬體的特定作業。 TAPI 2.x 提供透過 [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) 或 [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) 函式存取這類作業的功能。 TAPI 3.x 會公開 [提供者特定的介面](./provider-specific-interfaces.md)。

下圖說明控制項和資訊的流程，其中顯示一部獨立的 TSP (Unimodem) 和一組 TSP/MSP 組 (h.) 。

![獨立的 tsp 和成對的 tsp/msp 控制與資訊的流程](images/tsp-msp1.png)

下圖說明包含 TSP 和 MSP 之來電的進度。

![具有 tsp 和 msp 的撥入電話](images/tspmspin.png)

## <a name="incoming-call-setup"></a>撥入電話設定

-   TSP 會將 [**一行 \_ NEWCALL**](line-newcall.md) 訊息傳送至 TAPISRV。 [**通話狀態**](./linecallstate--constants.md)為 LINECALLSTATE 供應專案 \_ 。
-   TAPISRV 會通知用戶端呼叫。
-   TAPI3 會建立 TAPI Call 物件，然後呼叫由 MSP 所執行的 [**ITMSPAddress：： CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall)。
-   MSP 會根據呼叫所需的 [**媒體類型**](./tapimediatype--constants.md) ，建立 msp 呼叫物件和預設串流。 它會傳回 MSP 呼叫物件的 IUnknown 指標。
-   TAPI3 會將 MSP 呼叫物件匯總至 TAPI 呼叫物件，讓應用程式可以使用 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 等介面。 然後，它會通知應用程式有新的呼叫。

然後，應用程式可以使用 [**ITStream：： SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) 等方法來完成通話完成的準備工作。

## <a name="incoming-call-completion"></a>撥入電話完成

-   應用程式會呼叫 [**ITBasicCallControl：：解答**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)。
-   TAPI3 呼叫 [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer)。
-   TAPISERV 會呼叫 [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)。
-   TSP 起始通話串流。 通常，TSP 會將訊息傳送至對應的 MSP，而 MSP 會啟動串流。 在某些 TSP/MSP 實施中，TSP 會啟動串流。

## <a name="tspmsp-communication-during-call-progress"></a>通話過程中的 TSP/MSP 通訊

進行呼叫之後，TSP 和 MSP 會透過 TAPISRV 和 TAPI3 傳遞不透明的緩衝區來進行通訊。

-   TSP 將 [**\_ SENDMSPDATA**](line-sendmspdata.md) 訊息傳送至 TAPISRV，以將資訊傳送至 MSP。
-   MSP 會透過 [**ITMSPAddress：： ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) 方法接收來自 TSP 的資訊。 如果資料與 MSP 呼叫物件相關，則會以該方法的參數形式提供 MSP 呼叫物件的介面指標。
-   MSP 會將 MSP \_ TSP \_ 資料事件傳送到 TAPI 3，以將資訊傳送至 TSP。
-   TSP 會透過 [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) 函式接收來自 MSP 的資訊。

服務提供者之間的確切程式和通訊內容，是指定的 TSP/MSP 集合專屬的。

> [!Note]  
> 對於外寄呼叫，MSP 通常會知道 TSP 之前的呼叫。 如果 MSP 嘗試在 TSP 告知來電之前與 TSP 進行通訊，則通訊會失敗。 當 MSP 和 TSP 需要交換有關特定通話的資訊時，TSP 應該起始通訊。

 

 

 
