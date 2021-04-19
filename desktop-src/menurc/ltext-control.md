---
title: LTEXT 控制項
description: 定義靠左對齊的文字控制項。
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- LTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969901"
---
# <a name="ltext-control"></a>LTEXT 控制項

定義靠左對齊的文字控制項。 控制項是一個簡單的矩形，可顯示矩形中靠左對齊的指定文字。 文字會在顯示之前格式化。 延伸超過行尾的單字會自動換行到下一行的開頭。 長度超過控制項寬度的文字會被截斷。

**LTEXT** 語句只能用在 [**DIALOGEX**](dialogex-resource.md)語句中，可定義控制項的文字、識別碼、維度和屬性。

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是 **BS \_ 選項按鈕** 樣式和下列樣式的任意組合： **SS \_ LEFT**、 **WS \_ TABSTOP** 和 **WS \_ GROUP**。

如果您未指定樣式，則預設樣式為 `SS_LEFT | WS_GROUP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

這個範例會定義一個靠左對齊的文字控制項，其標示為 Filename：

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[編輯控制項](../controls/about-edit-controls.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 