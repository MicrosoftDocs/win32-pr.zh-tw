---
title: 建立動畫變數
description: 應用程式必須針對每個要使用 Windows 動畫製作動畫的視覺特性建立動畫變數。
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- 動畫變數 Windows 動畫，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382486"
---
# <a name="create-animation-variables"></a><span data-ttu-id="d4a10-104">建立動畫變數</span><span class="sxs-lookup"><span data-stu-id="d4a10-104">Create Animation Variables</span></span>

<span data-ttu-id="d4a10-105">應用程式必須針對每個要使用 Windows 動畫製作動畫的視覺特性建立動畫變數。</span><span class="sxs-lookup"><span data-stu-id="d4a10-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="d4a10-106">概觀</span><span class="sxs-lookup"><span data-stu-id="d4a10-106">Overview</span></span>

<span data-ttu-id="d4a10-107">動畫變數是使用動畫管理員建立的，而且只要需要，應用程式應保留每個變數的參考。</span><span class="sxs-lookup"><span data-stu-id="d4a10-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="d4a10-108">您的應用程式通常會在繪製動畫的視覺物件時，同時建立每個動畫變數。</span><span class="sxs-lookup"><span data-stu-id="d4a10-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="d4a10-109">建立動畫變數時，必須指定其初始值。</span><span class="sxs-lookup"><span data-stu-id="d4a10-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="d4a10-110">之後，只能透過以動畫顯示動畫的腳本來變更其值。</span><span class="sxs-lookup"><span data-stu-id="d4a10-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="d4a10-111">當建立分鏡腳本時，會以參數的形式傳遞動畫變數，因此應用程式不應該釋出它們，直到它們表示的視覺特性不再需要產生動畫，通常是在相關聯的視覺物件終結時。</span><span class="sxs-lookup"><span data-stu-id="d4a10-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="d4a10-112">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="d4a10-112">Example Code</span></span>

-   [<span data-ttu-id="d4a10-113">製作色彩動畫</span><span class="sxs-lookup"><span data-stu-id="d4a10-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="d4a10-114">繪製 x 和 y 座標的動畫</span><span class="sxs-lookup"><span data-stu-id="d4a10-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="d4a10-115">製作色彩動畫</span><span class="sxs-lookup"><span data-stu-id="d4a10-115">Animating Colors</span></span>

<span data-ttu-id="d4a10-116">下列範例程式碼取自 Windows 動畫中的 MainWindow，範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [計時器驅動動畫](timer-driven-animation-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a10-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="d4a10-117">在此範例中，會使用 [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) 建立三個動畫變數來表示背景色彩。</span><span class="sxs-lookup"><span data-stu-id="d4a10-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="d4a10-118">程式碼也會使用 [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) 和 [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) 方法來控制動畫變數的值。</span><span class="sxs-lookup"><span data-stu-id="d4a10-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="d4a10-119">請注意 MainWindow 的下列定義。</span><span class="sxs-lookup"><span data-stu-id="d4a10-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="d4a10-120">繪製 x 和 y 座標的動畫</span><span class="sxs-lookup"><span data-stu-id="d4a10-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="d4a10-121">下列範例程式碼取自 Windows 動畫 [方格配置範例](/windows/desktop/UIAnimation/grid-layout-sample)中的縮圖 .cpp;請參閱 CMainWindow：： CreateAnimationVariables 方法。</span><span class="sxs-lookup"><span data-stu-id="d4a10-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="d4a10-122">系統會建立兩個動畫變數來代表每個物件的 X 和 Y 座標。</span><span class="sxs-lookup"><span data-stu-id="d4a10-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="d4a10-123">請注意下列來自微縮圖的定義。</span><span class="sxs-lookup"><span data-stu-id="d4a10-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="d4a10-124">動畫變數是浮點數，但其值也可以做為整數來提取。</span><span class="sxs-lookup"><span data-stu-id="d4a10-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="d4a10-125">根據預設，每個值會四捨五入為最接近的整數，但可以覆寫變數所使用的舍入模式。</span><span class="sxs-lookup"><span data-stu-id="d4a10-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="d4a10-126">下列範例程式碼會使用 [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) 方法來指定應該一律四捨五入的值。</span><span class="sxs-lookup"><span data-stu-id="d4a10-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="d4a10-127">上一個步驟</span><span class="sxs-lookup"><span data-stu-id="d4a10-127">Previous Step</span></span>

<span data-ttu-id="d4a10-128">開始此步驟之前，您應該已完成此步驟： [建立主要動畫物件](adding-animation-to-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="d4a10-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="d4a10-129">後續步驟</span><span class="sxs-lookup"><span data-stu-id="d4a10-129">Next Step</span></span>

<span data-ttu-id="d4a10-130">完成此步驟後，下一個步驟是： [更新動畫管理員並繪製畫面](introducing-windows-animation-manager.md)格。</span><span class="sxs-lookup"><span data-stu-id="d4a10-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4a10-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4a10-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a10-132">**IUIAnimationManager::CreateAnimationVariable**</span><span class="sxs-lookup"><span data-stu-id="d4a10-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="d4a10-133">**IUIAnimationVariable::SetLowerBound**</span><span class="sxs-lookup"><span data-stu-id="d4a10-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="d4a10-134">**IUIAnimationVariable::SetRoundingMode**</span><span class="sxs-lookup"><span data-stu-id="d4a10-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="d4a10-135">**IUIAnimationVariable::SetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="d4a10-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="d4a10-136">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="d4a10-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 