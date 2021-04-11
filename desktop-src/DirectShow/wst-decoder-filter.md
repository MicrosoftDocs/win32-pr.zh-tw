---
description: WST 解碼篩選
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848423"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="9d7cd-103">WST 解碼篩選</span><span class="sxs-lookup"><span data-stu-id="9d7cd-103">WST Decoder Filter</span></span>

<span data-ttu-id="9d7cd-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="9d7cd-105">它可在 Windows XP 和 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="9d7cd-106">從 Windows Vista 開始，DirectShow 未提供篩選來解碼全球標準 Teletext (WST) 。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="9d7cd-107">WST 解碼器是一種核心模式篩選器，接受來自 [WST 編解碼器](wst-codec-filter.md) 的已解碼全球標準 Teletext 資料，並使用 Microsoft 提供的字型，將重迭 [混音](overlay-mixer-filter.md) 器上的點陣圖傳遞給釘選2。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="9d7cd-108">目前只支援西歐語言;目前未提供任何 Unicode 字型。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="9d7cd-109">您可以藉由呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)，使用 WST 編解碼器的輸出 pin 來自動將此篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="9d7cd-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9d7cd-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="9d7cd-110">Filter Interfaces</span></span>                        | <span data-ttu-id="9d7cd-111">ISpecifyPropertyPages、 [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="9d7cd-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="9d7cd-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9d7cd-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="9d7cd-113">媒體 \_ VBI、MEDIASUBTYPE \_ TELETEXT</span><span class="sxs-lookup"><span data-stu-id="9d7cd-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="9d7cd-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="9d7cd-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="9d7cd-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9d7cd-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="9d7cd-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9d7cd-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="9d7cd-117">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="9d7cd-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="9d7cd-118">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="9d7cd-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="9d7cd-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9d7cd-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="9d7cd-120">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="9d7cd-120">Filter CLSID</span></span>                             | <span data-ttu-id="9d7cd-121">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="9d7cd-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="9d7cd-122">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="9d7cd-122">Property Page CLSID</span></span>                      | <span data-ttu-id="9d7cd-123">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="9d7cd-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="9d7cd-124">可執行檔</span><span class="sxs-lookup"><span data-stu-id="9d7cd-124">Executable</span></span>                               | <span data-ttu-id="9d7cd-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="9d7cd-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="9d7cd-126">優點</span><span class="sxs-lookup"><span data-stu-id="9d7cd-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="9d7cd-127">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="9d7cd-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="9d7cd-128">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="9d7cd-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9d7cd-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="9d7cd-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="9d7cd-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d7cd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d7cd-131">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="9d7cd-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9d7cd-132">觀賞全球標準 Teletext</span><span class="sxs-lookup"><span data-stu-id="9d7cd-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



