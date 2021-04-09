---
title: 'RtmDeleteRoute 函式 (Rtm. h) '
description: RtmDeleteRoute 函式會刪除路由專案。
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934602"
---
# <a name="rtmdeleteroute-function"></a>RtmDeleteRoute 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmDeleteRoute** 函式會刪除路由專案。

## <a name="syntax"></a>語法


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientHandle* \[在\]
</dt> <dd>

識別用戶端的控制碼，因此是已新增或更新路由的路由通訊協定。 藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。

</dd> <dt>

*路由* \[在\]
</dt> <dd>

通訊協定系列特定結構的指標，指定新的或更新的路由。 路由表管理員會使用下欄欄位來更新路由表：



| 值                                                                                                                                                                                                         | 意義                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**RR \_ 網路**</dt> </dl>                             | 指定目的地網路編號。 <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>             | 指定接收路由的介面索引。<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl> | 指定下一個躍點路由器的網路位址。<br/>                      |



 

</dd> <dt>

*旗標* \[擴展\]
</dt> <dd>

一組旗標的指標，指出變更訊息的類型，以及在提供的緩衝區中放置哪些資訊。 此參數是下列其中一個值。



| Flags                                                                                                                                                                      | 意義                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ 無 \_ 變更**</dt> </dl>             | 刪除路由並不會影響到任何目的地網路的最佳路由。 換句話說，另一個專案代表相同目的地網路的路由，且具有較低的度量。<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_ \_ 已刪除 RTM 路由**</dt> </dl> | 已刪除的路由是特定目的地網路唯一可用的路由。<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM \_ 路由 \_ 已變更**</dt> </dl> | 刪除此路由之後，另一個路由就會成為特定目的地網路的最佳路由。 *CurBestRoute* 會指向新的最佳路由資訊。<br/>               |



 

</dd> <dt>

*CurBestRoute* \[擴展\]
</dt> <dd>

結構的指標，此結構會接收目前的最佳路由資訊（如果有的話）。 結構的類型是通訊協定系列專用的，例如 IP 或 IPX。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值不會是 **\_ 錯誤**。

如果函式失敗，則傳回值是下列其中一個錯誤碼。



| 值                                                                                                       | 描述                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | 用戶端控制碼參數不是有效的控制碼。<br/>                                          |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | *Route* 參數所指向的路由結構包含成員值。<br/>            |
| <dl> <dt>**錯誤 \_ 沒有 \_ 這類 \_ 路由**</dt> </dl>       | 路由表中沒有任何專案符合指定路由的參數。<br/> |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行此作業。 <br/>                                 |



 

## <a name="remarks"></a>備註

如果目的地網路的最佳路由變更為刪除的結果，此函式會產生路由變更訊息。 但是，不會將路由變更訊息傳送給進行此呼叫的用戶端。 相反地，此函式會將相關資訊直接傳回給該用戶端。

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

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





