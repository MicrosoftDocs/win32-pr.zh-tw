---
title: 讀取動畫變數值
description: 每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- 動畫變數 Windows 動畫、讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2cc164091be9ecca292e26ab1247ba18c61d89f11dad8fc2530a3e45ca7629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058165"
---
# <a name="read-the-animation-variable-values"></a>讀取動畫變數值

每次您的應用程式繪製時，都應該讀取代表要進行動畫之視覺特性的動畫變數目前的值。

## <a name="overview"></a>概觀

繪製框架時，應用程式可以使用 [**IUIAnimationVariable：： GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) 或 [**IUIAnimationVariable：： GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) 方法來要求任何會影響框架內視覺效果的動畫變數值。 您可以將動畫變數裁剪至值範圍 ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) 和 [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) ，並使用指定的舍入配置 ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) ，來要求其值四捨五入為整數。

應用程式可以使用 [**IUIAnimationVariable：： SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) 或 [**IUIAnimationVariable：： SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) 方法來註冊一個或多個變數變更處理常式，只在變數的值變更時才接收通知，而不是讀取每個框架的所有變數值， ([**IUIAnimationVariableChangeHandler：： OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) 或四捨五入值 ([**IUIAnimationVariableIntegerChangeHandler：： OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)) 。 若要識別傳遞給變數變更處理常式的變數，應用程式可以使用 [**IUIAnimationVariable：： SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) 方法，將標記套用至變數。 這些是 \* 由應用程式所解讀的物件 (IUnknown) 、整陣列。

## <a name="example-code"></a>範例程式碼

下列範例程式碼取自 Windows 動畫範例[方格](/windows/desktop/UIAnimation/grid-layout-sample)配置中的縮圖 .cpp;請參閱 CMainWindow：： Render 方法。 它會使用 [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) 方法將值讀取為浮點值。


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



下列範例程式碼取自 Windows 動畫範例[計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：:D rawBackground 方法。 它會使用 [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) 方法將值讀取為整數值。


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



## <a name="previous-step"></a>上一個步驟

開始此步驟之前，您應該已完成此步驟： [更新動畫管理員並繪製畫面](introducing-windows-animation-manager.md)格。

## <a name="next-step"></a>後續步驟

完成此步驟後，下一個步驟是： [建立分鏡腳本並加入轉換](updating---timer-driven-animation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable：： GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Windows動畫總覽](scenic-animation-api-overview.md)
</dt> </dl>

 

 