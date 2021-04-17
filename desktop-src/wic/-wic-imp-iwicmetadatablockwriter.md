---
description: 執行 IWICMetadataBlockWriter
ms.assetid: 31824f21-04b1-45ca-adfa-15fd348e14a1
title: 執行 IWICMetadataBlockWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62044ce9695a45a8fe052d67479158aa9e4baf6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514173"
---
# <a name="implementing-iwicmetadatablockwriter"></a><span data-ttu-id="5f2c4-103">執行 IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="5f2c4-103">Implementing IWICMetadataBlockWriter</span></span>

## <a name="iwicmetadatablockwriter"></a><span data-ttu-id="5f2c4-104">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="5f2c4-104">IWICMetadataBlockWriter</span></span>

-   [<span data-ttu-id="5f2c4-105">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="5f2c4-105">InitializeFromBlockReader</span></span>](#initializefromblockreader)
-   [<span data-ttu-id="5f2c4-106">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-106">GetWriterByIndex</span></span>](#getwriterbyindex)
-   [<span data-ttu-id="5f2c4-107">AddWriter</span><span class="sxs-lookup"><span data-stu-id="5f2c4-107">AddWriter</span></span>](#addwriter)
-   [<span data-ttu-id="5f2c4-108">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-108">SetWriterByIndex</span></span>](#setwriterbyindex)
-   [<span data-ttu-id="5f2c4-109">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-109">RemoveWriterByIndex</span></span>](#removewriterbyindex)

<span data-ttu-id="5f2c4-110">框架層級編碼類別會執行這個介面，以公開所有中繼資料區塊，並為每個區塊要求適當的中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-110">The frame-level encoding class implements this interface to expose all the metadata blocks and request the appropriate metadata writer for each block.</span></span> <span data-ttu-id="5f2c4-111">如果您的影像格式支援全域中繼資料，在任何個別的框架之外，您也應該在容器層級編碼器類別上執行此介面。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-111">If your image format supports global metadata, outside of any individual frame, you should also implement this interface on the container-level encoder class.</span></span> <span data-ttu-id="5f2c4-112">如需元資料處理程式的更詳細討論，請參閱有關如何執行 WIC-Enabled 的解碼器一節中的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 一節。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-112">For a more detailed discussion of metadata handlers, refer to the section on the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the section on Implementing a WIC-Enabled Decoder.</span></span>

``` syntax
interface IWICMetadataBlockWriter : IWICMetadataBlockReader
{
   // All methods required
   HRESULT InitializeFromBlockReader ( IWICMetadataBlockReader *pIMDBlockReader );
   HRESULT GetWriterByIndex ( UINT nIndex, IWICMetadataWriter **ppIMetadataWriter );
   HRESULT AddWriter (IWICMetadataWriter *pIMetadataWriter );
   HRESULT SetWriterByIndex ( UINT nIndex, IWICMetadataWriter *pIMetadataWriter );
   HRESULT RemoveWriterByIndex ( UINT nIndex );
}
```

### <a name="initializefromblockreader"></a><span data-ttu-id="5f2c4-113">InitializeFromBlockReader</span><span class="sxs-lookup"><span data-stu-id="5f2c4-113">InitializeFromBlockReader</span></span>

<span data-ttu-id="5f2c4-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) 會使用 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 來初始化區塊寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-114">[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader) uses an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) to initialize the block writer.</span></span> <span data-ttu-id="5f2c4-115">您可以從解碼映射的解碼器取得 **IWICMetadataBlockReader** 。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-115">You can get the **IWICMetadataBlockReader** from the decoder that decoded the image.</span></span>


```C++
UINT blockCount = 0;
IWICMetadataReader* pMetadataReader = NULL;
IWICMetadataWriter** ppMetadataWriter = NULL;
HRESULT hr;

hr = m_pBlockReader->GetCount(&blockCount);
ppMetadataWriter = IWICMetadataWriter*[blockCount];

for (UINT x=0; x < blockCount; x++)
{
   hr = m_pBlockReader->GetReaderByIndex(&pMetadataReader);
   hr = m_pComponentFactory->CreateMetadataWriterFromReader(
         pMetadataReader, NULL, &ppMetadataWriter[x]);
}
```



<span data-ttu-id="5f2c4-116">由於使用 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)初始化 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)會將 **IWICMetadataBlockReader** 物件所公開之每個中繼資料讀取器的中繼資料寫入器具現化，因此應用程式不需要明確要求每個中繼資料區塊的寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-116">Because initializing the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) with an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) instantiates a metadata writer for each metadata reader exposed by the **IWICMetadataBlockReader** object, the application doesn’t have to explicitly request a writer for each block of metadata.</span></span>

### <a name="getwriterbyindex"></a><span data-ttu-id="5f2c4-117">GetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-117">GetWriterByIndex</span></span>

<span data-ttu-id="5f2c4-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) 會傳回第 n 個中繼資料區塊的 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) 物件，其中 n 是在 *nIndex* 參數中傳遞的值。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-118">[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex) returns the [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) object for the nth metadata block, where n is the value passed in the *nIndex* parameter.</span></span> <span data-ttu-id="5f2c4-119">如果沒有任何已註冊的中繼資料寫入器可處理第 n 個區塊中的元資料類型，則元件 factory 會傳回未知的元資料處理程式，此處理程式會將中繼資料區塊視為二進位大型物件 (BLOB) 。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-119">If there is no metadata writer registered that can handle the type of metadata in the nth block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB).</span></span> <span data-ttu-id="5f2c4-120">它會將它序列化為位資料流程，而不會嘗試加以剖析。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-120">It will serialize it out as a bit stream without attempting to parse it.</span></span>

### <a name="addwriter"></a><span data-ttu-id="5f2c4-121">AddWriter</span><span class="sxs-lookup"><span data-stu-id="5f2c4-121">AddWriter</span></span>

<span data-ttu-id="5f2c4-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) 可讓呼叫者加入新的中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-122">[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter) allows a caller to add a new metadata writer.</span></span> <span data-ttu-id="5f2c4-123">如果應用程式想要加入的中繼資料，與任何現有的中繼資料區塊不同，則這是必要的。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-123">This is required if an application wants to add metadata of a different format than any of the existing metadata blocks.</span></span> <span data-ttu-id="5f2c4-124">例如，應用程式可能會想要新增一些 XMP 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-124">For example, an application may want to add some XMP metadata.</span></span> <span data-ttu-id="5f2c4-125">如果沒有任何現有的 XMP 中繼資料區塊，則應用程式必須具現化 XMP 中繼資料寫入器，並使用 **AddWriter** 方法將它包含在中繼資料寫入器的集合中。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-125">If there is no existing XMP metadata block, the application must instantiate an XMP metadata writer and use the **AddWriter** method to include it in the collection of metadata writers.</span></span>

### <a name="setwriterbyindex"></a><span data-ttu-id="5f2c4-126">SetWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-126">SetWriterByIndex</span></span>

<span data-ttu-id="5f2c4-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) 是用來在集合中的特定索引處加入中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-127">[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex) is used to add a metadata writer at a specific index in the collection.</span></span> <span data-ttu-id="5f2c4-128">如果中繼資料寫入器目前存在於該索引中，則新的寫入器應該取代它。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-128">If a metadata writer is currently exists at that index, the new one should replace it.</span></span>

### <a name="removewriterbyindex"></a><span data-ttu-id="5f2c4-129">RemoveWriterByIndex</span><span class="sxs-lookup"><span data-stu-id="5f2c4-129">RemoveWriterByIndex</span></span>

<span data-ttu-id="5f2c4-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) 是用來從集合中移除中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="5f2c4-130">[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex) is used to remove a metadata writer from the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f2c4-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f2c4-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5f2c4-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="5f2c4-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f2c4-133">執行 IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="5f2c4-133">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="5f2c4-134">編解碼器安裝和註冊</span><span class="sxs-lookup"><span data-stu-id="5f2c4-134">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="5f2c4-135">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="5f2c4-135">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5f2c4-136">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="5f2c4-136">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



