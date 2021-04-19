---
description: 效果元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: 'effect 元素 (Gdipluseffects .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991187"
---
# <a name="effect-element"></a>effect 元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`effect`元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。

## <a name="attributes"></a>屬性

[**clsid**](clsid-attribute.md)、[**鎖定**](lock-attribute.md)、[**靜音**](mute-attribute.md)、[**啟動**](start-attribute.md)、[**停止**](stop-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid、使用者**](userid-attribute.md)[**名稱**](username-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| 父代   | [**複合**](composite-element.md)、 [**群組**](group-element.md)、 [**剪輯**](clip-element.md)、 [**追蹤**](track-element.md) |
| Children | [**參數**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>備註

**Clsid** 屬性會指定建立效果的子物件。

## <a name="examples"></a>範例


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Gdipluseffects。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 




