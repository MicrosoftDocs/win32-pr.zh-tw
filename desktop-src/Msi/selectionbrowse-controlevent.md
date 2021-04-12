---
description: SelectionTree 控制項會使用 SelectionBrowse 事件來產生流覽對話方塊，讓您可以修改反白專案的路徑。
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321067"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent

[SelectionTree 控制項](selectiontree-control.md)會使用 SelectionBrowse 事件來產生 **流覽** 對話方塊，讓您可以修改反白專案的路徑。

這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。 此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

如果已選取已安裝、無法設定或未選取要進行本機安裝的功能，則任何發佈 SelectionBrowse 事件的控制項都會變成停用狀態。 若要設定，此功能必須在功能資料表的 [目錄] 欄位中輸入[公用屬性](public-properties.md) \_ 。 [](feature-table.md)

## <a name="published-by"></a>發佈者

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>引數

要產生之對話方塊的名稱。

## <a name="action-on-subscribers"></a>訂閱者的動作

無。

## <a name="typical-use"></a>一般用法

與 SelectionTree 相同的強制回應對話方塊中的 [按鈕](pushbutton-control.md) 控制項，會使用此事件來觸發 [ **流覽** ] 對話方塊。

 

 



