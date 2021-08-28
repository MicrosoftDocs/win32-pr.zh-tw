---
description: DECLARE \_ IUNKNOWN 宏會為新介面宣告基底介面的三種方法。
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: 'DECLARE_IUNKNOWN (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21ba606a5721635398cc9bcf48bba70978e00354188e1a62d83239c853a28b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953207"
---
# <a name="declare_iunknown"></a>宣告 \_ IUNKNOWN

**DECLARE \_ IUNKNOWN** 宏會為新介面宣告基底介面的三種方法。

**語法**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>備註

當您建立新的介面時，它必須衍生自 **IUnknown**，其中有三個方法： **QueryInterface**、 **AddRef** 和 **Release**。 這個宏會針對新介面宣告這些方法，藉此簡化宣告程式。

這個宏只適用于直接或間接衍生自 [**CUnknown**](cunknown.md) 類別的類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COM Helper 函數**](com-helper-functions.md)
</dt> <dt>

[**CUnknown：： GetOwner**](cunknown-getowner.md)
</dt> <dt>

[如何執行 IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




