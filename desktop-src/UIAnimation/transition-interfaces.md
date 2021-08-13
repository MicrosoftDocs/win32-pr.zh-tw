---
title: 轉換介面
description: 本節包含支援轉換之 Windows 動畫管理員介面的參考規格。
ms.assetid: 581C853D-F213-4227-AC61-4ED2E5D4EF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5791de6e2ca148e42ef836c8bb9be2d9dc96304df00a856b1bc036e05fca3fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418598"
---
# <a name="transition-interfaces"></a>轉換介面

本節包含支援轉換之 Windows 動畫管理員介面的參考規格。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                     | 描述                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator)<br/>                                   | 定義用來建立自訂插即用的方法。<br/>                                                                                                                                                                                                             |
| [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2)<br/>                                 | 擴充 [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) 介面，此介面會定義用來建立自訂插即用的方法。 [**IUIAnimationInterpolator2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator2) 支援指定維度中的插補。 <br/>        |
| [**IUIAnimationPrimitiveInterpolation**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprimitiveinterpolation)<br/>               | 定義方法，此方法可讓自訂的插線以三個多項式曲線的形式提供轉換資訊給動畫管理員。<br/>                                                                                                        |
| [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition)<br/>                                       | 定義轉換，決定動畫變數隨著時間的變更。<br/>                                                                                                                                                                             |
| [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)<br/>                                     | 擴充定義轉換的 [**IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition) 介面。 [**IUIAnimationTransition2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransition2)轉換可決定動畫變數在給定維度中的時間如何變更。<br/> |
| [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)<br/>                         | 定義用來建立自訂 interpolators 轉換的方法。<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionFactory2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory2)<br/>                       | 定義用來建立自訂 interpolators 轉換的方法。<br/>                                                                                                                                                                                            |
| [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)<br/>                         | 定義標準轉換的程式庫。 <br/>                                                                                                                                                                                                                     |
| [**IUIAnimationTransitionLibrary2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary2)<br/>                       | 定義指定維度的標準轉換程式庫。<br/>                                                                                                                                                                                            |
| [**IUIAnimationVariable**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable)<br/>                                           | 定義動畫變數，此變數表示可以動畫顯示的視覺元素。<br/>                                                                                                                                                                          |
| [**IUIAnimationVariable2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariable2)<br/>                                         | 定義動畫變數，此變數表示可以在多個維度中進行動畫的視覺元素。<br/>                                                                                                                                                   |
| [**IUIAnimationVariableChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler)<br/>                 | 定義處理動畫變數更新相關事件的方法。<br/>                                                                                                                                                                                     |
| [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2)<br/>               | 定義處理動畫變數更新事件的方法。 [**IUIAnimationVariableChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablechangehandler2) 會處理在指定維度中發生的事件。<br/>                                                            |
| [**IUIAnimationVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler)<br/>   | 定義處理動畫變數更新事件的方法。<br/>                                                                                                                                                                                                 |
| [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2)<br/> | 定義處理動畫變數更新事件的方法。 [**IUIAnimationVariableIntegerChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariableintegerchangehandler2) 會處理在指定維度中發生的事件。<br/>                                              |
| [**IUIAnimationVariableCurveChangeHandler2**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationvariablecurvechangehandler2)<br/>     | 定義處理動畫曲線更新事件的方法。 <br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[介面](windows-animation-reference.md)
</dt> </dl>

 

 





