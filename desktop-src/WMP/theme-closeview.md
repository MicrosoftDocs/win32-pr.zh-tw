---
title: CloseView
description: CloseView 方法會關閉開啟的視圖。
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- CloseView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998785"
---
# <a name="themecloseview"></a>CloseView

**CloseView** 方法會關閉開啟的 **視圖**。

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

**字串**，指定要關閉之 **視圖** 的 **識別碼**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="examples"></a>範例


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> <dt>

[**主題. openView**](theme-openview.md)
</dt> </dl>

 

 





