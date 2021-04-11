---
title: 'RtmDequeueRouteChangeMessage 函式 (Rtm. h) '
description: RtmDequeueRouteChangeMessage 函式會傳回與指定之用戶端相關聯之佇列中的下一個路由變更訊息。
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage 函式 RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104388"
---
# <a name="rtmdequeueroutechangemessage-function"></a>RtmDequeueRouteChangeMessage 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmDequeueRouteChangeMessage** 函式會傳回與指定之用戶端相關聯之佇列中的下一個路由變更訊息。

## <a name="syntax"></a>語法


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientHandle* \[在\]
</dt> <dd>

識別要執行作業之用戶端的控制碼。 藉由呼叫 [**RtmRegisterClient**](rtmregisterclient.md)來取得此控制碼。

</dd> <dt>

*旗標* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標。 此變數的值是由路由表管理員所設定。 值會指定變更訊息的類型，以及在提供的緩衝區中傳回的資訊。 此參數是下列其中一項。



| Flags                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_ \_ 已新增 RTM 路由**</dt> </dl>       | 已針對特定目的地網路新增第一個路由。 *CurBestRoute* 參數會指向新增路由的資訊。<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_ \_ 已刪除 RTM 路由**</dt> </dl> | 特定目的地網路唯一可用的路由已刪除。 *PrevBestRoute* 參數會指向已刪除之路由的資訊。<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**RTM \_ 路由 \_ 已變更**</dt> </dl> | 至少有一個重要的參數變更，以取得特定目的地網路的最佳路由。 重要的參數包括： <br/> 通訊協定識別碼<br/> 介面索引<br/> 下個躍點位址<br/> 通訊協定系列特定的資料 (包括路由計量) <br/> |



 

*PrevBestRoute* 參數會指向變更之前的路由資訊。 *CurBestRoute* 參數會指向目前的 (，也就是變更後) 路由資訊。

</dd> <dt>

*CurBestRoute* \[擴展\]
</dt> <dd>

結構的指標，此結構會接收目前的最佳路由資訊 (是否有任何) 。 結構的類型是通訊協定系列專用的，例如 IP 或 IPX。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則不會傳回目前的最佳路由資訊。

</dd> <dt>

*PrevBestRoute* \[擴展\]
</dt> <dd>

結構的指標，此結構會接收先前的最佳路由資訊（如果有的話）。 結構的類型是通訊協定系列專用的，例如 IP 或 IPX。

這是選擇性參數。 如果呼叫端為此參數指定 **Null** ，則不會傳回先前的最佳路由資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個程式碼。



| 值                                                                                                       | 描述                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>                    | 此訊息是用戶端佇列中的最後一則訊息。 事件物件已重設。<br/>                                                                                                                                               |
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | *ClientHandle* 參數不是有效的控制碼，或在註冊時，用戶端未提供變更訊息通知的事件物件 (請參閱 [**RtmRegisterClient**](rtmregisterclient.md)) 。<br/>                           |
| <dl> <dt>**錯誤 \_ 的 \_ 訊息**</dt> </dl>        | 用戶端的佇列包含額外的訊息。 用戶端應該儘快呼叫 **RtmDequeueRouteChangeMessage** ，以允許路由表管理員釋放與擱置中訊息相關聯的資源。<br/> |
| <dl> <dt>**錯誤 \_ \_ 訊息**</dt> </dl>          | 用戶端的佇列不包含任何訊息;呼叫未經要求。 此事件已重設。<br/>                                                                                                                                            |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/>                                                                                                                                                                      |



 

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

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





