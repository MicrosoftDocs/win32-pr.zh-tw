---
description: 使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: 使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025954"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="bdeaf-103">使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出</span><span class="sxs-lookup"><span data-stu-id="bdeaf-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="bdeaf-104">資訊佇列由介面管理 (請參閱儲存、抓取及篩選 debug 訊息的 [**ID3D10InfoQueue 介面**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="bdeaf-105">佇列包含：訊息佇列、選擇性的儲存體篩選堆疊，以及選擇性的抓取篩選堆疊。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="bdeaf-106">儲存體篩選堆疊可以用來篩選您想要儲存的訊息;抓取篩選堆疊可以用來篩選您想要儲存的訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="bdeaf-107">當您篩選訊息之後，訊息將會列印到 [debug] 視窗並儲存在適當的堆疊中。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="bdeaf-108">一般而言：</span><span class="sxs-lookup"><span data-stu-id="bdeaf-108">In general:</span></span>

-   <span data-ttu-id="bdeaf-109">呼叫 [**ID3D10InfoQueue：： AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) 以產生使用者定義的訊息</span><span class="sxs-lookup"><span data-stu-id="bdeaf-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="bdeaf-110">呼叫 [**ID3D10InfoQueue：： GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) 是用來取得傳遞選擇性抓取篩選)  (的訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="bdeaf-111">登錄控制項</span><span class="sxs-lookup"><span data-stu-id="bdeaf-111">Registry Controls</span></span>

<span data-ttu-id="bdeaf-112">使用登錄機碼來調整篩選設定、調整中斷點，以及將偵錯工具輸出靜音。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="bdeaf-113">Debug 層會檢查這些登錄機碼的路徑;將會使用第一個找到的路徑。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="bdeaf-114">HKCU \\ Software \\ Microsoft \\ Direct3D \\<使用者定義的子機碼></span><span class="sxs-lookup"><span data-stu-id="bdeaf-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="bdeaf-115">HKLM \\ Software \\ Microsoft \\ Direct3D \\<使用者定義的子機碼></span><span class="sxs-lookup"><span data-stu-id="bdeaf-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="bdeaf-116">HKCU \\ Software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="bdeaf-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="bdeaf-117">其中：</span><span class="sxs-lookup"><span data-stu-id="bdeaf-117">Where:</span></span>

-   <span data-ttu-id="bdeaf-118">HKCU 適用于 HKEY \_ 目前的 \_ 使用者，以及 HKLM 的 HKEY \_ 本機 \_ 電腦。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="bdeaf-119"><使用者定義的子機碼> 是用來儲存應用程式之偵錯工具設定的任意名稱</span><span class="sxs-lookup"><span data-stu-id="bdeaf-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="bdeaf-120">使用登錄機碼篩選調試訊息</span><span class="sxs-lookup"><span data-stu-id="bdeaf-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="bdeaf-121">如果登錄包含 InfoQueueStorageFilterOverride 機碼 (且為非零) ，則可以藉由新增下列登錄控制項來篩選訊息 (和偵錯工具輸出) 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="bdeaf-122">DWORD 靜音 \_ 類別 \_ \* -如果此索引鍵為非零，則為 Debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="bdeaf-123">DWORD 靜音 \_ 嚴重性 \_ \* -如果此索引鍵為非零，則會停用偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="bdeaf-124">DWORD 靜音 \_ 識別碼 \_ \* -訊息名稱或數位可用於 (， \* 就像 \_ \_ \* 先前) 所述的 BreakOn 識別碼一樣。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="bdeaf-125">如果此索引鍵為非零，則會停用偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="bdeaf-126">DWORD \_ 非靜音嚴重性 \_ 資訊-如果此索引鍵不是零，則會啟用偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="bdeaf-127">根據預設，啟用 InfoQueueStorageFilterOverride 時，會將具有嚴重性資訊的 debug 訊息設為靜音，因此此索引鍵可讓資訊重新開啟。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="bdeaf-128">這些控制項會變更是否錄製或顯示訊息;它們不會影響 API 是否通過或失敗。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="bdeaf-129">使用登錄機碼設定中斷條件</span><span class="sxs-lookup"><span data-stu-id="bdeaf-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="bdeaf-130">您可以使用下列登錄機碼強制應用程式在訊息上中斷。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="bdeaf-131">**EnableBreakOnMessage** -此金鑰可讓 (的訊息中斷，並導致我的 SetBreakOnCategory () /SetBreakOnSeverity () /SetBreakOnID () 設定) 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="bdeaf-132">實際要中斷的訊息會使用下列定義的一或多個 BreakOn 值來定義 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="bdeaf-133">\**BreakOn \_\_類別 \** _-在任何通過儲存體篩選的訊息上中斷。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="bdeaf-134">\_ 這是其中一個 D3D10 \_ 訊息 \_ 類別目錄訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="bdeaf-135">\**BreakOn \_\_嚴重性 \** _-在傳遞儲存體篩選器的任何訊息上中斷。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="bdeaf-136">\_ 這是其中一項 D3D10 \_ 訊息 \_ 嚴重性 \_ 訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="bdeaf-137">\**BreakOn \_\_識別碼 \** _-在傳遞儲存體篩選器的任何訊息上中斷。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="bdeaf-138">\_ 這是其中一個 D3D10 \_ 訊息 \_ 識別碼 \_ 訊息，也可以是錯誤列舉的數值。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="bdeaf-139">例如，假設識別碼為 "D3D10 \_ message \_ id 假設" 的訊息在 \_ D3D10 \_ 訊息識別碼列舉中具有值 123 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="bdeaf-140">在此情況下，建立值 BreakOn \_ 識別碼 \_ 假設 = 1 或 BreakOn \_ 識別碼 \_ 123 = 1，就會在遇到識別碼 D3D10 \_ 訊息識別碼假設的訊息時，完成相同的動作 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="bdeaf-141">使用登錄機碼的靜音調試輸出</span><span class="sxs-lookup"><span data-stu-id="bdeaf-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="bdeaf-142">您可以使用 MuteDebugOutput 索引鍵將調試輸出靜音。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="bdeaf-143">在登錄中存在此值會強制覆寫 InfoQueue 的 [**ID3D10InfoQueue：： SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) 方法。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="bdeaf-144">MuteDebugOutput 會停止傳遞存放裝置篩選器的訊息，使其無法傳送至 debug 輸出。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="bdeaf-145">停用 Debug Layer 訊息</span><span class="sxs-lookup"><span data-stu-id="bdeaf-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="bdeaf-146">您可以透過使用 [**ID3D10InfoQueue：： AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries)來指定篩選，在執行時間將 individualy 或做為群組來停用調試層訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="bdeaf-147">**ID3D10InfoQueue：： AddStorageFilterEntries** 的 *pFilter* 引數會採用包含允許清單和拒絕清單的 [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter)結構。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="bdeaf-148">[允許] 和 [拒絕] 清單是由 [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選 \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) 結構所描述，可讓您依分類、嚴重性和個別訊息識別碼來指定篩選。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="bdeaf-149">下列程式碼是設定 [**ID3D10InfoQueue 介面**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) 的範例，以拒絕 D3D10 \_ 訊息 \_ 識別碼 \_ 裝置 \_ 繪製 \_ 索引 \_ 緩衝區 \_ 太 \_ 小的訊息。</span><span class="sxs-lookup"><span data-stu-id="bdeaf-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="bdeaf-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdeaf-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdeaf-151">API 層</span><span class="sxs-lookup"><span data-stu-id="bdeaf-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="bdeaf-152"> (Direct3D 10) 的 API 功能 </span><span class="sxs-lookup"><span data-stu-id="bdeaf-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



