---
description: 此事件會通知 DirectoryList 控制項必須建立新資料夾;它會建立新的資料夾，並選取資料夾的 [名稱] 欄位以進行編輯。
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281835954c947e4bcaaf6e4e2019cbd422151e6cca39b83fa84a0abe0db010cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378898"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent

此事件會通知 [DirectoryList 控制項](directorylist-control.md) 必須建立新資料夾;它會建立新的資料夾，並選取資料夾的 [名稱] 欄位以進行編輯。 新資料夾的預設名稱可能會在 [UIText 資料表](uitext-table.md)中撰寫。 在索引鍵資料行中輸入 "NewFolder"。 在 [文字] 資料行中，輸入新資料夾的預設名稱值。 這個值必須是 [Filename](filename.md) 資料行資料類型的格式，並使用 SFN \| LFN 語法。 如果此值不存在於 UIText 資料表中或為無效值，則安裝程式會使用預設值 "Fldr \| New Folder"。 如需相關資訊，請參閱 [流覽對話方塊](browse-dialog.md)。

這個事件應該是由與訂閱此事件的控制項位於相同對話方塊的 [按鈕控制項](pushbutton-control.md) 所發行。 此事件應該在 [ControlEvent 資料表](controlevent-table.md)中撰寫。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

請注意，如果在新資料夾已存在時再次呼叫這個 ControlEvent，則不會建立第二個新的資料夾。 在此情況下，呼叫 DirectoryListNew 會選取現有的新資料夾名稱進行編輯。

## <a name="published-by"></a>發佈者

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

與 DirectoryList 相同的強制回應對話方塊中的 [按鈕](pushbutton-control.md) 控制項，可用來觸發新資料夾的建立。

 

 



