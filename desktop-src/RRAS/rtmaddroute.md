---
title: 'RtmAddRoute 函式 (Rtm. h) '
description: RtmAddRoute 函式會新增路由專案，或更新現有的路由專案。
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965310"
---
# <a name="rtmaddroute-function"></a>RtmAddRoute 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmAddRoute** 函式會新增路由專案，或更新現有的路由專案。

## <a name="syntax"></a>語法


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientHandle* \[在\]
</dt> <dd>

識別用戶端的控制碼，以及新增或更新路由的路由通訊協定。 藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。

</dd> <dt>

*路由* \[在\]
</dt> <dd>

通訊協定系列特定結構的指標，指定新的或更新的路由。 路由表管理員會使用下欄欄位來更新路由表：



| 值                                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**RR \_ 網路**</dt> </dl>                                                     | 指定目的地網路編號。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**RR \_ InterfaceID**</dt> </dl>                                     | 指定接收路由的介面索引。<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**RR \_ NextHopAddress**</dt> </dl>                         | 指定下一個躍點路由器的位址。<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**RR \_ FamilySpecificData**</dt> </dl>         | 指定通訊協定系列的特定資料。 雖然資料對路由表管理員而言是透明的，但在比較路由以判斷路由資訊是否已變更時，會考慮這一點。 資料也會用來設定與路由通訊協定無關的度量值。 因此，此資料會用來決定目的地網路的最佳路由。<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**RR \_ ProtocolSpecificData**</dt> </dl> | 指定提供路由的路由通訊協定專用的資料。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**RR \_ 時間戳記**</dt> </dl>                                             | 指定目前的系統時間。 此欄位是由路由表管理員所設定。<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[在\]
</dt> <dd>

指定指定路由應保留在路由表中的秒數。 如果這個參數設為無限，路由會一直保留到明確刪除為止。 目前的 *TimeToLive* 限制為2147483秒 (24 + 天) 。

</dd> <dt>

*旗標* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標。 此變數的值是由路由表管理員所設定。 值指出變更的類型，以及在提供的緩衝區中傳回的資訊。 此參數是下列其中一項。



| Flags                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**RTM \_ 無 \_ 變更**</dt> </dl>             | 新增或更新可能不會變更任何重要的路由參數，或受影響的路由專案不是目的地網路專案之間的最佳路由。<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_ \_ 已新增 RTM 路由**</dt> </dl>       | 已為目的地網路新增路由。 *CurBestRoute* 參數會指向新增路由的資訊。<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM \_ 路由 \_ 已變更**</dt> </dl> | 至少有一個重要參數變更為目的地網路的最佳路由。 重要的參數包括： <br/> 通訊協定識別碼<br/> 介面索引<br/> 下個躍點位址<br/> 通訊協定系列特定的資料 (包括路由計量) <br/> |



 

*PrevBestRoute* 參數會指向變更之前的路由資訊。 *CurBestRoute* 參數指向目前的 (，也就是變更後) 路由資訊。

</dd> <dt>

*CurBestRoute* \[擴展\]
</dt> <dd>

結構的指標，此結構會接收目前的最佳路由資訊（如果有的話）。 結構的類型是通訊協定系列專用的，例如 IP 或 IPX。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。

</dd> <dt>

*PrevBestRoute* \[擴展\]
</dt> <dd>

結構的指標，此結構會接收先前的最佳路由資訊（如果有的話）。 結構的類型是通訊協定系列專用的，例如 IP 或 IPX。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則不會傳回先前的最佳路由資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個程式碼。



| 值                                                                                                       | 描述                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>                    | 已成功新增或更新路由。<br/>                 |
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | 用戶端控制碼參數不是有效的控制碼。<br/>           |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | 路由結構包含不正確參數。<br/>           |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/> |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>   | 記憶體不足，無法配置路由專案。<br/>    |



 

## <a name="remarks"></a>備註

如果目的地網路的最佳路由因為這項作業的結果而變更，此函式會產生路由變更訊息。 但是，不會將路由變更訊息傳送給進行此呼叫的用戶端。 相反地，此函式會透過 *Flags*、 *CurBestRoute* 和 *PrevBestRoute* 參數，將相關資訊直接傳回給該用戶端。

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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





