---
title: 'DeducingStringGetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 getter 回呼。
ms.assetid: 434E3360-D6C3-46CB-818E-15A185F4BB84
keywords:
- DeducingStringGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99e23a2f79f38527dfae76c74e5e2ad8b828dce1a0ff984f622bd95fd287c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342958"
---
# <a name="deducingstringgetter"></a>DeducingStringGetter

會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 getter 回呼。

> [!Note]  
> DeducingStringGetter 不應該直接呼叫。

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringGetter(
    _In_ HRESULT (C::*callback)(PWSTR, UINT32, UINT32*) const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize 
    ) 
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D2d1effecthelpers。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Direct2D：:D educingStringSetter**](deducingstringsetter.md)
</dt> </dl>

 

 





