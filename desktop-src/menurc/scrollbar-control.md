---
title: 捲軸控制項
description: 定義捲軸控制項。
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- 捲軸控制項功能表和其他資源
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733436"
---
# <a name="scrollbar-control"></a>捲軸控制項

定義捲軸控制項。 控制項是包含捲動方塊的矩形，而且兩端都有方向箭號。 每當使用者按一下控制項中的滑鼠時，捲軸控制項就會將通知訊息傳送到其父系。 父代負責更新捲動方塊的位置。 捲軸控制項可放置在視窗中的任何位置，並在需要時用來提供滾動輸入。

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

下列樣式的零或組合： **ws \_ TABSTOP**、 **ws \_ GROUP** 和 **WS \_ 已停用**。

除了這些樣式之外， *style* 參數可以包含捲軸類別樣式的 (或無) 的組合。

如果您未指定樣式，則預設樣式為 **SBS \_ HORZ**。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。 請注意，您不能指定這個控制項的文字。

## <a name="examples"></a>範例

下列範例示範如何使用 **捲軸** 語句：

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[捲軸](../controls/about-scroll-bars.md)
</dt> </dl>

 

 