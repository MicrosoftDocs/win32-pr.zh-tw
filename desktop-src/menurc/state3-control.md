---
title: STATE3 控制項
description: 定義三個狀態的核取方塊控制項。 控制項與核取方塊相同，不同之處在于它有三個已核取、未選取和停用的狀態 (灰色) 。
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- STATE3 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678287"
---
# <a name="state3-control"></a>STATE3 控制項

定義三個狀態的核取方塊控制項。 控制項與 [**核取方塊**](checkbox-control.md)相同，不同之處在于它有三種狀態： [已選取]、[未選取] 和 [已停用] (灰色) 。

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

要在控制項右邊顯示的文字。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是 button 類別樣式 **BS \_ 3STATE** 和 **ws \_ TABSTOP** 和 **ws \_ GROUP** 樣式的組合。

如果您未指定樣式，則預設樣式為 `BS_3STATE | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[核取方塊](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**相應**](checkbox-control.md)
</dt> <dt>

[**控制**](control-control.md)
</dt> </dl>

 

 




