---
description: SetQOSApplicationID 方法會設定應用程式的 QOS 識別碼。
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID：： SetQOSApplicationID 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e7783efaf8ec30ea8f70fec634eefff0acd2f5df99453fc1958258a5a26597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774588"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ITQOSApplicationID：： SetQOSApplicationID 方法

\[此方法無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**SetQOSApplicationID** 方法會設定應用程式的 QOS 識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pApplicationID* \[在\]
</dt> <dd>

應用程式進程的唯一識別碼。

</dd> <dt>

*pApplicationGUID* \[在\]
</dt> <dd>

應用程式 GUID。

</dd> <dt>

*pSubIDs* \[在\]
</dt> <dd>

與目前呼叫相關聯的 Sub-IDs。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




