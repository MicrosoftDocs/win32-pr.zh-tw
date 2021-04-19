---
description: 時間軸
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: 時間軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985146"
---
# <a name="the-timeline"></a><span data-ttu-id="95be0-103">時間軸</span><span class="sxs-lookup"><span data-stu-id="95be0-103">The Timeline</span></span>

<span data-ttu-id="95be0-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="95be0-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="95be0-105">時間軸會顯示 [**IAMTimeline**](iamtimeline.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="95be0-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="95be0-106">此介面包含在時間軸上設定屬性的方法;將群組新增至時間軸;以及建立時間軸物件，例如群組、追蹤和來源。</span><span class="sxs-lookup"><span data-stu-id="95be0-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="95be0-107">若要建立新的時間軸，請呼叫標準 **CoCreateInstance** 函數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="95be0-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="95be0-108">新的時間軸是空的。</span><span class="sxs-lookup"><span data-stu-id="95be0-108">The new timeline is empty.</span></span> <span data-ttu-id="95be0-109">此時您可以載入現有的專案檔 (查看 [載入和預覽專案](loading-and-previewing-a-project.md)) ，或建立新的物件來建立時間軸， (參閱 [建立時間軸](constructing-a-timeline.md)) 。</span><span class="sxs-lookup"><span data-stu-id="95be0-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95be0-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="95be0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95be0-111">時間軸元件的總覽</span><span class="sxs-lookup"><span data-stu-id="95be0-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



