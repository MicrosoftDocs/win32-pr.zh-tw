---
title: 'IPX_SPECIFIC_DATA 結構 (Rtm) '
description: IPX \_ 特定 \_ 資料結構包含 ipx 特定資料。
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA 結構 RAS
- PIPX_SPECIFIC_DATA 結構指標 RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0367e02dd8b0a46304538a2e5830e101eb9573e6548383fbae617a856df83621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790746"
---
# <a name="ipx_specific_data-structure"></a>IPX \_ 特定 \_ 資料結構

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**Ipx \_ 特定 \_ 資料** 結構包含 ipx 特定資料。

## <a name="syntax"></a>語法


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**FSD \_ 旗標**
</dt> <dd>

指定描述路由的旗標。 目前，這個成員是零或下列旗標值。



| 值                                                                                                                                                                                                      | 意義                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**IPX \_ 全域 \_ 用戶端 \_ WAN \_ 路由**</dt> </dl> | 指定此路由適用于配置給所有 WAN 用戶端的全域網路。<br/> |



 

</dd> <dt>

**FSD \_ TickCount**
</dt> <dd>

指定到達目的地網路所花費的刻度數目。 RIP 以外的路由通訊協定應該將其計量轉換成刻度。

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

指定與路由相關聯的躍點計數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Rtm. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[路由表管理員第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版結構](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IPX \_ 路由**](rtm-ipx-route.md)
</dt> </dl>

 

 





