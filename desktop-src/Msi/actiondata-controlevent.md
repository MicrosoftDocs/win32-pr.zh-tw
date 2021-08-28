---
description: 安裝程式會使用此事件來發佈最新動作的資料。 訂閱此 ControlEvent 的文字控制項可以在對話方塊上顯示資料。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c280bbd2c0a184ec281e4401037687893942b4c344824b20a59c410b59fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105478"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent

安裝程式會使用此事件來發佈最新動作的資料。 訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊上顯示資料。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

當新動作開始時，系統會隱藏訂閱者，並在新的動作資料從安裝程式抵達時顯示。

## <a name="typical-use"></a>一般用法

非強制回應對話方塊上的 [文字控制項](text-control.md) 會透過 [EventMapping 資料表](eventmapping-table.md)訂閱此事件。 此 [文字控制項屬性](text-control-attribute.md) 會列在此資料表的 [屬性] 欄位中，以接收目前的動作資料。 通常用來顯示檔案複製期間複製的檔案名。

 

 



