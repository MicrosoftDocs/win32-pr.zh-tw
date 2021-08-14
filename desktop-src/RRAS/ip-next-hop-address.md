---
title: 'IP_NEXT_HOP_ADDRESS 結構 (Rtm) '
description: IP \_ 下一個 \_ 躍點 \_ 位址結構包含 ip 路由之下一個躍點路由器的位址。
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS 結構 RAS
- PIP_NEXT_HOP_ADDRESS 結構 RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f79b850c7d5f48e5f409e5380ad7345288187b8939b752b4f282b2274a99cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790962"
---
# <a name="ip_next_hop_address-structure"></a>IP \_ 下一個 \_ 躍點 \_ 位址結構

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**Ip \_ 下一個 \_ 躍點 \_ 位址** 結構包含 ip 路由之下一個躍點路由器的位址。

## <a name="syntax"></a>語法


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

以電腦位元組順序指定以 IP 位址表示的 IP 網路位址。

</dd> <dt>

**N \_ 網路遮罩**
</dt> <dd>

指定網路遮罩。 將此遮罩套用至 IP 位址，以便將網路位址解壓縮。 網路遮罩是以電腦位元組順序排列。

</dd> </dl>

## <a name="remarks"></a>備註

**Ip \_ 下一個 \_ 躍點 \_ 位址** 結構是 [**ip \_ 網路**](ip-network.md)結構的 typedef。 Typedef 位於 Rtm. h 中。

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

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> </dl>

 

 





