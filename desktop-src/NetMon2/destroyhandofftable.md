---
description: DestroyHandoffTable 函式會終結以 CreateHandoffTable 建立的遞交資料表。
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: 'DestroyHandoffTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ec956ff4d0098b5a8992d6d28ab10afb925e76cb95b55d85ea7aa813ab2ba3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796264"
---
# <a name="destroyhandofftable-function"></a>DestroyHandoffTable 函式

**DestroyHandoffTable** 函式會終結以 **CreateHandoffTable** 建立的遞交資料表。

## <a name="syntax"></a>語法


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTable* \[在\]
</dt> <dd>

損毀的交付資料表的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




