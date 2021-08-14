---
title: BUTTONGROUP. showBackground
description: ShowBackground 屬性會指定或抓取值，指出 BUTTONGROUP 是否只顯示按鈕，或顯示影像屬性中指定的完整點陣圖。
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP. showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342671"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP. showBackground

**ShowBackground** 屬性會指定或抓取值，指出 **BUTTONGROUP** 是否只顯示按鈕，或顯示 **影像** 屬性中指定的完整點陣圖。

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | 按鈕隨即顯示，而按鈕未佔用的區域則是從影像點陣圖繪製。 |
| false | 預設值。 只會顯示按鈕。                                                   |



 

## <a name="remarks"></a>備註

當 **showBackground** 為 true 時，會顯示整個主要 **映射** 。

當 **showBackground** 為 false 時，只會轉譯對應至已指派 **mappingImage** 色彩的區域。 換句話說，只會顯示已指派 **mappingColor** 的 **BUTTONELEMENTs** 。

如果指定了不正確值，則會維護先前的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





