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
# <a name="create-animation-variables"></a>建立動畫變數

應用程式必須針對每個要使用 Windows 動畫製作動畫的視覺特性建立動畫變數。

## <a name="overview"></a>概觀

動畫變數是使用動畫管理員建立的，而且只要需要，應用程式應保留每個變數的參考。 您的應用程式通常會在繪製動畫的視覺物件時，同時建立每個動畫變數。

建立動畫變數時，必須指定其初始值。 之後，只能透過以動畫顯示動畫的腳本來變更其值。

當建立分鏡腳本時，會以參數的形式傳遞動畫變數，因此應用程式不應該釋出它們，直到它們表示的視覺特性不再需要產生動畫，通常是在相關聯的視覺物件終結時。

## <a name="example-code"></a>範例程式碼

-   [製作色彩動畫](#animating-colors)
-   [繪製 x 和 y 座標的動畫](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>製作色彩動畫

下列範例程式碼取自 Windows 動畫中的 MainWindow，範例 [應用程式驅動的動畫](application-driven-animation-sample.md) 和 [計時器驅動動畫](timer-driven-animation-sample.md)。 在此範例中，會使用 [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) 建立三個動畫變數來表示背景色彩。 程式碼也會使用 [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) 和 [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) 方法來控制動畫變數的值。


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



請注意 MainWindow 的下列定義。


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



### <a name="animating-x-and-y-coordinates"></a>繪製 x 和 y 座標的動畫

下列範例程式碼取自 Windows 動畫 [方格配置範例](/windows/desktop/UIAnimation/grid-layout-sample)中的縮圖 .cpp;請參閱 CMainWindow：： CreateAnimationVariables 方法。 系統會建立兩個動畫變數來代表每個物件的 X 和 Y 座標。


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



請注意下列來自微縮圖的定義。


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



動畫變數是浮點數，但其值也可以做為整數來提取。 根據預設，每個值會四捨五入為最接近的整數，但可以覆寫變數所使用的舍入模式。 下列範例程式碼會使用 [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) 方法來指定應該一律四捨五入的值。


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



## <a name="previous-step"></a>上一個步驟

開始此步驟之前，您應該已完成此步驟： [建立主要動畫物件](adding-animation-to-an-application.md)。

## <a name="next-step"></a>後續步驟

完成此步驟後，下一個步驟是： [更新動畫管理員並繪製畫面](introducing-windows-animation-manager.md)格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**IUIAnimationVariable::SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**IUIAnimationVariable::SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**IUIAnimationVariable::SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Windows 動畫總覽](scenic-animation-api-overview.md)
</dt> </dl>

 

 