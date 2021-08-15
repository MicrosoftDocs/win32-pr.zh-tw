---
description: FilterAddObject 函式會將單一物件加入至顯示篩選。
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: 'FilterAddObject 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938731"
---
# <a name="filteraddobject-function"></a>FilterAddObject 函式

**FilterAddObject** 函式會將單一物件加入至 [*顯示篩選*](d.md)。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFilter* \[在\]
</dt> <dd>

顯示篩選的控制碼。

</dd> <dt>

*lpFilterObject* \[擴展\]
</dt> <dd>

[FILTEROBJECT](filterobject.md)結構的指標，該結構定義要加入至篩選的物件。 每個物件都可以是運算子、值或屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                              | Description                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 不正確 \_ 參數**</dt> </dl> | *HFilter* 參數的值無效。<br/>                     |
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl>    | 網路監視器沒有足夠的記憶體可建立物件。<br/> |



 

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **FilterAddObject** 函數。

每次將篩選物件加入至顯示篩選時，就會呼叫 **FilterAddObject** 函數。 顯示篩選是物件的後置堆疊，可以是運算子、值或屬性。

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

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




