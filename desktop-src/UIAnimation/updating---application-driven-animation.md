---
title: 讀取動畫變數值
description: 每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- 動畫變數 Windows 動畫，讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967272"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="106c3-104">讀取動畫變數值</span><span class="sxs-lookup"><span data-stu-id="106c3-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="106c3-105">每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。</span><span class="sxs-lookup"><span data-stu-id="106c3-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="106c3-106">概觀</span><span class="sxs-lookup"><span data-stu-id="106c3-106">Overview</span></span>

<span data-ttu-id="106c3-107">繪製框架時，應用程式可以使用 [**IUIAnimationVariable：： GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) 或 [**IUIAnimationVariable：： GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) 方法來要求任何會影響框架內視覺效果的動畫變數值。</span><span class="sxs-lookup"><span data-stu-id="106c3-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="106c3-108">您可以將動畫變數裁剪至值範圍 ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) 和 [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) ，並使用指定的舍入配置 ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) ，來要求其值四捨五入為整數。</span><span class="sxs-lookup"><span data-stu-id="106c3-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="106c3-109">應用程式可以使用 [**IUIAnimationVariable：： SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) 或 [**IUIAnimationVariable：： SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) 方法來註冊一個或多個變數變更處理常式，只在變數的值變更時才接收通知，而不是讀取每個框架的所有變數值， ([**IUIAnimationVariableChangeHandler：： OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) 或四捨五入值 ([**IUIAnimationVariableIntegerChangeHandler：： OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)) 。</span><span class="sxs-lookup"><span data-stu-id="106c3-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="106c3-110">若要識別傳遞給變數變更處理常式的變數，應用程式可以使用 [**IUIAnimationVariable：： SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) 方法，將標記套用至變數。</span><span class="sxs-lookup"><span data-stu-id="106c3-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="106c3-111">這些是 \* 由應用程式所解讀的物件 (IUnknown) 、整陣列。</span><span class="sxs-lookup"><span data-stu-id="106c3-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="106c3-112">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="106c3-112">Example Code</span></span>

<span data-ttu-id="106c3-113">下列範例程式碼取自 Windows 動畫範例 [方格](/windows/desktop/UIAnimation/grid-layout-sample)配置中的縮圖 .cpp;請參閱 CMainWindow：： Render 方法。</span><span class="sxs-lookup"><span data-stu-id="106c3-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="106c3-114">它會使用 [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) 方法將值讀取為浮點值。</span><span class="sxs-lookup"><span data-stu-id="106c3-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="106c3-115">下列範例程式碼取自 Windows 動畫範例 [計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：:D rawBackground 方法。</span><span class="sxs-lookup"><span data-stu-id="106c3-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="106c3-116">它會使用 [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) 方法將值讀取為整數值。</span><span class="sxs-lookup"><span data-stu-id="106c3-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="106c3-117">上一個步驟</span><span class="sxs-lookup"><span data-stu-id="106c3-117">Previous Step</span></span>

<span data-ttu-id="106c3-118">開始此步驟之前，您應該已完成此步驟： [更新動畫管理員並繪製畫面](introducing-windows-animation-manager.md)格。</span><span class="sxs-lookup"><span data-stu-id="106c3-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="106c3-119">後續步驟</span><span class="sxs-lookup"><span data-stu-id="106c3-119">Next Step</span></span>

<span data-ttu-id="106c3-120">完成此步驟後，下一個步驟是： [建立分鏡腳本並加入轉換](updating---timer-driven-animation.md)。</span><span class="sxs-lookup"><span data-stu-id="106c3-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="106c3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="106c3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="106c3-122">**IUIAnimationVariable::GetIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="106c3-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="106c3-123">**IUIAnimationVariable：： GetValue**</span><span class="sxs-lookup"><span data-stu-id="106c3-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="106c3-124">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="106c3-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 