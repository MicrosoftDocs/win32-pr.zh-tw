---
description: 線性元素會在特定時間定義 param 專案的值，相對於包含 param 專案的轉換或效果的開頭。
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: '線性元素 (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999100"
---
# <a name="linear-element"></a>線性元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

線性元素會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含 **param** 專案的轉換或效果的開頭。 `linear`元素會讓參數從先前的值轉換成新值。 若要立即跳至新的值，請使用 [**at**](at-element.md) 元素。

## <a name="attributes"></a>屬性

[**時間**](time-attribute.md)、 [**值**](value-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



|          |                                |
|----------|--------------------------------|
| 父代   | [**參數**](param-element.md) |
| Children | 無                           |



 

## <a name="examples"></a>範例


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Camerauicontrol。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 




