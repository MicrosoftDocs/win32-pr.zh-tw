---
title: EQUALIZERSETTINGS.gainLevels
description: GainLevels 屬性會指定或抓取對應于所提供之索引的帶狀增益層級。
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977463"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

**GainLevels** 屬性會指定或抓取對應于所提供之索引的帶狀增益層級。

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*
</dt> <dd>

**數位** (**長**) 介於1到10之間，表示帶狀的索引。

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會接受參數，但其值是以與其他屬性值相同的方式，在腳本程式碼中指定。 它不能在 EQUALIZERSETTINGS 元素中指定，也不能與 **wmpprop** 接聽屬性一起使用。 相反地，在這些情況下，會提供編號增益層級的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**接聽屬性**](listening-attributes.md)
</dt> </dl>

 

 





