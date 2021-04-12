---
description: 電視調諧器篩選器
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: 電視調諧器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320399"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="1354d-103">電視調諧器篩選器</span><span class="sxs-lookup"><span data-stu-id="1354d-103">TV Tuner Filter</span></span>

<span data-ttu-id="1354d-104">電視調諧器篩選器會選取要查看的類比廣播或纜線頻道。</span><span class="sxs-lookup"><span data-stu-id="1354d-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="1354d-105">單一輸出資料流程是類比基帶影片的硬體路徑。</span><span class="sxs-lookup"><span data-stu-id="1354d-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="1354d-106">此輸出應該連接到類比視頻縱橫條篩選器。</span><span class="sxs-lookup"><span data-stu-id="1354d-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="1354d-107">輸入 pin 包含纜線和天線輸入的輸入。</span><span class="sxs-lookup"><span data-stu-id="1354d-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1354d-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="1354d-108">Filter Interfaces</span></span>                        | <span data-ttu-id="1354d-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner)、 **ISpecifyPropertyPages**、 **IPersistPropertyBag**、 **IKsObject**、 [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="1354d-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="1354d-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1354d-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="1354d-111">不適用。</span><span class="sxs-lookup"><span data-stu-id="1354d-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1354d-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1354d-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1354d-113">不適用。</span><span class="sxs-lookup"><span data-stu-id="1354d-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1354d-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1354d-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="1354d-115">影片：媒體 \_ 類型 AnalogVideo、KSDATAFORMAT \_ 子類型 \_ NONE 音訊：媒體類型 \_ AnalogAudio、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="1354d-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="1354d-116">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1354d-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="1354d-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="1354d-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="1354d-118">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="1354d-118">Filter CLSID</span></span>                             | <span data-ttu-id="1354d-119">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="1354d-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="1354d-120">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="1354d-120">Property Page CLSID</span></span>                      | <span data-ttu-id="1354d-121">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="1354d-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="1354d-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="1354d-122">Executable</span></span>                               | <span data-ttu-id="1354d-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="1354d-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="1354d-124">優點</span><span class="sxs-lookup"><span data-stu-id="1354d-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="1354d-125">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="1354d-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="1354d-126">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="1354d-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1354d-127">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="1354d-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="1354d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1354d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1354d-129">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1354d-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



