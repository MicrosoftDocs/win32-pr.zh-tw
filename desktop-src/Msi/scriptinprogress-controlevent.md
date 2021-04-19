---
description: 當編譯安裝的執行腳本時，安裝程式會使用此事件來顯示資訊字串。
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986944"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent

當編譯安裝的執行腳本時，安裝程式會使用此事件來顯示資訊字串。 訂閱此 ControlEvent 的 [文字控制項](text-control.md) 可以在對話方塊中顯示資訊字串。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 可由使用者介面在 [*基本 ui*](b-gly.md)、 [*縮減 UI*](r-gly.md)或 [*完整 ui*](f-gly.md) 層級上執行。 如需 UI 層級的詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

訂閱 ScriptInProgress 的 [文字控制項](text-control.md) 將會顯示 [UIText 資料表](uitext-table.md)中指定的文字字串。

## <a name="typical-use"></a>一般用法

在編譯執行腳本時，安裝程式會顯示 ProgressBar，指出腳本執行開始之前的剩餘時間。 封裝作者在這段時間可以顯示初步訊息來說明 ProgressBar。 若要顯示初步訊息，請在與 ProgressBar 相同的非強制回應對話方塊中包含 [文字控制項](text-control.md) 。 指定此文字控制項透過 [EventMapping 資料表](eventmapping-table.md)訂閱 ScriptInProgress ControlEvent。 在 [UIText 資料表](uitext-table.md) 中包含索引鍵欄位中指定 ScriptInProgress 的專案。 在 UIText 資料表的文字欄位中，將初稿訊息指定為文字字串。 然後，在腳本編譯期間，安裝程式會在文字控制項中顯示此字串。 腳本編譯完成時，顯示的文字就會消失。

訂閱 ScriptInProgress ControlEvent 的相同文字控制項也可以訂閱 [TimeRemaining ControlEvent](timeremaining-controlevent.md)。 在此情況下，當初稿 ScriptInProgress 字串的文字消失時，就會以「剩餘時間： xx 分鐘」字串取代。

 

 



