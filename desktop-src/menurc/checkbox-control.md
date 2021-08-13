---
title: 'CHECKBOX 控制項 (資源編譯器) '
description: 定義核取方塊控制項。
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- CHECKBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461328"
---
# <a name="checkbox-control"></a>CHECKBOX 控制項

定義核取方塊控制項。 控制項是一個小型矩形 (核取方塊) ，其旁邊會顯示指定的文字 (通常是右邊) 。 當使用者選取控制項時，控制項會反白顯示矩形，並將訊息傳送至其父視窗。

**CHECKBOX** 語句（只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用）會定義控制項的文字、識別碼、維度和屬性。

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

要在控制項右邊顯示的文字。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是按鈕類別樣式 **BS \_ 核取方塊** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。

如果您未指定樣式，則預設樣式為 `BS_CHECKBOX | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

這個範例會定義標記為斜體的核取方塊控制項：

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[核取方塊](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 