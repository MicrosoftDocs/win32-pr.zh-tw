---
title: 設定索引子
description: 設定索引子
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows媒體格式 SDK，設定索引子
- Advanced Systems Format (ASF) 、設定索引子
- ASF (Advanced Systems Format) ，設定索引子
- 索引，設定索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a624a4ed9ae749559a1908e3809500bf8aece2b29b8ad406769c5f639e547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845623"
---
# <a name="to-configure-the-indexer"></a>設定索引子

您可以先設定索引子，再使用它來為 ASF 檔案編制索引。 檔案中的每個資料流程都可以個別設定，或者您可以為所有資料流程設定相同的設定。

如果您要設定多個 steams 以在檔案中編制索引，您必須設定全部，然後開始編制索引。 如果您設定和編制資料流程的索引，然後在相同的檔案中設定另一個資料流程，則再次啟動索引子將會刪除第一個索引。 這是為了遵守 ASF 檔案格式。

下列程式碼顯示如何設定索引子。 此程式碼會假設要編制索引的檔案有兩個數據流：第一個是不需要編制索引的音訊資料流程，而第二個則是影片串流。 此程式碼只會顯示如何設定索引子。 若要為檔案編制索引，您必須遵循中提供的步驟 [來為 ASF 檔案編制索引](to-index-an-asf-file.md)。


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> 預設索引類型 WMT \_ 它最近的 \_ \_ 清除 \_ 點。 雖然您可以將索引類型設定為其他值，但是這樣做會降低搜尋效能。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMIndexer2：： Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**為 ASF 檔案編制索引**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




