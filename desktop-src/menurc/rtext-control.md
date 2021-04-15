---
title: RTEXT 控制項
description: 定義靠右對齊的文字控制項。
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- RTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463133"
---
# <a name="rtext-control"></a>RTEXT 控制項

定義靠右對齊的文字控制項。 控制項是一個簡單的矩形，可在矩形中顯示指定的文字（靠右對齊）。 文字會在顯示之前格式化。 延伸超過行尾的單字會自動換行到下一行的開頭。 長度超過控制項寬度的文字會被截斷。

**RTEXT** 語句只能用在 [**DIALOGEX**](dialogex-resource.md)語句中，可定義控制項的文字、識別碼、維度和屬性。

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

文字控制項的樣式，可以是下列各項的任意組合： **WS \_ TABSTOP** 和 **WS \_ GROUP**。

如果您未指定樣式，則預設樣式為 `SS_RIGHT | WS_GROUP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **RTEXT** 語句：

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[編輯控制項](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 