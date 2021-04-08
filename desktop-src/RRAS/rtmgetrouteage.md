---
title: 'RtmGetRouteAge 函式 (Rtm. h) '
description: RtmGetRouteAge 函數會傳回路由的年齡。 Age 是建立或上次更新之後的時間（以秒為單位）。
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686078"
---
# <a name="rtmgetrouteage-function"></a>RtmGetRouteAge 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmGetRouteAge** 函數會傳回路由的年齡。 Age 是建立或上次更新之後的時間（以秒為單位）。

## <a name="syntax"></a>語法


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*路由* \[在\]
</dt> <dd>

通訊協定系列特定結構的指標，指定最近從路由表管理員取得的路由資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個值。



| 值                                                                                   | 描述                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**RouteAge**</dt> </dl> | 建立路由或上次更新之後的時間（以秒為單位）。<br/>                                                                                    |
| <dl> <dt>**INFINITE**</dt> </dl> | 路由結構的內容無效。 在此情況下，對 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的呼叫會傳回錯誤 \_ 無效 \_ 的參數。<br/> |



 

## <a name="remarks"></a>備註

路由存留期是從 \_ *路由* 參數所指向之結構的 RR TimeStamp 成員計算而來。 當新增或更新路由時，路由表管理員會設定這個成員的值。

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

[路由表管理員 \_ 第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版函數](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ 路由**](rtm-ipx-route.md)
</dt> </dl>

 

