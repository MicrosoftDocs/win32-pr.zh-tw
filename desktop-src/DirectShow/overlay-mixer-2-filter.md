---
description: 覆蓋混音器2篩選
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: 覆蓋混音器2篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997467"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="9786d-103">覆蓋混音器2篩選</span><span class="sxs-lookup"><span data-stu-id="9786d-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="9786d-104">覆迭混音器2篩選與覆迭 [混音](overlay-mixer-filter.md) 器篩選器相同，不同之處如下：</span><span class="sxs-lookup"><span data-stu-id="9786d-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="9786d-105">它僅支援具有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9786d-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="9786d-106">它有更高的優點，可讓它自動新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="9786d-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="9786d-107">系統會提供重迭混音器2，讓篩選圖形管理員在轉譯非 DVD MPEG-2 影片時，將它新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="9786d-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="9786d-108">選擇是否要使用覆迭混音器或覆迭混音器2，是由建立圖形的元件（[篩選圖形管理員]、[Capture Graph Builder] 或 [DVD 圖形產生器]）所處理。</span><span class="sxs-lookup"><span data-stu-id="9786d-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="9786d-109">從應用程式的觀點來看，它們是相同的篩選器，具有相同的介面和功能。</span><span class="sxs-lookup"><span data-stu-id="9786d-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="9786d-110">下表包含重迭混音器2的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="9786d-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="9786d-111">針對其他所有篩選資料，請參閱重迭混音器的檔。</span><span class="sxs-lookup"><span data-stu-id="9786d-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9786d-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="9786d-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="9786d-113">格式類型： Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="9786d-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9786d-114">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="9786d-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="9786d-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="9786d-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9786d-116"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="9786d-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="9786d-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="9786d-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="9786d-118">Windows Vista 或更新版本： MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="9786d-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9786d-119">在 Windows Vista 或更新版本中， \_ \_ \_ 因為較新的影片轉譯器 (VMR-7、VMR-9 和 EVR) 全部支援 **VIDEOINFOHEADER2** 格式，所以不需要使用覆迭混音器，因此不會使用覆迭混音器2篩選器的優點。</span><span class="sxs-lookup"><span data-stu-id="9786d-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9786d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9786d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9786d-121">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="9786d-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



