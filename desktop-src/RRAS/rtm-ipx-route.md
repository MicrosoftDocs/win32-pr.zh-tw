---
title: 'RTM_IPX_ROUTE 結構 (Rtm) '
description: RTM \_ ipx \_ 路由結構包含描述 IPX 通訊協定系列之路由的資訊。
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE 結構 RAS
- PRTM_IPX_ROUTE 結構指標 RAS
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934151"
---
# <a name="rtm_ipx_route-structure"></a>RTM \_ IPX \_ 路由結構

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RTM \_ ipx \_ 路由** 結構包含描述 IPX 通訊協定系列之路由的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a>成員

<dl> <dt>

**RR \_ 時間戳記**
</dt> <dd>

指定建立或上次更新路由專案的時間。 此成員是由路由表管理員所設定。 時間會表示為 FILETIME 結構。

</dd> <dt>

**RR \_ RoutingProtocol**
</dt> <dd>

指定新增路由的路由通訊協定。

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

指定取得路由的介面。

</dd> <dt>

**RR \_ ProtocolSpecificData**
</dt> <dd>

指定 [**通訊協定 \_ 特定的 \_ 資料**](protocol-specific-data.md) 結構，其中包含針對路由通訊協定特定資料所保留的記憶體。

</dd> <dt>

**RR \_ 網路**
</dt> <dd>

指定包含 IP 網路位址的 [**IPX \_ 網路**](ipx-network.md) 結構。

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

指定包含下一個躍點路由器位址的 [**IPX \_ 下一個 \_ 躍點 \_ 位址**](ipx-next-hop-address.md) 結構。

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

指定包含 IPX 通訊協定系列專屬資料的 [**\_ 特定 ipx \_ 資料**](ipx-specific-data.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

**RTM \_ IPX \_ 路由** 結構的成員都已對齊 **DWORD** 。

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

[路由表管理員 \_ 第1版 \_ 結構](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**IPX \_ 網路**](ipx-network.md)
</dt> <dt>

[**IPX \_ 下一個 \_ 躍點 \_ 位址**](ipx-next-hop-address.md)
</dt> <dt>

[**\_特定 IPX \_ 資料**](ipx-specific-data.md)
</dt> </dl>

 

 





