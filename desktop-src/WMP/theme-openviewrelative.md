---
title: OpenViewRelative
description: OpenViewRelative 方法會在相對於面板左上角的指定初始位置，在新視窗中開啟一個 VIEW。
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- OpenViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999236"
---
# <a name="themeopenviewrelative"></a>OpenViewRelative

**OpenViewRelative** 方法會在相對於面板左上角的指定初始位置，在新視窗中開啟一個 **VIEW** 。

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*視圖*
</dt> <dd>

**字串**，指定要開啟之 **視圖** 的 **識別碼**。

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*離開*
</dt> <dd>

**數位** (**long**) 指定外觀左邊框線的初始距離（以圖元為單位）  。 負數值表示外觀框線左邊的初始位置。

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*返回頁首*
</dt> <dd>

**數位** (**Long**) 指定 **視圖** 的上框線相對於面板上框線的初始位置。 負數值表示外觀框線上方的初始位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

第一次呼叫這個方法時，會使用針對 **view** 指定的位置，之後使用者可以將 **視圖** 拖曳至另一個位置。 儲存新的位置，並在後續的呼叫中使用最新的位置。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> <dt>

[**CloseView**](theme-closeview.md)
</dt> <dt>

[**主題. openView**](theme-openview.md)
</dt> </dl>

 

 





