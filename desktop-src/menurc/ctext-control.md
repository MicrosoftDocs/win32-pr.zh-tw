---
title: CTEXT 控制項
description: 定義中央文字控制項。
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- CTEXT 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092688"
---
# <a name="ctext-control"></a>CTEXT 控制項

定義中央文字控制項。 控制項是一個簡單的矩形，可顯示以矩形為中心的指定文字。 文字會在顯示之前格式化。 延伸超過行尾的單字會自動換行到下一行的開頭。 長度超過控制項寬度的文字會被截斷。

[**LTEXT**](ltext-control.md)語句只能用在 rep 語句中，可定義控制項的文字、識別碼、維度和屬性。

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

要置於控制項矩形區域中的文字。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是下列樣式的任意組合： **SS \_ CENTER**、 **WS \_ TABSTOP** 和 **WS \_ GROUP**。

如果您未指定樣式，則預設樣式為 `SS_CENTER | WS_GROUP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

此範例會定義標示為 Filename 的中央文字控制項：

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control-control.md)
</dt> <dt>

[編輯控制項](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 