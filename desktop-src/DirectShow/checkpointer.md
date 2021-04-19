---
description: 檢查指標是否為 Null。 如果指標為 Null，則宏出現的函式或方法會傳回指定的值。
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: 'CheckPointer 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994360"
---
# <a name="checkpointer-macro"></a>CheckPointer 宏

檢查指標是否為 **Null**。 如果指標為 **Null**，則宏出現的函式或方法會傳回指定的值。

## <a name="syntax"></a>語法


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*P* 
</dt> <dd>

要檢查的指標。

</dd> <dt>

*Ret* 
</dt> <dd>

如果 *p* 為 **Null**，則函式或方法所傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *p* 為 **Null**，則周圍函數會傳回 *ret* 。 否則，宏不會造成周圍函數傳回。

## <a name="examples"></a>範例


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wxdebug (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指標驗證宏](pointer-validation-macros.md)
</dt> </dl>

 

 




