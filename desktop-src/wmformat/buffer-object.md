---
title: 緩衝區物件
description: 緩衝區物件
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- Windows Media 格式 SDK，緩衝區物件
- Advanced Systems Format (ASF) ，buffer 物件
- ASF (Advanced Systems Format) ，buffer 物件
- 物件，緩衝區物件
- 緩衝區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968271"
---
# <a name="buffer-object"></a><span data-ttu-id="d9206-108">緩衝區物件</span><span class="sxs-lookup"><span data-stu-id="d9206-108">Buffer Object</span></span>

<span data-ttu-id="d9206-109">緩衝區物件是用來保存範例，並在 Windows Media 格式 SDK 的物件和您的應用程式之間傳遞它們。</span><span class="sxs-lookup"><span data-stu-id="d9206-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="d9206-110">當您寫入檔案時，您會使用緩衝區物件，將輸入範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="d9206-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="d9206-111">當您讀取檔案時，讀取器物件或同步讀取器物件會在緩衝區物件中提供應用程式的範例。</span><span class="sxs-lookup"><span data-stu-id="d9206-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="d9206-112">針對將範例寫入檔案，您可以使用 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) 方法建立緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="d9206-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="d9206-113">若要讀取範例，讀取器物件和同步讀取器物件都會在內部建立緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="d9206-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="d9206-114">如果您選擇，您可以使用 [**IWMReaderAllocatorEx：： AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) 或 [**IWMReaderAllocatorEx：： AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)，配置您自己的緩衝區物件來讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="d9206-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="d9206-115">每個緩衝區物件都支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="d9206-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="d9206-116">介面</span><span class="sxs-lookup"><span data-stu-id="d9206-116">Interface</span></span>                          | <span data-ttu-id="d9206-117">描述</span><span class="sxs-lookup"><span data-stu-id="d9206-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d9206-118">**INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="d9206-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="d9206-119">控制項並提供緩衝區的存取權。</span><span class="sxs-lookup"><span data-stu-id="d9206-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="d9206-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="d9206-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="d9206-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="d9206-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="d9206-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="d9206-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="d9206-123">支援用於資料單位延伸的緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="d9206-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="d9206-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="d9206-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="d9206-125">列舉緩衝區屬性。</span><span class="sxs-lookup"><span data-stu-id="d9206-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d9206-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="d9206-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9206-127">**物件**</span><span class="sxs-lookup"><span data-stu-id="d9206-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




