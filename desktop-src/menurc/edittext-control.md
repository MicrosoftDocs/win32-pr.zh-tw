---
title: EDITTEXT 控制項
description: 定義屬於編輯類別的編輯控制項。
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- EDITTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b287f01b89aaa3e378309e8f98f777acc475bcca962557305021aaf471926ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847388"
---
# <a name="edittext-control"></a>EDITTEXT 控制項

定義屬於編輯類別的編輯控制項。 它會建立一個矩形區域，讓使用者可以在其中輸入和編輯文字。 當使用者按一下滑鼠時，控制項會顯示資料指標。 使用者接著可以使用鍵盤來輸入文字或編輯現有文字。 編輯索引鍵包括倒退鍵和刪除鍵。 使用者也可以使用滑鼠來選取要刪除的字元，或選取要插入新字元的位置。

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是編輯類別樣式和下列樣式的組合： **WS \_ TABSTOP**、 **ws \_ GROUP**、 **ws \_ VSCROLL**、 **ws \_ HSCROLL** 和 **ws \_ DISABLED**。

如果您未指定樣式，則預設樣式為 `ES_LEFT | WS_BORDER | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **EDITTEXT** 語句：

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[編輯控制項](../controls/about-edit-controls.md)
</dt> </dl>

 

 