---
title: 為 ASF 檔案編制索引
description: 為 ASF 檔案編制索引
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows媒體格式 SDK，為 ASF 檔案編制索引
- Advanced Systems Format (ASF) 、編制檔案索引
- ASF (Advanced 系統格式) 、編制檔案索引
- 索引，為 ASF 檔案編制索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845576"
---
# <a name="to-index-an-asf-file"></a>為 ASF 檔案編制索引

為 ASF 檔案編制索引的程式非常簡單。 呼叫 [**IWMIndexer：： StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) 並傳遞檔案名。 索引子會執行其餘工作。 對 **StartIndexing** 的呼叫是非同步，因此必須使用 **OnStatus** 回呼來監視狀態。

下列程式碼說明如何編制 ASF 檔案的索引。 如果您想要在為檔案編制索引之前設定索引子，您必須包含包含在中的範例程式碼， [以設定索引子](to-configure-the-indexer.md)。

在此範例中，指向事件的控制碼必須建立為全域變數，才能讓回呼存取它。 下列宣告應該會出現在全域範圍中。


```C++
HANDLE g_hEvent = NULL;

```



在更實際的案例中，事件控制碼應該是類別的資料成員，其中包含回呼和啟動索引子的邏輯。

在呼叫 **IWMIndexer：： StartIndexing** 之後，索引子會將數個事件傳送至 **OnStatus** 回呼。 您可以視需要為您的應用程式加以攔截。 您至少需要在索引完成時，將 WMT 設為 [ \_ 已關閉]。 在 **OnStatus** 回呼的執行中，于訊息切換內使用下列邏輯。


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



在這個範例中，假設您是透過名為 MyCallback 的物件來存取 **OnStatus** 回呼的實作為。 如需有關搭配此 SDK 使用事件和回呼的詳細資訊，請參閱 [使用回呼方法](using-the-callback-methods.md)。


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMIndexer 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**設定索引子**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




