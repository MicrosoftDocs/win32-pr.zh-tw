---
description: ExpertFreeMemory 函式會釋出呼叫 ExpertAllocMemory 和 ExpertReallocMemory 函數所取得的記憶體。
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: 'ExpertFreeMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: edc4d1a9e33139372d0f397053d233a28c9e2445ba270a47e7dbfe97090eb6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890827"
---
# <a name="expertfreememory-function"></a>ExpertFreeMemory 函式

**ExpertFreeMemory** 函式會釋出呼叫 [**ExpertAllocMemory**](expertallocmemory.md)和 [**ExpertReallocMemory**](expertreallocmemory.md)函數所取得的記憶體。

## <a name="syntax"></a>語法


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* 
</dt> <dd>

獨特的專家識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*pMemory* \[在\]
</dt> <dd>

網路監視器配置之記憶體的指標。 *PMemory* 指標可由前一個對 [**ExpertAllocMemory**](expertallocmemory.md)或 [**ExpertReallocMemory**](expertreallocmemory.md)的呼叫傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則為。 傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會指出失敗的原因。 如果傳回值是 NMERR \_ 專家 \_ 終止，則專家會立即清除並返回。

## <a name="remarks"></a>備註

請務必注意，專家應該使用網路監視器記憶體配置函式來進行記憶體管理。 如果您的專家在執行時間失敗，使用這些函式會允許網路監視器釋出它所配置的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




