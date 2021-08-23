---
description: FindPropertyInstance 函數會尋找 hProperty 參數所指定之屬性的第一個實例。
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: 'FindPropertyInstance 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac8b7d34b33bb76bfffc26b3ae6fc455857fafb65a9a2aef7e91fd0c2763adc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938579"
---
# <a name="findpropertyinstance-function"></a>FindPropertyInstance 函式

**FindPropertyInstance** 函數會尋找 *hProperty* 參數所指定之屬性的第一個實例。

## <a name="syntax"></a>語法


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。 [GetFrame](getframe.md)函式的呼叫可以取出框架控制碼。

</dd> <dt>

*hProperty* \[在\]
</dt> <dd>

您要尋找的屬性的控制碼。 [GetProperty](getproperty.md)函式的呼叫可以取出屬性控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果) 找到此屬性，則傳回值為屬性之第一個實例的指標。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

若要取出屬性的下一個實例，請呼叫 [FindPropertyInstanceRestart](findpropertyinstancerestart.md)。

[*專家*](e.md) 和 [*剖析*](p.md)器可以呼叫 **FindPropertyInstance** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




