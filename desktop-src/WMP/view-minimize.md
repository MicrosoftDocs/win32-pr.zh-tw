---
title: VIEW. 最小化
description: 最小化方法會將視圖降至最低。
ms.assetid: 97c257fa-aa4f-4e6f-bc49-fa54db63b59b
keywords:
- VIEW. Windows Media Player 的最小化
topic_type:
- apiref
api_name:
- VIEW.minimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0351ad27e18750832151e8820dec8594319024791850f1ab92764e175d9582b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332960"
---
# <a name="viewminimize"></a>VIEW. 最小化

**最小化** 方法會將 **視圖** 降至最低。

``` syntax
        elementID.minimize()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.minimize()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**視圖。最大化**](view-maximize.md)
</dt> </dl>

 

 





