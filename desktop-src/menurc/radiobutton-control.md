---
title: 選項按鈕控制項
description: 定義選項按鈕控制項。
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- 選項按鈕控制項功能表和其他資源
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023475"
---
# <a name="radiobutton-control"></a>選項按鈕控制項

定義選項按鈕控制項。 控制項是一個小圓圈，其旁邊會顯示指定的文字，通常會顯示在右邊。 控制項會在使用者選取按鈕時，反白顯示圓形並將訊息傳送至其父視窗。 控制項會移除反白顯示，並在下一次選取按鈕時傳送訊息。

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

選項按鈕的樣式，可以是按鈕類別樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。

如果您未指定樣式，則預設樣式為 `BS_RADIOBUTTON | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **選項按鈕** 語句：

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[選項按鈕](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 