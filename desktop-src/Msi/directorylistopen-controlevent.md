---
description: 此事件會選取並反白顯示 DirectoryList 控制項中使用者已選擇要開啟的目錄。 如需相關資訊，請參閱流覽對話方塊。
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1453ffd42e0763ec747f02f7030818eaba3d533e5dfcca4570c13596efdcb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947322"
---
# <a name="directorylistopen-controlevent"></a>DirectoryListOpen ControlEvent

此事件會選取並反白顯示 [DirectoryList 控制項](directorylist-control.md) 中使用者已選擇要開啟的目錄。 如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。

這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。 此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

如果未在 [DirectoryList 控制項](directorylist-control.md)中選取任何目錄，DirectoryListOpen 事件就會停用任何其他發行 DirectoryListOpen 事件的控制項。

## <a name="published-by"></a>發佈者

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會對訂閱者執行任何動作。

## <a name="typical-use"></a>一般用法

在相同的強制回應對話方塊上，使用 DirectoryList 的 [按鈕](pushbutton-control.md) 控制項，可用來觸發路徑中的逐步執行。

 

 



