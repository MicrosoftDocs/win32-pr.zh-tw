---
title: 'RTM_IP_ROUTE 結構 (Rtm) '
description: RTM \_ ip \_ 路由結構包含描述 IP 通訊協定系列所擁有之路由的資訊。
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE 結構 RAS
- PRTM_IP_ROUTE 結構指標 RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd854864dcc61397fa52df7af9419a38ac829a81382be6b6190e4cb3db41d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026728"
---
# <a name="rtm_ip_route-structure"></a>RTM \_ IP \_ 路由結構

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RTM \_ ip \_ 路由** 結構包含描述 IP 通訊協定系列所擁有之路由的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
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

指定 [**通訊協定 \_ 特定的 \_ 資料**](protocol-specific-data.md) 結構，其中包含保留給路由通訊協定特定資料的記憶體。

</dd> <dt>

**RR \_ 網路**
</dt> <dd>

指定包含 IP 網路位址的 [**ip \_ 網路**](ip-network.md) 結構。

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

指定 [**IP \_ 下一個 \_ 躍點 \_ 位址**](ip-next-hop-address.md) 結構，其中包含下一個躍點路由器的位址。

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

指定包含 IP 通訊協定系列特定資料的 [**ip \_ 特定 \_ 資料**](ip-specific-data.md) 結構。

</dd> </dl>

## <a name="remarks"></a>備註

**RTM \_ IP \_ 路由** 結構的成員都已對齊 **DWORD** 。

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

[**IP \_ 網路**](ip-network.md)
</dt> <dt>

[**IP \_ 下一個 \_ 躍點 \_ 位址**](ip-next-hop-address.md)
</dt> <dt>

[**IP \_ 特定 \_ 資料**](ip-specific-data.md)
</dt> </dl>

 

 





