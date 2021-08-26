---
description: 此事件會通知 DirectoryList 控制項，表示使用者想要選取目前目錄的父系。 如需相關資訊，請參閱流覽對話方塊。
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99fb0731a06f30cf788e3565e0988bf5b20ebce7abec8be351f4d1fe9d2aab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086178"
---
# <a name="directorylistup-controlevent"></a>DirectoryListUp ControlEvent

此事件會通知 [DirectoryList 控制項](directorylist-control.md) ，表示使用者想要選取目前目錄的父系。 如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。

這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。 此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

如果目前的目錄是磁片磁碟機的根目錄，DirectoryListUp 事件會停用任何其他發行 DirectoryListUp 事件的控制項。

## <a name="published-by"></a>發佈者

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

在與 DirectoryList 相同的強制回應對話方塊上，使用 [ [按鈕](pushbutton-control.md) ] 控制項來觸發路徑中的逐步執行。

 

 



