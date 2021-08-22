---
description: 安裝程式會使用 SetProgress 事件來發佈有關安裝進度的資訊。
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625078"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent

安裝程式會使用 SetProgress 事件來發佈有關安裝進度的資訊。 [ProgressBar 控制項](progressbar-control.md)或[佈告欄控制項](billboard-control.md)應藉由命名其進度指出的動作，來透過[EventMapping 資料表](eventmapping-table.md)訂閱事件。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

非強制回應對話方塊上的 [ProgressBar](progressbar-control.md) 控制項會使用 [進度](progress-control-attribute.md) 屬性來接收進度資訊，以訂閱此事件。

 

 



