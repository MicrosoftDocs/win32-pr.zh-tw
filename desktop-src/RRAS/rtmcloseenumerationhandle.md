---
title: 'RtmCloseEnumerationHandle 函式 (Rtm. h) '
description: RtmCloseEnumerationHandle 會終止指定的列舉，並釋出相關聯的資源。
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RtmCloseEnumerationHandle 函式 RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025241"
---
# <a name="rtmcloseenumerationhandle-function"></a>RtmCloseEnumerationHandle 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmCloseEnumerationHandle** 會終止指定的列舉，並釋出相關聯的資源。

## <a name="syntax"></a>語法


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EnumerationHandle* \[在\]
</dt> <dd>

要終止之列舉的控制碼。 藉由呼叫 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)來取得此控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值不會是 \_ 錯誤。

如果函式失敗，則傳回值是下列其中一個錯誤碼。



| 值                                                                                                       | 描述                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | 參數無效。<br/>                                  |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Rtm. h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Rtm .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[路由表管理員第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版函數](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





