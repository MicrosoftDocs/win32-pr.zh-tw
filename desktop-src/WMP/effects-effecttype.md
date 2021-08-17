---
title: 效果。 >effecttype
description: '>effecttype 方法會使用指定的登錄索引來抓取視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。'
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- 效果： >effecttype Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749230"
---
# <a name="effectseffecttype"></a>效果。 >effecttype

**>Effecttype** 方法會使用指定的登錄索引來抓取視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

包含視覺效果登錄索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

在腳本的視覺效果之間切換時，這個方法很有用。 使用者介面可以顯示一組標題，但是當使用者選取其中一個時，腳本必須使用 **currentEffectType** 來切換視覺效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> <dt>

[**效果。 currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





