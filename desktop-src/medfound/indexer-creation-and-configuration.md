---
description: 本主題提供有關建立媒體基礎所提供之預設索引子物件的資訊。
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: 建立和設定索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193779"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="c064a-103">建立和設定索引子</span><span class="sxs-lookup"><span data-stu-id="c064a-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="c064a-104">ASF *索引子* 是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="c064a-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c064a-105">本主題提供有關建立媒體基礎所提供之預設索引子物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="c064a-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="c064a-106">如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="c064a-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="c064a-107">**建立並初始化 ASF 索引子**</span><span class="sxs-lookup"><span data-stu-id="c064a-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="c064a-108">呼叫 [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) 函數，以接收索引子物件的 [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) 指標。</span><span class="sxs-lookup"><span data-stu-id="c064a-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="c064a-109">呼叫 [**IMFASFIndexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) 來指定索引子物件的讀取或寫入模式。</span><span class="sxs-lookup"><span data-stu-id="c064a-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="c064a-110">根據預設，索引子會設定為向前搜尋。</span><span class="sxs-lookup"><span data-stu-id="c064a-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="c064a-111">使用</span><span class="sxs-lookup"><span data-stu-id="c064a-111">Use</span></span>                       | <span data-ttu-id="c064a-112">旗標</span><span class="sxs-lookup"><span data-stu-id="c064a-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="c064a-113">讀取 (向前搜尋) </span><span class="sxs-lookup"><span data-stu-id="c064a-113">Reading (forward seeking)</span></span> | <span data-ttu-id="c064a-114">零 (預設值) </span><span class="sxs-lookup"><span data-stu-id="c064a-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="c064a-115">讀取 (反向搜尋) </span><span class="sxs-lookup"><span data-stu-id="c064a-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="c064a-116">**\_REVERSEPLAYBACK 的 MFASF 索引子 \_ 讀取 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c064a-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="c064a-117">寫入</span><span class="sxs-lookup"><span data-stu-id="c064a-117">Writing</span></span>                   | <span data-ttu-id="c064a-118">MFASF \_ 索引子 \_ 寫入 \_ 新的 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="c064a-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="c064a-119">相同的索引子實例無法用於讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="c064a-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="c064a-120">您必須設定一個或另一個的索引子。</span><span class="sxs-lookup"><span data-stu-id="c064a-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="c064a-121">呼叫 [**IMFASFIndexer：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) 以初始化索引子，方法是指定 ContentInfo 物件的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 指標，以描述要寫入或讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="c064a-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="c064a-122">ContentInfo 物件包含構成 [ASF 標頭物件](asf-file-structure.md)的資訊。</span><span class="sxs-lookup"><span data-stu-id="c064a-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="c064a-123">在產生或讀取 ASF 檔案的索引項目之前，索引子物件需要有效的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="c064a-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="c064a-124">下列程式碼範例會示範應用程式如何建立和初始化索引子物件，以使用特定的 ASF 內容。</span><span class="sxs-lookup"><span data-stu-id="c064a-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="c064a-125">ContentInfo 物件代表 ASF 標頭物件;內容會以位元組資料流程的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="c064a-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c064a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c064a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c064a-127">ASF 索引子</span><span class="sxs-lookup"><span data-stu-id="c064a-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="c064a-128">使用索引子在 ASF 檔案內搜尋</span><span class="sxs-lookup"><span data-stu-id="c064a-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="c064a-129">使用索引子來寫入新的索引</span><span class="sxs-lookup"><span data-stu-id="c064a-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



