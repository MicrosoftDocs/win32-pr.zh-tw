---
description: VBI 介面配置器
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI 介面配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909006"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="9b18e-103">VBI 介面配置器</span><span class="sxs-lookup"><span data-stu-id="9b18e-103">VBI Surface Allocator</span></span>

<span data-ttu-id="9b18e-104">VBI 介面配置器會使用硬體視訊連接埠捕獲案例，控制類比電視圖中 VBI 緩衝區的配置。</span><span class="sxs-lookup"><span data-stu-id="9b18e-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="9b18e-105">使用 Bt829 解碼器這類裝置時，框架緩衝區可能包含多個 VBI capture 緩衝區，而這些緩衝區可透過以一般方式（通常是影片埠）的專屬硬體機制來存取。</span><span class="sxs-lookup"><span data-stu-id="9b18e-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="9b18e-106">VBI 介面配置器篩選器會從 capture 篩選器連線下游，而且沒有輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="9b18e-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="9b18e-107">此篩選器會與重迭 [混音](overlay-mixer-filter.md) 器 (緊密配合，透過 DirectDraw) 在硬體視訊連接埠上執行協調作業，並利用相同的有限 SVGA 框架緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="9b18e-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="9b18e-108">標籤</span><span class="sxs-lookup"><span data-stu-id="9b18e-108">Label</span></span> | <span data-ttu-id="9b18e-109">值</span><span class="sxs-lookup"><span data-stu-id="9b18e-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9b18e-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="9b18e-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="9b18e-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="9b18e-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="9b18e-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9b18e-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="9b18e-113">媒體媒體 \_ 、MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="9b18e-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="9b18e-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="9b18e-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="9b18e-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9b18e-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="9b18e-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9b18e-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="9b18e-117">媒體 \_ 值 Null、MEDIASUBTYPE \_ Null。</span><span class="sxs-lookup"><span data-stu-id="9b18e-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="9b18e-118"> (沒有任何東西連接到輸出釘選。 ) </span><span class="sxs-lookup"><span data-stu-id="9b18e-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="9b18e-119">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="9b18e-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="9b18e-120">不適用。</span><span class="sxs-lookup"><span data-stu-id="9b18e-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="9b18e-121">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="9b18e-121">Filter CLSID</span></span>                             | <span data-ttu-id="9b18e-122">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="9b18e-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="9b18e-123">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="9b18e-123">Property Page CLSID</span></span>                      | <span data-ttu-id="9b18e-124">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="9b18e-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="9b18e-125">可執行檔</span><span class="sxs-lookup"><span data-stu-id="9b18e-125">Executable</span></span>                               | <span data-ttu-id="9b18e-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="9b18e-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="9b18e-127">優點</span><span class="sxs-lookup"><span data-stu-id="9b18e-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="9b18e-128">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="9b18e-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="9b18e-129">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="9b18e-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9b18e-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="9b18e-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="9b18e-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b18e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b18e-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="9b18e-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



