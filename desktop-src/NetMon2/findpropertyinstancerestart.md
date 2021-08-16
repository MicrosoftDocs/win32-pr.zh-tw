---
description: 尋找 hProperty 參數所指定之屬性的下一個實例。
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: 'FindPropertyInstanceRestart 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0699cb37165e9181bf78bc3a86ad68c07dbbd589469e3e0bca6a1cd0228573f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890808"
---
# <a name="findpropertyinstancerestart-function"></a>FindPropertyInstanceRestart 函式

**FindPropertyInstanceRestart** 函數會尋找 *hProperty* 參數所指定之屬性的下一個實例。

## <a name="syntax"></a>語法


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
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

要尋找之屬性的控制碼。 [GetProperty](getproperty.md)函式的呼叫可以取出屬性控制碼。

</dd> <dt>

*lpRestartKey* \[在\]
</dt> <dd>

當做搜尋起點使用的屬性實例指標。 如果 *lpRestartKey* 參數設定為 **Null**，則會根據 *DirForward* 參數的值，從框架的開頭或框架的結尾開始搜尋。

如果 *lpRestartKey* 指向 **Null**，則會在 *DirForward* 為 **TRUE** 時從框架的開頭開始搜尋，如果參數為 **FALSE**，則會從框架的結尾開始搜尋。

</dd> <dt>

*DirForward* \[在\]
</dt> <dd>

搜尋方向的指標。 如果值為 **TRUE**，搜尋會從目前的位置移至框架的結尾。 如果值為 **FALSE**，搜尋會從目前的位置移至框架的開頭。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是下一個有效的 **LPPROPERTYINST**。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **FindPropertyInstanceRestart** 函數。

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

[GetFrame](getframe.md)
</dt> <dt>

[GetProperty](getproperty.md)
</dt> </dl>

 

 




