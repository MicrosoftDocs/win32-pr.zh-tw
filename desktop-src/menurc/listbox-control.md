---
title: 'LISTBOX 控制項 (功能表和其他資源) '
description: 定義用於對話方塊或視窗的常用控制項。 控制項是包含字串清單的矩形， (例如可供使用者選取的檔案名) 。
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- LISTBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226346"
---
# <a name="listbox-control"></a>LISTBOX 控制項

定義用於對話方塊或視窗的常用控制項。 控制項是包含字串清單的矩形， (例如可供使用者選取的檔案名) 。

**LISTBOX** 語句（只能用在 [**DIALOGEX**](dialogex-resource.md)或 **WINDOW** 語句中）會定義控制項視窗的識別碼、維度和屬性。

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是清單方塊類別樣式和下列任何樣式的組合： **WS \_ BORDER** 和 **ws \_ VSCROLL**。

如果您未指定樣式，則預設樣式為 `LBS_NOTIFY | WS_BORDER` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

此範例會定義識別碼為101的清單方塊控制項：

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**組合**](combobox-control.md)
</dt> <dt>

[清單方塊](../controls/about-list-boxes.md)
</dt> </dl>

 

 