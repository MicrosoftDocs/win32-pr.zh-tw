---
description: 轉換元素會定義轉換物件。 轉換是兩個輸入轉換，會導致從某個資料流程 (例如複合或追蹤) 轉換為另一個資料流程。
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: 轉換元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910036"
---
# <a name="transition-element"></a>轉換元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`transition`元素會定義轉換物件。 轉換是兩個輸入轉換，會導致從某個資料流程 (例如複合或追蹤) 轉換為另一個資料流程。

## <a name="attributes"></a>屬性

[**clsid**](clsid-attribute.md)、 [**cutpoint**](cutpoint-attribute.md)、 [**cutsonly**](cutsonly-attribute.md)、 [**lock**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**start**](start-attribute.md)、 [**stop**](stop-attribute.md)、 [**swapinputs**](swapinputs-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
|----------|------------------------------------------------------------------------|
| 父代   | [**複合**](composite-element.md)、 [**追蹤**](track-element.md) |
| Children | [**參數**](param-element.md)                                         |



 

## <a name="remarks"></a>備註

**Clsid** 屬性會指定建立轉換的子物件。

## <a name="examples"></a>範例


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



