---
description: ExpertAllocMemory 函式會為專家配置記憶體。
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: 'ExpertAllocMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd932a5330baf687d5578bac4e4bfac77ad4f5bad0560263ab7f1e8832e61fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890848"
---
# <a name="expertallocmemory-function"></a>ExpertAllocMemory 函式

**ExpertAllocMemory** 函式會為專家配置記憶體。

## <a name="syntax"></a>語法


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* 
</dt> <dd>

獨特的專家識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*n* \[在\]
</dt> <dd>

配置的記憶體（以位元組為單位）。

</dd> <dt>

*pError* \[擴展\]
</dt> <dd>

錯誤指標。 如果函式失敗， *n* 參數會包含錯誤碼。 如果錯誤碼是 NMERR \_ 專家 \_ 終止，則專家必須清除並立即返回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是所配置之記憶體的指標。

如果函式不成功，則傳回值為 **Null**，而 *pError* 會提供錯誤碼來指出失敗的原因。

## <a name="remarks"></a>備註

請務必注意，專家應該使用網路監視器記憶體配置函式 (包括記憶體管理的 [ExpertReallocMemory](expertreallocmemory.md)) 。 如果您的專家在執行時間失敗，使用這些函式會允許網路監視器釋出它所配置的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




