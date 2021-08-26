---
title: PUSHBOX 控制項
description: 定義與按鍵相同的推播方塊控制項，不同之處在于它不會顯示按鈕臉部或框架;只會顯示文字。
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- PUSHBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06135aad813141e15bede8364a71e8fbc3016c7cb79afe0085bb6bc7bbcb2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952368"
---
# <a name="pushbox-control"></a>PUSHBOX 控制項

定義與 [**按鍵**](pushbutton-control.md)相同的推播方塊控制項，不同之處在于它不會顯示按鈕臉部或框架;只會顯示文字。

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

Pushbox 的樣式，可以是 **BS \_ pushbox** 樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。

如果您未指定樣式，則預設樣式為 `BS_PUSHBOX | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[推播按鈕](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**按鈕**](pushbutton-control.md)
</dt> </dl>

 

 




