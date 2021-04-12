---
description: ExpertSubmitEvent 函式會指出事件條件存在，並提供描述條件的資料結構。
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: 'ExpertSubmitEvent 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318080"
---
# <a name="expertsubmitevent-function"></a>ExpertSubmitEvent 函式

**ExpertSubmitEvent** 函式會指出事件條件存在，並提供描述條件的資料結構。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

專家的唯一識別碼。 網路監視器在呼叫 [Run](run.md)函式時，將 *hExpertKey* 傳遞給專家。

</dd> <dt>

*pExpertEvent* \[在\]
</dt> <dd>

描述事件條件之 **NMEVENTDATA** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會指出失敗的原因。 如果傳回值是 NMERR \_ 專家 \_ 終止，則專家會立即清除並返回。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




