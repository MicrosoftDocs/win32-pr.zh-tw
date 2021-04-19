---
description: SetProperty 事件的語法與其他事件名稱的語法不同，它會以方括弧括住屬性（ \[ property \_ name） \] 。
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984598"
---
# <a name="setproperty-controlevent"></a>SetProperty ControlEvent

SetProperty 事件的語法與其他事件名稱的語法不同，它會以方括弧括住屬性（ \[ property \_ name） \] 。 引數是屬性的新值。 若要取消設定屬性，引數必須是 {} 。 這是必要的，因為引數是資料表中的主鍵，因此不能是 null。 引數將使用 FormatText 方法進行格式化，因此引數可以包含 FormatText 方法可以處理的任何運算式。 屬性值會在 ControlEvent 時進行評估。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)、 [CheckBox 控制項](checkbox-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

屬性的新值。 {} 若為 null。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

連結至這個事件之對話方塊上的 [按鈕控制項，](pushbutton-control.md) 以便在推送按鈕時變更屬性。

 

 



