---
description: 類比視頻縱橫條篩選
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: 類比視頻縱橫條篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935797"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="d144f-103">類比視頻縱橫條篩選</span><span class="sxs-lookup"><span data-stu-id="d144f-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="d144f-104">類比視頻縱橫條篩選器表示影片啟用裝置上的一種影片，可支援 Windows Driver Model (WDM) 。</span><span class="sxs-lookup"><span data-stu-id="d144f-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="d144f-105">此篩選器是在 WDM 串流裝置上 crossbars 的包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="d144f-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="d144f-106">篩選的易記名稱取自裝置。</span><span class="sxs-lookup"><span data-stu-id="d144f-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="d144f-107">每個輸出圖釘都代表類比基帶影片的硬體路徑。</span><span class="sxs-lookup"><span data-stu-id="d144f-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="d144f-108">其中一個輸入針腳是電視調諧器 ([Tv 調諧器篩選器](tv-tuner-filter.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d144f-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="d144f-109">其他輸入 pin 支援影片或音訊串流。</span><span class="sxs-lookup"><span data-stu-id="d144f-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="d144f-110">篩選準則支援下游連接所支援的任何媒體子類型和格式。</span><span class="sxs-lookup"><span data-stu-id="d144f-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="d144f-111">您無法使用 CoCreateInstance 直接建立此篩選器。</span><span class="sxs-lookup"><span data-stu-id="d144f-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="d144f-112">[**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面會視需要自動將此篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="d144f-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="d144f-113">如需包裝函式篩選和 WDM 串流裝置的詳細資訊，請參閱 [硬體裝置如何參與篩選圖形](how-hardware-devices-participate-in-the-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="d144f-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d144f-114">篩選介面</span><span class="sxs-lookup"><span data-stu-id="d144f-114">Filter Interfaces</span></span>                        | <span data-ttu-id="d144f-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)、ISpecifyPropertyPages、IPersistPropertyBag、IPersistStream</span><span class="sxs-lookup"><span data-stu-id="d144f-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="d144f-116">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="d144f-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="d144f-117">媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="d144f-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="d144f-118">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="d144f-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="d144f-119">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d144f-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="d144f-120">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="d144f-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="d144f-121">媒體 \_ AnalogAudio，媒體媒體 \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="d144f-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="d144f-122">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="d144f-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="d144f-123">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d144f-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="d144f-124">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="d144f-124">Filter CLSID</span></span>                             | <span data-ttu-id="d144f-125">不適用</span><span class="sxs-lookup"><span data-stu-id="d144f-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="d144f-126">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="d144f-126">Property Page CLSID</span></span>                      | <span data-ttu-id="d144f-127">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="d144f-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="d144f-128">可執行檔</span><span class="sxs-lookup"><span data-stu-id="d144f-128">Executable</span></span>                               | <span data-ttu-id="d144f-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="d144f-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="d144f-130">優點</span><span class="sxs-lookup"><span data-stu-id="d144f-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="d144f-131">驅動程式相依。</span><span class="sxs-lookup"><span data-stu-id="d144f-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="d144f-132">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="d144f-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d144f-133">AM \_ KSCATEGORY \_ 縱橫</span><span class="sxs-lookup"><span data-stu-id="d144f-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="d144f-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="d144f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d144f-135">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="d144f-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d144f-136">使用 Crossbars</span><span class="sxs-lookup"><span data-stu-id="d144f-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



