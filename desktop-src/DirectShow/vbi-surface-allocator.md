---
description: VBI 介面配置器
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI 介面配置器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693759"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="e3c27-103">VBI 介面配置器</span><span class="sxs-lookup"><span data-stu-id="e3c27-103">VBI Surface Allocator</span></span>

<span data-ttu-id="e3c27-104">VBI 介面配置器會使用硬體視訊連接埠捕獲案例，控制類比電視圖中 VBI 緩衝區的配置。</span><span class="sxs-lookup"><span data-stu-id="e3c27-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="e3c27-105">使用 Bt829 解碼器這類裝置時，框架緩衝區可能包含多個 VBI capture 緩衝區，而這些緩衝區可透過以一般方式（通常是影片埠）的專屬硬體機制來存取。</span><span class="sxs-lookup"><span data-stu-id="e3c27-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="e3c27-106">VBI 介面配置器篩選器會從 capture 篩選器連線下游，而且沒有輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="e3c27-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="e3c27-107">此篩選器會與重迭 [混音](overlay-mixer-filter.md) 器 (緊密配合，透過 DirectDraw) 在硬體視訊連接埠上執行協調作業，並利用相同的有限 SVGA 框架緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="e3c27-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c27-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="e3c27-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="e3c27-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e3c27-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="e3c27-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e3c27-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="e3c27-111">媒體媒體 \_ 、MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="e3c27-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="e3c27-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="e3c27-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="e3c27-113">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="e3c27-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="e3c27-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e3c27-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="e3c27-115">媒體 \_ 值 Null、MEDIASUBTYPE \_ Null。</span><span class="sxs-lookup"><span data-stu-id="e3c27-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="e3c27-116"> (沒有任何東西連接到輸出釘選。 ) </span><span class="sxs-lookup"><span data-stu-id="e3c27-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="e3c27-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="e3c27-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="e3c27-118">不適用。</span><span class="sxs-lookup"><span data-stu-id="e3c27-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="e3c27-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="e3c27-119">Filter CLSID</span></span>                             | <span data-ttu-id="e3c27-120">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="e3c27-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="e3c27-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="e3c27-121">Property Page CLSID</span></span>                      | <span data-ttu-id="e3c27-122">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="e3c27-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="e3c27-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="e3c27-123">Executable</span></span>                               | <span data-ttu-id="e3c27-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="e3c27-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="e3c27-125">優點</span><span class="sxs-lookup"><span data-stu-id="e3c27-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="e3c27-126">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="e3c27-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="e3c27-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="e3c27-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e3c27-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e3c27-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e3c27-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3c27-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c27-130">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="e3c27-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



