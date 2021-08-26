---
title: 'RtmEnumerateGetNextRoute 函式 (Rtm. h) '
description: RtmEnumerateGetNextRoute 函式會傳回列舉中由 RtmCreateEnumerationHandle 呼叫開始的下一個路由專案。
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6105340003c6240b49acec4699fa7b229d11963116367ab0fa0c069211b6fd1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035868"
---
# <a name="rtmenumerategetnextroute-function"></a>RtmEnumerateGetNextRoute 函式

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmEnumerateGetNextRoute** 函式會傳回列舉中由 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)呼叫開始的下一個路由專案。

## <a name="syntax"></a>語法


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*EnumerationHandle* \[在\]
</dt> <dd>

識別列舉的控制碼，並指定其範圍。 藉由呼叫 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)來取得此控制碼。

</dd> <dt>

*路由* \[擴展\]
</dt> <dd>

通訊協定系列特定路由結構的指標， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。 此結構會接收列舉中的下一個路由。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值不會是 \_ 錯誤。

如果函式失敗，則傳回值是下列其中一個錯誤碼。



| 值                                                                                                       | 描述                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | *EnumerationHandle* 參數無效。<br/>              |
| <dl> <dt>**錯誤 \_ 沒有 \_ 其他 \_ 路由**</dt> </dl>      | 列舉中沒有任何路由。<br/>                 |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

雖然路由不會以任何特定順序傳回，但是列舉中的每個路由只會傳回一次。

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

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ 路由**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





