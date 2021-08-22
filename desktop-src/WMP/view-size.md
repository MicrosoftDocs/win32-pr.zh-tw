---
title: VIEW. size
description: 大小方法會在指定的邊緣上調整視圖的大小。
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VIEW. size Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0d9bd583b280f39bee38f0e109e6bb2bba6ce08ec0e7cea4c082b4a6db55739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615308"
---
# <a name="viewsize"></a>VIEW. size

大小方法會在指定的邊緣上調整 **視圖** 的 **大小**。

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*處理*
</dt> <dd>

字串，指定調整大小時要移動的邊緣或角落。 此字串必須有下列八個值的其中一個。



| Edge   | 邊角      |
|--------|-------------|
| top    | 右上    |
| 向右  | bottomright |
| 下 | bottomleft  |
| left   | 下拉式功能表     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

通常會從 **onmousedown** 處理常式內呼叫這個方法。 當滑鼠拖曳時，它會負責調整大小，並在放開滑鼠按鍵時停止調整大小。 如果 **視圖** 的大小受到限制，您就無法拖曳滑鼠來將 **視圖** 的大小調整到超出限制的範圍。

## <a name="examples"></a>範例


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
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

 

 





