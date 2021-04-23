---
description: 檔案寫入器篩選
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: 檔案寫入器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909686"
---
# <a name="file-writer-filter"></a><span data-ttu-id="4837f-103">檔案寫入器篩選</span><span class="sxs-lookup"><span data-stu-id="4837f-103">File Writer Filter</span></span>

<span data-ttu-id="4837f-104">檔案寫入器篩選器可以用來將檔案寫入光碟，而不管格式為何。</span><span class="sxs-lookup"><span data-stu-id="4837f-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="4837f-105">篩選器只會寫入其輸入 pin 所收到的光碟，因此必須將上游連接到可正確格式化檔案的多工器。</span><span class="sxs-lookup"><span data-stu-id="4837f-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="4837f-106">您可以使用檔案寫入器建立新的輸出檔，或指定現有的檔案;如果檔案已存在，則會以新資料完全覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="4837f-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="4837f-107">檔案寫入器篩選器會使用輸入資料流程的時間戳記做為檔案位移，並提供檔案的隨機存取。</span><span class="sxs-lookup"><span data-stu-id="4837f-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="4837f-108">它支援 **IStream** ，以允許在圖形停止之後讀取和寫入檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="4837f-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="4837f-109">為了改善效能，它也支援未緩衝的重迭寫入，並處理對應的緩衝區協商。</span><span class="sxs-lookup"><span data-stu-id="4837f-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="4837f-110">若要寫入 ASF 檔案，請使用 [WM Asf 寫入](wm-asf-writer-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="4837f-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="4837f-111">標籤</span><span class="sxs-lookup"><span data-stu-id="4837f-111">Label</span></span> | <span data-ttu-id="4837f-112">值</span><span class="sxs-lookup"><span data-stu-id="4837f-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4837f-113">篩選介面</span><span class="sxs-lookup"><span data-stu-id="4837f-113">Filter Interfaces</span></span>                        | <span data-ttu-id="4837f-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter)、 [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)、 **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="4837f-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="4837f-115">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="4837f-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="4837f-116">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="4837f-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="4837f-117">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="4837f-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="4837f-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 **IStream**</span><span class="sxs-lookup"><span data-stu-id="4837f-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="4837f-119">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="4837f-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="4837f-120">不適用</span><span class="sxs-lookup"><span data-stu-id="4837f-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="4837f-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="4837f-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="4837f-122">不適用</span><span class="sxs-lookup"><span data-stu-id="4837f-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="4837f-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="4837f-123">Filter CLSID</span></span>                             | <span data-ttu-id="4837f-124">CLSID \_ FileWriter</span><span class="sxs-lookup"><span data-stu-id="4837f-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4837f-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="4837f-125">Property Page CLSID</span></span>                      | <span data-ttu-id="4837f-126">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="4837f-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="4837f-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="4837f-127">Executable</span></span>                               | <span data-ttu-id="4837f-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="4837f-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="4837f-129">優點</span><span class="sxs-lookup"><span data-stu-id="4837f-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="4837f-130">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="4837f-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="4837f-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="4837f-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4837f-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4837f-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="4837f-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="4837f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4837f-134">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="4837f-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



