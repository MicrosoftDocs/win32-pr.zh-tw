---
title: 效果。 currentEffectType
description: CurrentEffectType 屬性會指定或抓取目前視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- 效果： currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996748"
---
# <a name="effectscurrenteffecttype"></a>效果。 currentEffectType

**CurrentEffectType** 屬性會指定或抓取目前視覺效果的登錄名稱。 這個名稱是視覺效果作者所定義的唯一識別碼。

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

您可以在執行時間使用這個屬性來變更目前顯示的效果。 若要這樣做，請遵循下列步驟：

1.  使用 **effectCount** 來取得已註冊效果的計數。
2.  在迴圈中，使用 **>effecttype** 取出每個已註冊效果的名稱。
3.  指定您為 **currentEffectType** 抓取的其中一個名稱，以設定目前的效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> <dt>

[**效果。 currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**效果。 effectCount**](effects-effectcount.md)
</dt> <dt>

[**效果。 >effecttype**](effects-effecttype.md)
</dt> </dl>

 

 





