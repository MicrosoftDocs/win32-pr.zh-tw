---
title: 排程分鏡腳本
description: 建立分鏡腳本之後，動畫管理員會進行排程。
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- 分鏡腳本視窗動畫，排程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020889"
---
# <a name="schedule-a-storyboard"></a><span data-ttu-id="82c71-104">排程分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="82c71-104">Schedule a Storyboard</span></span>

<span data-ttu-id="82c71-105">建立分鏡腳本之後，動畫管理員會進行排程。</span><span class="sxs-lookup"><span data-stu-id="82c71-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="82c71-106">概觀</span><span class="sxs-lookup"><span data-stu-id="82c71-106">Overview</span></span>

<span data-ttu-id="82c71-107">根據預設，每個分鏡腳本會在排程時立即啟動。</span><span class="sxs-lookup"><span data-stu-id="82c71-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="82c71-108">這表示當腳本開始以動畫顯示一或多個變數時，它可能會中斷任何其他以動畫顯示這些相同變數的分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="82c71-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="82c71-109">不過，應用程式可以藉由判斷分鏡腳本之間的相對優先順序來指定其他行為。</span><span class="sxs-lookup"><span data-stu-id="82c71-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="82c71-110">在排程腳本之後，就無法再變更它。</span><span class="sxs-lookup"><span data-stu-id="82c71-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="82c71-111">不過，在從排程中移除分鏡腳本之後，就可以將它排程為重新播放。</span><span class="sxs-lookup"><span data-stu-id="82c71-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="82c71-112">當重複使用分鏡腳本時，開發人員應該要特別小心，因為這應該只有在沒有機會讓相同的分鏡腳本因為使用者動作已在排程中播放或排入佇列時，才需要將其排入佇列。</span><span class="sxs-lookup"><span data-stu-id="82c71-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="82c71-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="82c71-113">Example Code</span></span>

<span data-ttu-id="82c71-114">下列範例程式碼取自 Windows 動畫中的 MainWindow，範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [計時器驅動動畫](timer-driven-animation-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="82c71-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="82c71-115">它會使用 [**IUIAnimationStoryboard：： schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) 方法來排程分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="82c71-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="82c71-116">這個方法需要目前的時間做為參數。</span><span class="sxs-lookup"><span data-stu-id="82c71-116">This method requires the current time as a parameter.</span></span>


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a><span data-ttu-id="82c71-117">上一個步驟</span><span class="sxs-lookup"><span data-stu-id="82c71-117">Previous Step</span></span>

<span data-ttu-id="82c71-118">開始此步驟之前，您應該已完成此步驟： [建立分鏡腳本並加入轉換](updating---timer-driven-animation.md)。</span><span class="sxs-lookup"><span data-stu-id="82c71-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c71-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="82c71-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c71-120">**IUIAnimationStoryboard：： Schedule**</span><span class="sxs-lookup"><span data-stu-id="82c71-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="82c71-121">**IUIAnimationTimer：： GetTime**</span><span class="sxs-lookup"><span data-stu-id="82c71-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="82c71-122">分鏡腳本總覽</span><span class="sxs-lookup"><span data-stu-id="82c71-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




