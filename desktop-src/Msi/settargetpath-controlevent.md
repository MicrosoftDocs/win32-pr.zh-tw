---
description: SetTargetPath 事件會通知安裝程式檢查並設定選取的路徑。 如果路徑無效而無法寫入，則安裝程式會封鎖與控制項相關聯的其他工作。
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193677"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent

SetTargetPath 事件會通知安裝程式檢查並設定選取的路徑。 如果路徑無效而無法寫入，則安裝程式會封鎖與控制項相關聯的其他工作。

這個事件可以透過 [按鈕控制項](pushbutton-control.md)或 [SelectionTree 控制項](selectiontree-control.md)來發行。 此事件應該撰寫至 [ControlEvent 資料表](controlevent-table.md)。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

此 ControlEvent 是由安裝程式所發佈。

## <a name="argument"></a>引數

包含路徑之屬性的名稱。 如果屬性是 indirected，則屬性名稱會以方括弧括住。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

流覽對話方塊上的 [按鈕](pushbutton-control.md) 控制項會系結至 [ControlEvent](controlevent-table.md) 資料表中的這個事件，以檢查選取的路徑，然後再返回選取專案對話方塊。

## <a name="remarks"></a>備註

如果已為目前使用者或其他使用者安裝使用這些路徑的元件，請不要嘗試設定目標路徑。 在發佈 SetTargetPath ControlEvent 之前，請先檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含該元件的產品。

 

 



