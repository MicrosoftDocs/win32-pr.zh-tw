---
description: SetQOSApplicationID 方法會設定應用程式的 QOS 識別碼。
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID：： SetQOSApplicationID 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979477"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ITQOSApplicationID：： SetQOSApplicationID 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

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



| 傳回碼                                                                                   | Description                                                     |
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

 

 




