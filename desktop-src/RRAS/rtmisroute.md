---
title: 'RtmIsRoute 函式 (Rtm. h) '
description: RtmIsRoute 函式會判斷是否有一或多個路由傳送至指定的目的地網路。 如果是，則函式會傳回最適合該網路的路由資訊。
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312b43a7cf66e17cc6016fe3ad35bd21cd1e7ae19ecd7864a10de4d977a92ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073808"
---
# <a name="rtmisroute-function"></a>RtmIsRoute 函式

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmIsRoute** 函式會判斷是否有一或多個路由傳送至指定的目的地網路。 如果是，則函式會傳回最適合該網路的路由資訊。

## <a name="syntax"></a>語法


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolFamily* \[在\]
</dt> <dd>

指定 *Network* 參數所指向的資料結構類型，例如 [**IP \_ network**](ip-network.md)、 [**IPX \_ network**](ipx-network.md)。

</dd> <dt>

*網路* \[在\]
</dt> <dd>

結構的指標，指定通訊協定系列特定的網路編號資料。 此資料會識別呼叫端搜尋路由資訊的網路。

</dd> <dt>

*BestRoute* \[擴展\]
</dt> <dd>

通訊協定系列特定結構的指標，此結構會接收目前最佳的路由資訊（如果有的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個程式碼。



| 值                                                                                                       | 描述                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**真**</dt> </dl>                         | 至少有一個指定網路的路由存在。 最佳路由會傳回在 *BestRoute* 參數所指向的結構中。<br/>      |
| <dl> <dt>**假**</dt> </dl>                        | 沒有指定網路的路由，或操作失敗。 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊：<br/> |
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>                    | 作業成功，但沒有指定網路的路由。<br/>                                                                      |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | *ProtocolFamily* 參數的值未對應到任何已安裝的通訊協定系列。<br/>                                             |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/>                                                                                  |



 

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

[**IP \_ 網路**](ip-network.md)
</dt> <dt>

[**IPX \_ 網路**](ipx-network.md)
</dt> <dt>

[RTMv1 通訊協定系列識別碼](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

