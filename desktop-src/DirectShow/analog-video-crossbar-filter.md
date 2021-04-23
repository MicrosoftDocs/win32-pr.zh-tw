---
description: 類比視頻縱橫條篩選
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: 類比視頻縱橫條篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909596"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="89cd0-103">類比視頻縱橫條篩選</span><span class="sxs-lookup"><span data-stu-id="89cd0-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="89cd0-104">類比視頻縱橫條篩選器表示影片啟用裝置上的一種影片，可支援 Windows Driver Model (WDM) 。</span><span class="sxs-lookup"><span data-stu-id="89cd0-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="89cd0-105">此篩選器是在 WDM 串流裝置上 crossbars 的包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="89cd0-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="89cd0-106">篩選的易記名稱取自裝置。</span><span class="sxs-lookup"><span data-stu-id="89cd0-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="89cd0-107">每個輸出圖釘都代表類比基帶影片的硬體路徑。</span><span class="sxs-lookup"><span data-stu-id="89cd0-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="89cd0-108">其中一個輸入針腳是電視調諧器 ([Tv 調諧器篩選器](tv-tuner-filter.md)) 。</span><span class="sxs-lookup"><span data-stu-id="89cd0-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="89cd0-109">其他輸入 pin 支援影片或音訊串流。</span><span class="sxs-lookup"><span data-stu-id="89cd0-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="89cd0-110">篩選準則支援下游連接所支援的任何媒體子類型和格式。</span><span class="sxs-lookup"><span data-stu-id="89cd0-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="89cd0-111">您無法使用 CoCreateInstance 直接建立此篩選器。</span><span class="sxs-lookup"><span data-stu-id="89cd0-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="89cd0-112">[**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面會視需要自動將此篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="89cd0-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="89cd0-113">如需包裝函式篩選和 WDM 串流裝置的詳細資訊，請參閱 [硬體裝置如何參與篩選圖形](how-hardware-devices-participate-in-the-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="89cd0-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="89cd0-114">標籤</span><span class="sxs-lookup"><span data-stu-id="89cd0-114">Label</span></span> | <span data-ttu-id="89cd0-115">值</span><span class="sxs-lookup"><span data-stu-id="89cd0-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89cd0-116">篩選介面</span><span class="sxs-lookup"><span data-stu-id="89cd0-116">Filter Interfaces</span></span>                        | <span data-ttu-id="89cd0-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)、ISpecifyPropertyPages、IPersistPropertyBag、IPersistStream</span><span class="sxs-lookup"><span data-stu-id="89cd0-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="89cd0-118">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="89cd0-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="89cd0-119">媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="89cd0-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="89cd0-120">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="89cd0-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="89cd0-121">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="89cd0-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="89cd0-122">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="89cd0-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="89cd0-123">媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="89cd0-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="89cd0-124">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="89cd0-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="89cd0-125">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="89cd0-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="89cd0-126">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="89cd0-126">Filter CLSID</span></span>                             | <span data-ttu-id="89cd0-127">不適用</span><span class="sxs-lookup"><span data-stu-id="89cd0-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="89cd0-128">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="89cd0-128">Property Page CLSID</span></span>                      | <span data-ttu-id="89cd0-129">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="89cd0-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="89cd0-130">可執行檔</span><span class="sxs-lookup"><span data-stu-id="89cd0-130">Executable</span></span>                               | <span data-ttu-id="89cd0-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="89cd0-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="89cd0-132">優點</span><span class="sxs-lookup"><span data-stu-id="89cd0-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="89cd0-133">驅動程式相依。</span><span class="sxs-lookup"><span data-stu-id="89cd0-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="89cd0-134">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="89cd0-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="89cd0-135">AM \_ KSCATEGORY \_ 縱橫</span><span class="sxs-lookup"><span data-stu-id="89cd0-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="89cd0-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="89cd0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89cd0-137">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="89cd0-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="89cd0-138">使用 Crossbars</span><span class="sxs-lookup"><span data-stu-id="89cd0-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



