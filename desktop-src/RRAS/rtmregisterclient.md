---
title: 'RtmRegisterClient 函式 (Rtm. h) '
description: RtmRegisterClient 函數會將用戶端註冊為指定之通訊協定的處理常式。 它會建立用戶端的路由變更通知機制，並設定通訊協定選項。
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient 函式 RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db58fc9457195c2149fd8d34a8a65a6d5085135275e1c878633f64cb742b02cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081038"
---
# <a name="rtmregisterclient-function"></a>RtmRegisterClient 函式

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmRegisterClient** 函數會將用戶端註冊為指定之通訊協定的處理常式。 它會建立用戶端的路由變更通知機制，並設定通訊協定選項。

## <a name="syntax"></a>語法


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolFamily* \[在\]
</dt> <dd>

指定要註冊之路由通訊協定的通訊協定系列。

</dd> <dt>

*RoutingProtocol* \[在\]
</dt> <dd>

指定路由通訊協定識別碼，與向路由器管理員註冊時所使用的相同。 請參閱 [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)。

</dd> <dt>

*ChangeEvent* \[在\]
</dt> <dd>

指定資料表中網路的最佳路由已變更。 路由表管理員會在變更為資料表中任何網路的最佳路由之後，對此事件發出信號。 如需路由變更通知的詳細資訊，請參閱 [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) 。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則路由表管理員不會通知用戶端最適合路由狀態的變更。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指定路由通訊協定特殊處理的其他選項。 目前支援下列值。



| Flags                                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**RTM \_ 通訊協定 \_ 單一 \_ 路由**</dt> </dl> | 路由表管理員只會針對路由通訊協定的每個目的地網路保留一個路由。 換句話說，路由表管理員會取代具有相同目的地網路編號的路由專案，而不是加入新的。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功傳回時，會在後續的路由表管理員呼叫中識別用戶端的 **控制碼** 值。

**Null** 控制碼指出路由表管理員無法註冊用戶端。 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得失敗的原因。



| 值                                                                                                         | 描述                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 用戶端 \_ 已 \_ 存在**</dt> </dl> | 另一個用戶端已註冊來處理指定的通訊協定。<br/>              |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>      | 不支援指定的通訊協定系列，或 *旗標* 參數無效。<br/> |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl>   | 資源不足，無法執行操作。<br/>                                   |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>     | 記憶體不足，無法配置用戶端的資料結構。<br/>                      |



 

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

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[RTMv1 通訊協定系列識別碼](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

