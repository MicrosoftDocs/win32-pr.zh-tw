---
description: 新增來源
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: 新增來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106979709"
---
# <a name="adding-a-source"></a><span data-ttu-id="01c72-103">新增來源</span><span class="sxs-lookup"><span data-stu-id="01c72-103">Adding a Source</span></span>

<span data-ttu-id="01c72-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="01c72-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="01c72-105">建立來源物件的方式與建立其他時程表物件的方式相同。</span><span class="sxs-lookup"><span data-stu-id="01c72-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="01c72-106">不過，在將它插入至時間軸之前，您必須至少在來源上指定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="01c72-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="01c72-107">相對於時間軸的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="01c72-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="01c72-108">呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="01c72-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="01c72-109">要做為來源使用的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="01c72-109">The media file to use as a source.</span></span> <span data-ttu-id="01c72-110">使用代表檔案名的寬字元字串來呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="01c72-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="01c72-111">媒體開始和停止時間，相對於原始檔案。</span><span class="sxs-lookup"><span data-stu-id="01c72-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="01c72-112">呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="01c72-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="01c72-113">如需媒體時間的詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="01c72-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="01c72-114">在下列範例中，來源剪輯會在檔案中開始四秒。</span><span class="sxs-lookup"><span data-stu-id="01c72-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="01c72-115">媒體持續時間為10秒，時間軸持續時間長度的兩倍，表示來源會以兩倍的一般速度播放。</span><span class="sxs-lookup"><span data-stu-id="01c72-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="01c72-116">常數單位定義為 10000000 (10 ^ 7) ，等於1秒。</span><span class="sxs-lookup"><span data-stu-id="01c72-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="01c72-117">目前，DES 無法同時轉譯超過75個以視訊壓縮管理員壓縮的來源 (BC-VCM-LVM-HYPERV) 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="01c72-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="01c72-118">此外，如果整個專案包含75以上的來源，您必須使用動態重新連接，否則 DES 無法預覽專案。</span><span class="sxs-lookup"><span data-stu-id="01c72-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="01c72-119">如需詳細資訊，請參閱 [**IRenderEngine：： SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)。</span><span class="sxs-lookup"><span data-stu-id="01c72-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="01c72-120">如需來源的詳細資訊，請參閱 [使用來源](working-with-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="01c72-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="01c72-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="01c72-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01c72-122">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="01c72-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



