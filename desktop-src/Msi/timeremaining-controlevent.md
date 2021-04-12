---
description: 安裝程式會使用 TimeRemaining 事件來發佈目前進度順序的大約剩餘時間（以秒為單位）。
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027400"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent

安裝程式會使用 TimeRemaining 事件來發佈目前進度順序的大約剩餘時間（以秒為單位）。 訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示剩餘的時間。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md) 訂閱此事件，並使用 [TimeRemaining 屬性](timeremaining-control-attribute.md) 來顯示剩餘的時間。

訂閱 TimeRemaining ControlEvent 的相同文字控制項也可以訂閱 [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)。 在此情況下，會以初步的 ScriptInProgress 訊息字串取代，並以「剩餘時間： xx 分鐘」字串取代。

 

 



