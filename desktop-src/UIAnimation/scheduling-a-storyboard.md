---
title: 排程分鏡腳本
description: 建立分鏡腳本之後，動畫管理員會進行排程。
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- 分鏡腳本 Windows 動畫、排程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008168"
---
# <a name="schedule-a-storyboard"></a>排程分鏡腳本

建立分鏡腳本之後，動畫管理員會進行排程。

## <a name="overview"></a>概觀

根據預設，每個分鏡腳本會在排程時立即啟動。 這表示當腳本開始以動畫顯示一或多個變數時，它可能會中斷任何其他以動畫顯示這些相同變數的分鏡腳本。 不過，應用程式可以藉由判斷分鏡腳本之間的相對優先順序來指定其他行為。

在排程腳本之後，就無法再變更它。 不過，在從排程中移除分鏡腳本之後，就可以將它排程為重新播放。 當重複使用分鏡腳本時，開發人員應該要特別小心，因為這應該只有在沒有機會讓相同的分鏡腳本因為使用者動作已在排程中播放或排入佇列時，才需要將其排入佇列。

## <a name="example-code"></a>範例程式碼

下列範例程式碼取自 Windows 動畫中的 MainWindow，範例[應用程式驅動的動畫](application-driven-animation-sample.md)和[計時器驅動動畫](timer-driven-animation-sample.md)。 它會使用 [**IUIAnimationStoryboard：： schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) 方法來排程分鏡腳本。 這個方法需要目前的時間做為參數。


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



## <a name="previous-step"></a>上一個步驟

開始此步驟之前，您應該已完成此步驟： [建立分鏡腳本並加入轉換](updating---timer-driven-animation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationStoryboard：： Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer：： GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[分鏡腳本總覽](storyboard-construction.md)
</dt> </dl>

 

 




