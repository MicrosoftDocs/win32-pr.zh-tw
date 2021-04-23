---
description: WST 解碼篩選
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908476"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="ffef5-103">WST 解碼篩選</span><span class="sxs-lookup"><span data-stu-id="ffef5-103">WST Decoder Filter</span></span>

<span data-ttu-id="ffef5-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="ffef5-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="ffef5-105">它可在 Windows XP 和 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ffef5-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="ffef5-106">從 Windows Vista 開始，DirectShow 未提供篩選來解碼全球標準 Teletext (WST) 。</span><span class="sxs-lookup"><span data-stu-id="ffef5-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="ffef5-107">WST 解碼器是一種核心模式篩選器，接受來自 [WST 編解碼器](wst-codec-filter.md) 的已解碼全球標準 Teletext 資料，並使用 Microsoft 提供的字型，將重迭 [混音](overlay-mixer-filter.md) 器上的點陣圖傳遞給釘選2。</span><span class="sxs-lookup"><span data-stu-id="ffef5-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="ffef5-108">目前只支援西歐語言;目前未提供任何 Unicode 字型。</span><span class="sxs-lookup"><span data-stu-id="ffef5-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="ffef5-109">您可以藉由呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)，使用 WST 編解碼器的輸出 pin 來自動將此篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="ffef5-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="ffef5-110">標籤</span><span class="sxs-lookup"><span data-stu-id="ffef5-110">Label</span></span> | <span data-ttu-id="ffef5-111">值</span><span class="sxs-lookup"><span data-stu-id="ffef5-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ffef5-112">篩選介面</span><span class="sxs-lookup"><span data-stu-id="ffef5-112">Filter Interfaces</span></span>                        | <span data-ttu-id="ffef5-113">ISpecifyPropertyPages、 [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="ffef5-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="ffef5-114">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ffef5-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="ffef5-115">媒體 \_ VBI、MEDIASUBTYPE \_ TELETEXT</span><span class="sxs-lookup"><span data-stu-id="ffef5-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="ffef5-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="ffef5-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="ffef5-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="ffef5-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="ffef5-118">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ffef5-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="ffef5-119">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="ffef5-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="ffef5-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="ffef5-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="ffef5-121">**IPin**</span><span class="sxs-lookup"><span data-stu-id="ffef5-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="ffef5-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="ffef5-122">Filter CLSID</span></span>                             | <span data-ttu-id="ffef5-123">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="ffef5-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="ffef5-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="ffef5-124">Property Page CLSID</span></span>                      | <span data-ttu-id="ffef5-125">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="ffef5-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="ffef5-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="ffef5-126">Executable</span></span>                               | <span data-ttu-id="ffef5-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="ffef5-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="ffef5-128">優點</span><span class="sxs-lookup"><span data-stu-id="ffef5-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="ffef5-129">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="ffef5-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="ffef5-130">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="ffef5-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ffef5-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ffef5-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="ffef5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffef5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffef5-133">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="ffef5-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ffef5-134">觀賞全球標準 Teletext</span><span class="sxs-lookup"><span data-stu-id="ffef5-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



