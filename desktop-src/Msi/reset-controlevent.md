---
description: 會重設此對話方塊。 換句話說，會呼叫對話方塊上的所有控制項，以復原它們所執行的屬性變更。 此事件會將所有屬性值重設為建立對話方塊時的值。
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: 重設 ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987638"
---
# <a name="reset-controlevent"></a>重設 ControlEvent

會重設此對話方塊。 換句話說，會呼叫對話方塊上的所有控制項，以復原它們所執行的屬性變更。 此事件會將所有屬性值重設為建立對話方塊時的值。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

在某些情況下，這種情況應該很少發生，此 ControlEvent 並不會正確處理。 如果相同對話方塊上有兩個或多個控制項連結到相同的屬性，且至少其中一個控制項開始有其他屬性，則這個屬性值有時會重設為其第二個值。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

無。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

強制回應對話方塊上的 [按鈕](pushbutton-control.md) 控制項可用來重設對話方塊上的所有值，以及取消頁面上的所有變更。

 

 



