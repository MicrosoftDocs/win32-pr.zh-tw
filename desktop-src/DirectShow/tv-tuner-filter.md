---
description: 電視調諧器篩選器
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: 電視調諧器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909026"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="1f21c-103">電視調諧器篩選器</span><span class="sxs-lookup"><span data-stu-id="1f21c-103">TV Tuner Filter</span></span>

<span data-ttu-id="1f21c-104">電視調諧器篩選器會選取要查看的類比廣播或纜線頻道。</span><span class="sxs-lookup"><span data-stu-id="1f21c-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="1f21c-105">單一輸出資料流程是類比基帶影片的硬體路徑。</span><span class="sxs-lookup"><span data-stu-id="1f21c-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="1f21c-106">此輸出應該連接到類比視頻縱橫條篩選器。</span><span class="sxs-lookup"><span data-stu-id="1f21c-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="1f21c-107">輸入 pin 包含纜線和天線輸入的輸入。</span><span class="sxs-lookup"><span data-stu-id="1f21c-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="1f21c-108">標籤</span><span class="sxs-lookup"><span data-stu-id="1f21c-108">Label</span></span> | <span data-ttu-id="1f21c-109">值</span><span class="sxs-lookup"><span data-stu-id="1f21c-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f21c-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="1f21c-110">Filter Interfaces</span></span>                        | <span data-ttu-id="1f21c-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner)、 **ISpecifyPropertyPages**、 **IPersistPropertyBag**、 **IKsObject**、 [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="1f21c-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="1f21c-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f21c-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="1f21c-113">不適用。</span><span class="sxs-lookup"><span data-stu-id="1f21c-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1f21c-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f21c-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1f21c-115">不適用。</span><span class="sxs-lookup"><span data-stu-id="1f21c-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1f21c-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f21c-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="1f21c-117">影片：媒體 \_ 類型 AnalogVideo、KSDATAFORMAT \_ 子類型 \_ NONE 音訊：媒體類型 \_ AnalogAudio、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="1f21c-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="1f21c-118">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f21c-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="1f21c-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="1f21c-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="1f21c-120">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f21c-120">Filter CLSID</span></span>                             | <span data-ttu-id="1f21c-121">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="1f21c-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="1f21c-122">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f21c-122">Property Page CLSID</span></span>                      | <span data-ttu-id="1f21c-123">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="1f21c-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="1f21c-124">可執行檔</span><span class="sxs-lookup"><span data-stu-id="1f21c-124">Executable</span></span>                               | <span data-ttu-id="1f21c-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="1f21c-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="1f21c-126">優點</span><span class="sxs-lookup"><span data-stu-id="1f21c-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="1f21c-127">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="1f21c-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="1f21c-128">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="1f21c-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1f21c-129">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="1f21c-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="1f21c-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f21c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f21c-131">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1f21c-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



