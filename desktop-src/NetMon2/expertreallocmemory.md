---
description: ExpertReallocMemory 函式會增加或減少網路監視器所配置的記憶體數量。
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: 'ExpertReallocMemory 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973420"
---
# <a name="expertreallocmemory-function"></a>ExpertReallocMemory 函式

**ExpertReallocMemory** 函式會增加或減少網路監視器所配置的記憶體數量。

## <a name="syntax"></a>語法


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

[**執行**](run.md)或 [**設定**](configure.md)時傳遞給專家的唯一識別碼。

</dd> <dt>

*pOriginalMemory* \[在\]
</dt> <dd>

網路監視器所配置之記憶體的指標。 *POriginalMemory* 指標可由前一個對 [**ExpertAllocMemory**](expertallocmemory.md)或 **ExpertReallocMemory** 的呼叫傳回。

</dd> <dt>

*n* \[在\]
</dt> <dd>

重新配置記憶體的大小。

</dd> <dt>

*pError* \[擴展\]
</dt> <dd>

傳回時，如果函式失敗，則為錯誤碼。 如果錯誤碼是 NMERR \_ 專家 \_ 終止，則專家必須清除並立即返回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是所配置之記憶體的指標。

如果函式不成功，則傳回值為 **null**，而且如果是非 **Null** 值，則 *pError* () 指出失敗的原因。

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



 

 




