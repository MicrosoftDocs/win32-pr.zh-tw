---
title: BUTTONGROUP 電臺
description: 單選屬性會指定或抓取值，指出 BUTTONGROUP 是否包含在選項按鈕中。
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP 電臺 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997768"
---
# <a name="buttongroupradio"></a>BUTTONGROUP 電臺

**單選** 屬性會指定或抓取值，指出 **BUTTONGROUP** 是否包含在選項按鈕中。

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                      |
|-------|--------------------------------------------------|
| true  | **BUTTONGROUP** 為單選樣式。              |
| false | 預設值。 **BUTTONGROUP** 不是無線電樣式。 |



 

## <a name="remarks"></a>備註

如果 [**無線電**] 設定為 [true]， **BUTTONGROUP** 中的所有 **BUTTONELEMENT** 元素都會是粘滯，但是一次只有一個按鈕會處於關閉狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONELEMENT。**](buttonelement-sticky.md)
</dt> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> </dl>

 

 





