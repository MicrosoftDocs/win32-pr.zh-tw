---
title: 設定索引子
description: 設定索引子
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK，設定索引子
- Advanced Systems Format (ASF) 、設定索引子
- ASF (Advanced Systems Format) ，設定索引子
- 索引，設定索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374506"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="64c33-107">設定索引子</span><span class="sxs-lookup"><span data-stu-id="64c33-107">To Configure the Indexer</span></span>

<span data-ttu-id="64c33-108">您可以先設定索引子，再使用它來為 ASF 檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="64c33-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="64c33-109">檔案中的每個資料流程都可以個別設定，或者您可以為所有資料流程設定相同的設定。</span><span class="sxs-lookup"><span data-stu-id="64c33-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="64c33-110">如果您要設定多個 steams 以在檔案中編制索引，您必須設定全部，然後開始編制索引。</span><span class="sxs-lookup"><span data-stu-id="64c33-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="64c33-111">如果您設定和編制資料流程的索引，然後在相同的檔案中設定另一個資料流程，則再次啟動索引子將會刪除第一個索引。</span><span class="sxs-lookup"><span data-stu-id="64c33-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="64c33-112">這是為了遵守 ASF 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="64c33-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="64c33-113">下列程式碼顯示如何設定索引子。</span><span class="sxs-lookup"><span data-stu-id="64c33-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="64c33-114">此程式碼會假設要編制索引的檔案有兩個數據流：第一個是不需要編制索引的音訊資料流程，而第二個則是影片串流。</span><span class="sxs-lookup"><span data-stu-id="64c33-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="64c33-115">此程式碼只會顯示如何設定索引子。</span><span class="sxs-lookup"><span data-stu-id="64c33-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="64c33-116">若要為檔案編制索引，您必須遵循中提供的步驟 [來為 ASF 檔案編制索引](to-index-an-asf-file.md)。</span><span class="sxs-lookup"><span data-stu-id="64c33-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


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
> <span data-ttu-id="64c33-117">預設索引類型 WMT \_ 它最近的 \_ \_ 清除 \_ 點。</span><span class="sxs-lookup"><span data-stu-id="64c33-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="64c33-118">雖然您可以將索引類型設定為其他值，但是這樣做會降低搜尋效能。</span><span class="sxs-lookup"><span data-stu-id="64c33-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64c33-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="64c33-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64c33-120">**IWMIndexer2：： Configure**</span><span class="sxs-lookup"><span data-stu-id="64c33-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="64c33-121">**為 ASF 檔案編制索引**</span><span class="sxs-lookup"><span data-stu-id="64c33-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="64c33-122">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="64c33-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="64c33-123">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="64c33-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




