---
title: 主題. openView
description: OpenView 方法會在新視窗中開啟一個 VIEW。
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- 主題. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001824"
---
# <a name="themeopenview"></a>主題. openView

**OpenView** 方法會在新視窗中開啟一個 **VIEW** 。

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*視圖*
</dt> <dd>

**字串**，指定要開啟之 **視圖** 的 **識別碼**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="examples"></a>範例


```JScript
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

[**CloseView**](theme-closeview.md)
</dt> <dt>

[**OpenViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





