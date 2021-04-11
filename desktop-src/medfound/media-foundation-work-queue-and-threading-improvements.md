---
description: 本主題說明 Microsoft 媒體基礎平臺中工作佇列和執行緒 Windows 8 的改善。
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: 工作佇列和執行緒改進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027682"
---
# <a name="work-queue-and-threading-improvements"></a>工作佇列和執行緒改進

本主題說明 Microsoft 媒體基礎平臺中工作佇列和執行緒 Windows 8 的改善。

-   [Windows 7 行為](#windows-7-behavior)
    -   [工作佇列](#work-queues)
    -   [MMCSS 支援](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Windows 8 改進](#windows-8-improvements)
    -   [多執行緒工作佇列](#multithreaded-work-queues)
    -   [共用工作工作佇列](#shared-task-work-queues)
    -   [等候佇列](#wait-queue)
    -   [MMCSS 支援的增強功能](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [拓撲分支](#topology-branches)
-   [建議](#recommendations)
-   [總結](#summary)
-   [相關主題](#related-topics)

## <a name="windows-7-behavior"></a>Windows 7 行為

本節摘要說明 Windows 7 中媒體基礎工作佇列的行為。

### <a name="work-queues"></a>工作佇列

媒體基礎平臺會建立數個標準的工作佇列。 只有兩個記錄為一般應用程式用途：

-   **MFASYNC \_ 回呼 \_ 佇列 \_ 標準**
-   **MFASYNC \_ 回呼 \_ 佇列 \_ LONG \_ 函數**

應用程式或元件可以藉由呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) 或 [**MFAllocateWorkQueueEx**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex)來配置新的工作佇列。 **MFAllocateWorkQueueEx** 函式會定義兩種類型的工作佇列：

-   **MF \_標準 \_ WORKQUEUE** 會建立工作佇列，而不使用訊息迴圈。
-   **MF \_視窗 \_ WORKQUEUE** 會使用訊息迴圈來建立工作佇列。

若要將工作專案排入佇列，請呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 或 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)。 平臺會藉由叫用呼叫端提供的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)執行來執行工作專案。 在 Windows 7 及更早版本中，平臺會為每個工作佇列建立一個執行緒。

### <a name="mmcss-support"></a>MMCSS 支援

[多媒體類別](../procthread/multimedia-class-scheduler-service.md)排程器服務 (MMCSS) 管理執行緒優先順序，讓多媒體應用程式取得 cpu 時間的一般配量，而不會拒絕 cpu 資源給較低優先順序的應用程式。 MMCSS 會定義一組具有不同 CPU 使用率配置 *檔的工作* 。 當執行緒加入 MMCSS 工作時，MMCSS 會根據數個因素來設定執行緒的優先順序：

-   工作的基本優先權，設定于登錄中。
-   相對執行緒優先順序，會呼叫 [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)在執行時間設定。
-   各種執行時間特性（例如應用程式是否在前景），以及每個 MMCSS 類別中的執行緒所耗用的 CPU 時間量。

應用程式可以藉由呼叫 [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss)，向 MMCSS 註冊工作佇列。 此函式會使用工作佇列識別碼、MMCSS 類別 (工作名稱) ，以及 MMCSS 工作識別碼。 就內部而言，它會使用工作名稱和工作識別碼來呼叫 [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) 。 使用 MMCSS 註冊工作佇列之後，您可以藉由呼叫 [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) 和 [**MFGetWorkQueueMMCSSTaskId**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid)來取得類別和工作識別碼。

[媒體會話](media-session.md)透過 [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)介面，提供對這些 api 較高層級的存取。 此介面提供兩種主要方法：

| 方法                                                                                                            | 描述                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | 使用 MMCSS 工作註冊工作佇列。 這個方法基本上是 [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss)上的精簡型包裝函式，但是您可以傳遞 **MFASYNC \_ 回呼 \_ 佇列 \_** 的值，以一次註冊所有平臺工作佇列。 |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | 使用工作佇列註冊拓撲的分支。                                                                                                                                                                                                                                         |



 

若要註冊拓撲分支，請執行下列動作。

1.  在分支的來源節點上設定 [ [MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼](mf-toponode-workqueue-id-attribute.md) ] 屬性。 使用任何應用程式定義的值。
2.  （選擇性）設定 **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別** ，以將工作佇列加入 MMCSS 工作。
3.  針對已解析的拓撲呼叫 [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) 。

媒體會話會為每個唯一值的 [MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼](mf-toponode-workqueue-id-attribute.md)配置新的工作佇列。 針對每個拓撲分支，會在指派給分支的工作佇列上執行非同步管線作業。

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

[**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)介面適用于建立自己的執行緒或使用工作佇列進行非同步作業的管線元件。 媒體會話會使用此介面來通知管線元件的正確行為，如下所示：

-   如果管線元件建立背景工作執行緒， [**IMFRealTimeClient：： RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) 方法會通知元件要加入的 MMCSS 類別。
-   如果管線元件使用工作佇列， [**IMFRealTimeClient：： SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) 方法會告知元件要使用的工作佇列。

通常，管線元件會使用執行緒或工作佇列來執行非同步工作，但不能同時使用這兩種方法。

## <a name="windows-8-improvements"></a>Windows 8 改進

### <a name="multithreaded-work-queues"></a>多執行緒工作佇列

在 Windows 8 中，媒體基礎支援稱為 *多執行緒佇列* 的新工作佇列類型。 多執行緒佇列使用系統執行緒集區來分派工作專案。 多執行緒佇列的縮放比例優於先前的單一執行緒佇列。 例如，

-   有幾個元件可以共用多執行緒佇列，而不會彼此封鎖，而需要建立較少的執行緒。

-   工作專案已優化，以避免在已設定事件時進行內容切換。 這比建立您自己的執行緒來等候事件更有效率。

使用 [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)時，應用程式應該避免啟動執行緒，而應該改為使用工作佇列。 為了達成此目的，應用程式應該執行 [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) ，而不是使用 [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) 和 [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads)。

當媒體基礎的平臺初始化時，它會建立具有識別碼 **MFASYNC \_ 回呼 \_ 佇列 \_ 多** 執行緒的多執行緒佇列。

多執行緒佇列不會將工作專案序列化。 只要執行緒集區中的執行緒變成可用，就會分派佇列中的下一個工作專案。 呼叫端必須確定已正確序列化工作。 為了簡化此作業，媒體基礎定義了 *序列工作佇列*。 序列佇列會包裝另一個工作佇列，但保證完全序列化執行。 在前一個專案完成之前，不會分派佇列中的下一個專案。

下列程式碼會透過平臺多執行緒佇列建立序列化程式佇列。


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



一個以上的序列佇列可以包裝相同的多執行緒佇列。 然後，序列佇列會共用相同的執行緒集區，並在每個佇列內強制執行序列化執行。

在 Windows 8 之前存在的標準工作佇列，現在會實作為包裝平臺多執行緒佇列的序列工作佇列。 這種變更可保留回溯相容性。

### <a name="shared-task-work-queues"></a>共用工作工作佇列

若要正確使用核心排程器，您所使用的每個 MMCSS 工作應該會有一個多執行緒的工作佇列。 媒體基礎平臺會視需要配置這些設定，每個進程最多可為每個 MMCSS 工作一個。 若要取得特定 MMCSS 工作的共用工作佇列，請呼叫 [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) 並指定工作名稱。 函數會查閱資料表中的工作名稱。 如果工作佇列尚未存在於此工作中，此函式會配置新的 MT 工作佇列，並立即將其加入 MMCSS 工作。 如果工作佇列已經存在於該工作中，此函式會傳回現有工作佇列的識別碼。

### <a name="wait-queue"></a>等候佇列

*等候佇列* 是一種特殊的平臺工作佇列，可等候事件收到信號。 如果元件需要等候事件收到信號，則可以使用等候佇列，而不是建立背景工作執行緒來等候事件。

若要使用等候佇列，請呼叫 [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)。 這些參數包括事件控制碼和 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 指標。 當事件收到信號時，等候佇列就會叫用您的回呼。 有單一的平臺等候佇列;應用程式無法建立自己的等候佇列。

### <a name="enhancements-to-mmcss-support"></a>MMCSS 支援的增強功能

下列新的媒體基礎平臺函數與 MMCSS 相關。



| 函式                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | 使用 MMCSS 註冊工作佇列。 此函式包含指定相對執行緒優先順序的參數。 就內部而言，此值會轉譯成 [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)的呼叫。                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | 查詢工作佇列的優先順序。                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | 使用 MMCSS 工作註冊所有平臺的工作佇列。 此函式類似于 [**IMFWorkQueueServices：： BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) 方法，但可以在不建立媒體會話實例的情況下使用。 此外，函式還包含參數來指定基底線程優先權。 |



 

使用媒體會話的應用程式應該將「適用于音訊轉譯」分支的 [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性設定為「音訊」。 將影片轉譯分支的屬性設定為「播放」。

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

[**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)介面，用來取代執行非同步作業之管線元件的 IMFRealTimeClient。



| 方法                                                             | 描述                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | 通知元件向 MMCSS 註冊其執行緒。 這個方法相當於 [**IMFRealTimeClient：： RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads)，但它會加入基底線程優先順序的參數。 |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | 通知元件使用特定的工作佇列。 這個方法相當於 [**IMFReadTimeClient：： SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue)，但它會加入工作專案優先順序的參數。               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | 通知元件從 MMCSS 取消註冊其執行緒。 這個方法與 [**IMFRealTimeClient：： UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) 方法相同。                                       |



 

管線元件應該使用工作佇列，且不應該建立背景工作執行緒，原因如下：

-   工作佇列的擴充更好，因為它們使用 OS 執行緒集區。
-   平臺會處理使用 MMCSS 註冊工作佇列的詳細資料。
-   工作者執行緒很容易就會造成難以進行調試的鎖死。

此外，如果您需要將非同步作業序列化，請考慮使用序列化程式工作佇列。

### <a name="topology-branches"></a>拓撲分支

如果 [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性使用 MMCSS 註冊拓撲分支，WINDOWS 8 媒體會話使用共用的 MT 工作佇列。 在舊版的 Windows 中，媒體會話已配置新的工作佇列。

針對使用 MMCSS 註冊拓撲分支，定義了兩個新的屬性。



| 屬性                                                                            | 描述                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY](mf-toponode-workqueue-mmcss-priority.md) | 指定基底線程優先權。 |
| [MF \_ TOPONODE \_ WORKQUEUE \_ 專案 \_ 優先順序](mf-toponode-workqueue-item-priority.md)   | 指定工作專案優先權。   |



 

## <a name="recommendations"></a>建議

-   使用媒體會話的應用程式應將 [ \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別](mf-toponode-workqueue-mmcss-class-attribute.md) 設定為音訊轉譯分支的 "音訊"，以及影片轉譯分支的「播放」。
-   使用媒體會話的應用程式應該在拓撲上呼叫 [**IMFWorkQueueServices：： BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) 。
-   針對管線元件，建議使用工作佇列，而不是背景工作執行緒。 如果元件使用工作佇列或背景工作執行緒，請執行 [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)。
-   請勿建立私用工作佇列，因為這樣會失去平臺工作佇列的目的。 請使用平臺多執行緒佇列或包裝平臺多執行緒佇列的序列佇列。
-   如果您需要序列化非同步作業，請使用序列佇列。

## <a name="summary"></a>總結

下列媒體基礎與執行緒和工作佇列相關的平臺 Api 是 Windows 8 的新。

-   [MF \_ TOPONODE \_ WORKQUEUE \_ 專案 \_ 優先順序](mf-toponode-workqueue-item-priority.md)
-   [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY](mf-toponode-workqueue-mmcss-priority.md)
-   [**MFAllocateSerialWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**MFUnregisterPlatformFromMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作佇列](work-queues.md)
</dt> </dl>

 

 
