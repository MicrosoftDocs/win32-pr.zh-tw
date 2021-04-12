---
description: 預覽效果和轉換
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: 預覽效果和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109553"
---
# <a name="previewing-effects-and-transitions"></a>預覽效果和轉換

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

某些效果和轉換需要相對較長的時間才能呈現。 在預覽期間，這可能會導致影片不穩定或與音訊同步。 您可以停用效果或轉換來提高預覽速度：

-   若要停用所有效果，請呼叫 [**IAMTimeline：： EnableEffects**](iamtimeline-enableeffects.md)。
-   若要停用所有轉換，請呼叫 [**IAMTimeline：： EnableTransitions**](iamtimeline-enabletransitions.md)。
-   若要停用特定轉換，請呼叫 [**IAMTimelineTrans：： SetCutsOnly**](iamtimelinetrans-setcutsonly.md)。

當效果停用時，不會在預覽期間轉譯。 當轉換停用時，它會轉譯為跳躍點剪下。 Segue 之間仍會進行追蹤，但不會轉譯視覺效果。

如果無法轉譯效果或轉換，轉譯引擎會替代預設效果或轉換。 呼叫 [**IAMTimeline：： SetDefaultEffect**](iamtimeline-setdefaulteffect.md) 方法來設定預設效果，並呼叫 [**IAMTimeline：： SetDefaultTransition**](iamtimeline-setdefaulttransition.md) 方法來設定預設轉換。 如果您未指定預設值，或您指定的也會造成錯誤，DES 會使用它自己的預設值。

> [!Note]  
> 您也可以藉由增加框架緩衝量來改善預覽品質。 請參閱 [**IAMTimelineGroup：： SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用效果和轉換](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



