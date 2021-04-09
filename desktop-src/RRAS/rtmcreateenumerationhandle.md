---
title: 'RtmCreateEnumerationHandle 函式 (Rtm. h) '
description: RtmCreateEnumerationHandle 函式會傳回要搭配 RtmEnumerateGetNextRoute 使用的控制碼，以掃描路由表管理員已知的所有路由或路由的子集。
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle 函式 RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094064"
---
# <a name="rtmcreateenumerationhandle-function"></a>RtmCreateEnumerationHandle 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmCreateEnumerationHandle** 函式會傳回要搭配 [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)使用的控制碼，以掃描路由表管理員已知的所有路由或路由的子集。

## <a name="syntax"></a>語法


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolFamily* \[在\]
</dt> <dd>

指定要列舉之路由的通訊協定系列。

</dd> <dt>

*EnumerationFlags* \[在\]
</dt> <dd>

指定應列舉的路由。 此參數會將列舉 API 傳回的路由集合，限制為下列旗標所定義的子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。 此參數可以是下列其中一個值。



| EnumerationFlags                                                                                                                                                                              | 意義                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**\_僅 RTM \_ 此 \_ 網路**</dt> </dl>       | 只列舉與 \_ CriteriaRoute 所指向之結構的 RR 網路成員具有相同網路編號的路由。<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**\_僅 RTM \_ 此 \_ 介面**</dt> </dl> | 只列舉透過 \_ CriteriaRoute 所指向之結構的 RR InterfaceID 欄位所指定的介面所取得的路由。<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**\_僅 RTM \_ 此 \_ 通訊協定**</dt> </dl>    | 只列舉由 \_ CriteriaRoute 所指向之結構的 RR RoutingProtocol 欄位所指定的路由通訊協定所加入的路由。<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**\_僅 RTM \_ 最適合的 \_ 路由**</dt> </dl>          | 只列舉集合中每個網路的最佳路由。<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[在\]
</dt> <dd>

通訊協定系列特定路由結構的指標， ([**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。 此結構中的成員值會對應至 *EnumerationFlags* 參數所指定的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值會是用於後續列舉呼叫的 **控制碼** 。

如果函式失敗，或沒有具有指定準則的路由存在，則傳回值為 **Null**。 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊。



| 值                                                                                                       | 描述                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 沒有 \_ 路由**</dt> </dl>            | 沒有具有指定準則的路由。<br/>                                                             |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | 一或多個輸入參數無效 (例如，未知的通訊協定系列、不正確列舉旗標) 。<br/> |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/>                                                      |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>   | 記憶體不足，無法配置此控制碼。<br/>                                                              |



 

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

[**3]。Getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ 路由**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

