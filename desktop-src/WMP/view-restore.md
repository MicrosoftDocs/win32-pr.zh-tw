---
title: VIEW. restore
description: 還原方法會還原此視圖。
ms.assetid: 8005c14e-771b-4f20-8039-fc09869dc726
keywords:
- VIEW. restore Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db92fc5e796acc55fe9c4faf93417d648652415e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001585"
---
# <a name="viewrestore"></a>VIEW. restore

**還原** 方法會還原此 **視圖**。

``` syntax
        elementID.restore()
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
        onclick="jscript:View1.restore()">
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
</dt> </dl>

 

 





