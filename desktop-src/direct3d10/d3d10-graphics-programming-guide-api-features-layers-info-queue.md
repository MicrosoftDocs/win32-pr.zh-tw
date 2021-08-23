---
description: 使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: 使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753828"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>使用 ID3D10InfoQueue (Direct3D 10) 自訂調試輸出

資訊佇列由介面管理 (請參閱儲存、抓取及篩選 debug 訊息的 [**ID3D10InfoQueue 介面**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) 。 佇列包含：訊息佇列、選擇性的儲存體篩選堆疊，以及選擇性的抓取篩選堆疊。 儲存體篩選堆疊可以用來篩選您想要儲存的訊息;抓取篩選堆疊可以用來篩選您想要儲存的訊息。 當您篩選訊息之後，訊息將會列印到 [debug] 視窗並儲存在適當的堆疊中。

一般而言：

-   呼叫 [**ID3D10InfoQueue：： AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) 以產生使用者定義的訊息
-   呼叫 [**ID3D10InfoQueue：： GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) 是用來取得傳遞選擇性抓取篩選)  (的訊息。

## <a name="registry-controls"></a>登錄控制項

使用登錄機碼來調整篩選設定、調整中斷點，以及將偵錯工具輸出靜音。 Debug 層會檢查這些登錄機碼的路徑;將會使用第一個找到的路徑。

1.  HKCU \\ Software \\ Microsoft \\ Direct3D \\<使用者定義的子機碼>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<使用者定義的子機碼>
3.  HKCU \\ Software \\ Microsoft \\ Direct3D

其中：

-   HKCU 適用于 HKEY \_ 目前的 \_ 使用者，以及 HKLM 的 HKEY \_ 本機 \_ 電腦。
-   <使用者定義的子機碼> 是用來儲存應用程式之偵錯工具設定的任意名稱

### <a name="filtering-debug-messages-using-registry-keys"></a>使用登錄機碼篩選調試訊息

如果登錄包含 InfoQueueStorageFilterOverride 機碼 (且為非零) ，則可以藉由新增下列登錄控制項來篩選訊息 (和偵錯工具輸出) 。

-   DWORD 靜音 \_ 類別 \_ \* -如果此索引鍵為非零，則為 Debug 輸出。
-   DWORD 靜音 \_ 嚴重性 \_ \* -如果此索引鍵為非零，則會停用偵錯工具輸出。
-   DWORD 靜音 \_ 識別碼 \_ \* -訊息名稱或數位可用於 (， \* 就像 \_ \_ \* 先前) 所述的 BreakOn 識別碼一樣。 如果此索引鍵為非零，則會停用偵錯工具輸出。
-   DWORD \_ 非靜音嚴重性 \_ 資訊-如果此索引鍵不是零，則會啟用偵錯工具輸出。 根據預設，啟用 InfoQueueStorageFilterOverride 時，會將具有嚴重性資訊的 debug 訊息設為靜音，因此此索引鍵可讓資訊重新開啟。

這些控制項會變更是否錄製或顯示訊息;它們不會影響 API 是否通過或失敗。

### <a name="setting-break-conditions-using-registry-keys"></a>使用登錄機碼設定中斷條件

您可以使用下列登錄機碼強制應用程式在訊息上中斷。

**EnableBreakOnMessage** -此金鑰可讓 (的訊息中斷，並導致我的 SetBreakOnCategory () /SetBreakOnSeverity () /SetBreakOnID () 設定) 。 實際要中斷的訊息會使用下列定義的一或多個 BreakOn 值來定義 \_ \* 。

-   **BreakOn \_\_類別 \** _-在任何通過儲存體篩選的訊息上中斷。 \_ 這是其中一個 D3D10 \_ 訊息 \_ 類別目錄訊息。
-   **BreakOn \_\_嚴重性 \** _-在傳遞儲存體篩選器的任何訊息上中斷。 \_ 這是其中一項 D3D10 \_ 訊息 \_ 嚴重性 \_ 訊息。
-   **BreakOn \_\_識別碼 \** _-在傳遞儲存體篩選器的任何訊息上中斷。 \_ 這是其中一個 D3D10 \_ 訊息 \_ 識別碼 \_ 訊息，也可以是錯誤列舉的數值。 例如，假設識別碼為 "D3D10 \_ message \_ id 假設" 的訊息在 \_ D3D10 \_ 訊息識別碼列舉中具有值 123 \_ 。 在此情況下，建立值 BreakOn \_ 識別碼 \_ 假設 = 1 或 BreakOn \_ 識別碼 \_ 123 = 1，就會在遇到識別碼 D3D10 \_ 訊息識別碼假設的訊息時，完成相同的動作 \_ \_ 。

### <a name="muting-debug-output-using-registry-keys"></a>使用登錄機碼的靜音調試輸出

您可以使用 MuteDebugOutput 索引鍵將調試輸出靜音。 在登錄中存在此值會強制覆寫 InfoQueue 的 [**ID3D10InfoQueue：： SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) 方法。 MuteDebugOutput 會停止傳遞存放裝置篩選器的訊息，使其無法傳送至 debug 輸出。

## <a name="disabling-debug-layer-messages"></a>停用 Debug Layer 訊息

您可以透過使用 [**ID3D10InfoQueue：： AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries)來指定篩選，在執行時間將 individualy 或做為群組來停用調試層訊息。 **ID3D10InfoQueue：： AddStorageFilterEntries** 的 *pFilter* 引數會採用包含允許清單和拒絕清單的 [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter)結構。 [允許] 和 [拒絕] 清單是由 [**D3D10 \_ 資訊 \_ 佇列 \_ 篩選 \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) 結構所描述，可讓您依分類、嚴重性和個別訊息識別碼來指定篩選。

下列程式碼是設定 [**ID3D10InfoQueue 介面**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) 的範例，以拒絕 D3D10 \_ 訊息 \_ 識別碼 \_ 裝置 \_ 繪製 \_ 索引 \_ 緩衝區 \_ 太 \_ 小的訊息。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[API 層](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[ (Direct3D 10) 的 API 功能 ](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



