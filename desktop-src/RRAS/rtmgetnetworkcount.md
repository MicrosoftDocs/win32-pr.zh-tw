---
title: 'RtmGetNetworkCount 函式 (Rtm. h) '
description: RtmGetNetworkCount 函式會抓取路由表管理員已路由傳送的網路數目。
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c721605988f15661030ddbeaadf4140fb716a089c87cc46fc2a8316bc2de9e42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035668"
---
# <a name="rtmgetnetworkcount-function"></a>RtmGetNetworkCount 函式

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmGetNetworkCount** 函式會抓取路由表管理員已路由傳送的網路數目。

## <a name="syntax"></a>語法


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolFamily* \[在\]
</dt> <dd>

指定要取得路由資訊的網路類型，例如 IP 或 IPX。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是網路計數，也就是指定之通訊協定系列的路由通訊協定所知道的網路數目。

如果傳回值為零，表示沒有可用的路由，或作業失敗。 呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得詳細資訊。



| 值                                                                                                    | 描述                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>                 | 作業成功，但沒有可用的路由。<br/>                                             |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl> | *ProtocolFamily* 參數的值未對應到任何已安裝的通訊協定系列。<br/> |



 

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

[RTMv1 通訊協定系列識別碼](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

