---
title: AUTOCHECKBOX 控制項
description: 定義自動核取方塊控制項。
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- AUTOCHECKBOX 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681922"
---
# <a name="autocheckbox-control"></a>AUTOCHECKBOX 控制項

定義自動核取方塊控制項。 控制項是一個小型矩形 (核取方塊) ，其旁邊會顯示指定的文字 (通常是右邊) 。 當使用者選擇控制項時，控制項會反白顯示矩形，並將訊息傳送至其父視窗。

**AUTOCHECKBOX** 語句只能用在 [**DIALOG**](dialog-resource.md)或 [**DIALOGEX**](dialogex-resource.md)語句的主體中。

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項的樣式。 這個值可以是 button 類別樣式 **BS \_ AUTOCHECKBOX** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。

如果您未指定樣式，則預設樣式為 `BS_AUTOCHECKBOX | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[按鈕樣式](../controls/button-styles.md)
</dt> <dt>

[**相應**](checkbox-control.md)
</dt> <dt>

[**控制**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 