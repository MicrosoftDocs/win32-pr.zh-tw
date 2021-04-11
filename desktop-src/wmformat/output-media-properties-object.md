---
title: 輸出媒體屬性物件
description: 輸出媒體屬性物件
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK，輸出媒體屬性物件
- Advanced Systems Format (ASF) 、output media properties 物件
- ASF (Advanced Systems Format) 、output media properties 物件
- 物件、輸出媒體屬性物件
- 輸出媒體屬性物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023172"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="01068-108">輸出媒體屬性物件</span><span class="sxs-lookup"><span data-stu-id="01068-108">Output Media Properties Object</span></span>

<span data-ttu-id="01068-109">輸出媒體屬性物件是用來取出和設定 output 屬性。</span><span class="sxs-lookup"><span data-stu-id="01068-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="01068-110">輸出媒體屬性物件是針對載入至讀取器物件的檔案中所支援的資料流程輸出格式所建立。</span><span class="sxs-lookup"><span data-stu-id="01068-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="01068-111">針對壓縮的資料流程，輸出屬性取決於解壓縮編解碼器的可能輸出。</span><span class="sxs-lookup"><span data-stu-id="01068-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="01068-112">輸出媒體屬性物件是由 [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) 建立的，此方法會建立輸出媒體屬性物件，其中包含預設輸出格式的屬性。</span><span class="sxs-lookup"><span data-stu-id="01068-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="01068-113">輸出可能支援其他格式。</span><span class="sxs-lookup"><span data-stu-id="01068-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="01068-114">若要取得其他輸出格式，您可以呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) 來取得支援的輸出格式數目，然後使用 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)的呼叫對它們執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="01068-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="01068-115">**GetOutputFormat** 會建立輸出媒體屬性物件，其中填入所選輸出格式的資料。</span><span class="sxs-lookup"><span data-stu-id="01068-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="01068-116">輸出媒體屬性物件也可以使用同步讀取器來建立。</span><span class="sxs-lookup"><span data-stu-id="01068-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="01068-117">所有方法名稱與讀取器中的名稱相同，而且全部都是由 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) 介面所公開。</span><span class="sxs-lookup"><span data-stu-id="01068-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="01068-118">**GetOutputProps** 和 **GetOutputFormat** 都會將指標設定為 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) 介面。</span><span class="sxs-lookup"><span data-stu-id="01068-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="01068-119">您可以藉由呼叫 **QueryInterface** 方法來取得輸出媒體屬性物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="01068-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="01068-120">每個輸出媒體屬性物件都支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="01068-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="01068-121">介面</span><span class="sxs-lookup"><span data-stu-id="01068-121">Interface</span></span>                                          | <span data-ttu-id="01068-122">描述</span><span class="sxs-lookup"><span data-stu-id="01068-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01068-123">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="01068-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="01068-124">用作其他媒體屬性介面的基底介面， (輸入、輸出和影片) 。</span><span class="sxs-lookup"><span data-stu-id="01068-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="01068-125">**IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="01068-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="01068-126">捕獲輸出的屬性。</span><span class="sxs-lookup"><span data-stu-id="01068-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="01068-127">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="01068-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="01068-128">管理影片資料流程的屬性。</span><span class="sxs-lookup"><span data-stu-id="01068-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="01068-129">這是選擇性的介面，僅適用于影片串流。</span><span class="sxs-lookup"><span data-stu-id="01068-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01068-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="01068-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01068-131">**物件**</span><span class="sxs-lookup"><span data-stu-id="01068-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="01068-132">**讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="01068-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




