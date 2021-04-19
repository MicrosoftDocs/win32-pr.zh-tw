---
description: LockIt 類別是鎖定和解除鎖定的內部類別。
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'IMediaObjectImpl：： LockIt 類別 (Dmoimpl .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994224"
---
# <a name="imediaobjectimpllockit-class"></a>IMediaObjectImpl：： LockIt 類別

`LockIt`類別是鎖定和解除鎖定的內部類別。

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="p"></span><span id="P"></span>*P*
</dt> <dd>

衍生物件的指標。

</dd> </dl>

## <a name="remarks"></a>備註

此 `LockIt` 函式會鎖定，而此函式會解除鎖定。 若要從您的衍生類別內鎖定物件，請宣告類型的本機變數 `LockIt` 。 當物件保持在範圍內時，會鎖定 `LockIt` ：


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



**IMediaObjectImpl** 中的方法會自動鎖定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dmoimpl。h</dt> </dl>                                                                     |
| 程式庫<br/> | <dl> <dt>Dmoguids .lib;</dt><dt>Msdmo .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMediaObjectImpl 類別範本**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




