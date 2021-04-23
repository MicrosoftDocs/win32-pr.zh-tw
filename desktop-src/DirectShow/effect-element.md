---
description: 效果元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: 'effect 元素 (Gdipluseffects .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908656"
---
# <a name="effect-element"></a>effect 元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`effect`元素定義音訊或影片效果物件。 效果會套用至單一資料流程 (例如撰寫、追蹤或來源) 。

## <a name="attributes"></a>屬性

[**clsid**](clsid-attribute.md)、[**鎖定**](lock-attribute.md)、[**靜音**](mute-attribute.md)、[**啟動**](start-attribute.md)、[**停止**](stop-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid、使用者**](userid-attribute.md)[**名稱**](username-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
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

 

 




