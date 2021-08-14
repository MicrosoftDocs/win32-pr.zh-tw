---
description: GetProperty 函數會傳回指定之屬性的控制碼。
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: 'GetProperty 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 07bd5a88017ee16f3bdb1773973283d9ad0f7bc6a942fa4441fb134b5f1930da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365971"
---
# <a name="getproperty-function"></a>GetProperty 函式

**GetProperty** 函數會傳回指定之屬性的控制碼。

## <a name="syntax"></a>語法


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

通訊協定的控制碼。

</dd> <dt>

*PropertyName* \[在\]
</dt> <dd>

屬性的名稱 (例如，總和 **檢查** 碼) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為屬性的控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

**GetProperty** 函式可以用來取得尋找屬性實例所需的屬性控制碼。 用來找出屬性實例的函式是 [FindPropertyInstance](findpropertyinstance.md) (會找出第一個) 的實例，以及找出下一個) 的 [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetProperty** 函數。

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

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




