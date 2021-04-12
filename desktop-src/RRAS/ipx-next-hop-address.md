---
title: 'IPX_NEXT_HOP_ADDRESS 結構 (Rtm) '
description: IPX \_ 下一個 \_ 躍點 \_ 位址結構包含 ipx 路由的下個躍點路由器的位址。
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS 結構 RAS
- PIPX_NEXT_HOP_ADDRESS 結構指標 RAS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464201"
---
# <a name="ipx_next_hop_address-structure"></a>IPX \_ 下一個 \_ 躍點 \_ 位址結構

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**Ipx \_ 下一個 \_ 躍點 \_ 位址** 結構包含 ipx 路由的下個躍點路由器的位址。

## <a name="syntax"></a>語法


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**NHA \_ Mac**
</dt> <dd>

指定下一個躍點路由器的 MAC 位址。

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

 

 





