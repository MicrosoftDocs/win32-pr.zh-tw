---
description: 安裝程式會使用此事件來發佈目前動作的名稱。 訂閱此 ControlEvent 的文字控制項可以在對話方塊上顯示名稱。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a216cb30dbcaa0be9972f12f7a83c8e45e5bb5686d93ce210bf96087aa3c4552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927378"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent

安裝程式會使用此事件來發佈目前動作的名稱。 訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示名稱。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

當新的進度資料從安裝程式抵達時，會顯示訂閱者。

## <a name="typical-use"></a>一般用法

非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。 [文字控制項屬性](text-control-attribute.md)應該列在此資料表的 [屬性] 欄位中，以接收目前動作的名稱。

 

 



