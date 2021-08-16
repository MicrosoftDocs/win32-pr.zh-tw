---
title: AUTO3STATE 控制項
description: 會定義三個自動狀態的核取方塊。
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- AUTO3STATE 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318d43f0b6d8a16d6e76ae3d12f934e41e265197690a955cfe148dd71176f440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735210"
---
# <a name="auto3state-control"></a>AUTO3STATE 控制項

會定義三個自動狀態的核取方塊。 控制項是一個開啟方塊，其中指定的文字位於方塊右邊。 選擇時，方塊會自動在三個狀態之間前進：已核取、未選取和停用的 (灰色) 。 每當使用者選擇控制項時，控制項會將訊息傳送到其父系。

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項的樣式，可以是 **BS \_ AUTO3STATE** 樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。

如果您未指定樣式，則預設樣式為 `BS_AUTO3STATE | WS_TABSTOP` 。

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
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[視窗樣式](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 