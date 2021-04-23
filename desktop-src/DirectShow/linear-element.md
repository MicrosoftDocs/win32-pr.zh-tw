---
description: 線性元素會在特定時間定義 param 專案的值，相對於包含 param 專案的轉換或效果的開頭。
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: '線性元素 (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910086"
---
# <a name="linear-element"></a>線性元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

線性元素會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含 **param** 專案的轉換或效果的開頭。 `linear`元素會讓參數從先前的值轉換成新值。 若要立即跳至新的值，請使用 [**at**](at-element.md) 元素。

## <a name="attributes"></a>屬性

[**時間**](time-attribute.md)、 [**值**](value-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
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

 

 




