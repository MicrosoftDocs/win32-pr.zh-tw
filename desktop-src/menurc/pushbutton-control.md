---
title: '將控制項按鈕 (功能表和其他資源) '
description: 定義按鈕控制項。 控制項是包含指定文字的圓角矩形。 文字是在控制項的中央。 每當使用者選擇控制項時，控制項會將訊息傳送到其父系。
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- 按鈕控制功能表和其他資源
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776998"
---
# <a name="pushbutton-control"></a>按鈕控制項

定義按鈕控制項。 控制項是包含指定文字的圓角矩形。 文字是在控制項的中央。 每當使用者選擇控制項時，控制項會將訊息傳送到其父系。

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

按鍵的樣式，可以是 **BS \_ 按鈕** 樣式和下列樣式的組合： **WS \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。

如果您未指定樣式，則預設樣式為 `BS_PUSHBUTTON | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **按鈕** 語句：

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[推播按鈕](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 