---
title: 建立分鏡腳本並新增轉換
description: 若要建立動畫，應用程式必須建立分鏡腳本。
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- 分鏡腳本視窗動畫，建立
- 分鏡腳本視窗動畫，新增轉換
- 轉換視窗動畫，建立
- 轉換視窗動畫，加入至分鏡腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301703"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="78177-107">建立分鏡腳本並新增轉換</span><span class="sxs-lookup"><span data-stu-id="78177-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="78177-108">若要建立動畫，應用程式必須建立分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="78177-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="78177-109">概觀</span><span class="sxs-lookup"><span data-stu-id="78177-109">Overview</span></span>

<span data-ttu-id="78177-110">建立分鏡腳本的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="78177-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="78177-111">建立分鏡腳本</span><span class="sxs-lookup"><span data-stu-id="78177-111">Create a storyboard</span></span>
2.  <span data-ttu-id="78177-112">建立一或多個轉換</span><span class="sxs-lookup"><span data-stu-id="78177-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="78177-113">將轉換新增至腳本，並指定其製作動畫的變數</span><span class="sxs-lookup"><span data-stu-id="78177-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="78177-114">您可以使用動畫管理員來建立空白的分鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="78177-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="78177-115">應用程式必須在每個分鏡腳本中填入轉換。</span><span class="sxs-lookup"><span data-stu-id="78177-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="78177-116">每個轉換會指定單一動畫變數在指定時間間隔內的變更方式。</span><span class="sxs-lookup"><span data-stu-id="78177-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="78177-117">您可以使用 Windows 動畫中包含的轉換程式庫元件來建立轉換。</span><span class="sxs-lookup"><span data-stu-id="78177-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="78177-118">或者，應用程式可以建立自己的自訂轉換，或使用協力廠商的轉換程式庫。</span><span class="sxs-lookup"><span data-stu-id="78177-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="78177-119">當應用程式將轉換新增至分鏡腳本時，它會指定轉換將會製作動畫的動畫變數。</span><span class="sxs-lookup"><span data-stu-id="78177-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="78177-120">分鏡腳本可包含一或多個動畫變數上的轉換。</span><span class="sxs-lookup"><span data-stu-id="78177-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="78177-121">更複雜的分鏡腳本可以使用主要畫面格來同步處理轉換的開始或結束，或是指定應重複 (固定次數或無限) 的分鏡腳本部分。</span><span class="sxs-lookup"><span data-stu-id="78177-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="78177-122">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="78177-122">Example Code</span></span>

<span data-ttu-id="78177-123">下列範例程式碼取自 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： ChangeColor 方法。</span><span class="sxs-lookup"><span data-stu-id="78177-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="78177-124">此範例會使用 [**IUIAnimationManager：： CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) 方法建立分鏡腳本 (步驟 1) 、使用 [**IUIAnimationTransitionLibrary：： CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) 方法建立轉換 (步驟 2) ，然後使用 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法將轉換新增至分鏡腳本 (步驟 3) 。</span><span class="sxs-lookup"><span data-stu-id="78177-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="78177-125">上一個步驟</span><span class="sxs-lookup"><span data-stu-id="78177-125">Previous Step</span></span>

<span data-ttu-id="78177-126">開始此步驟之前，您應該已完成此步驟： [讀取動畫變數值](updating---application-driven-animation.md)。</span><span class="sxs-lookup"><span data-stu-id="78177-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="78177-127">後續步驟</span><span class="sxs-lookup"><span data-stu-id="78177-127">Next Step</span></span>

<span data-ttu-id="78177-128">完成此步驟後，下一個步驟是： [排程分](scheduling-a-storyboard.md)鏡腳本。</span><span class="sxs-lookup"><span data-stu-id="78177-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78177-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="78177-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78177-130">**IUIAnimationManager::CreateStoryboard**</span><span class="sxs-lookup"><span data-stu-id="78177-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="78177-131">**IUIAnimationStoryboard::AddTransition**</span><span class="sxs-lookup"><span data-stu-id="78177-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="78177-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span><span class="sxs-lookup"><span data-stu-id="78177-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="78177-133">分鏡腳本總覽</span><span class="sxs-lookup"><span data-stu-id="78177-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




