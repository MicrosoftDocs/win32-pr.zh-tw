---
title: 'IP_NETWORK 結構 (Rtm) '
description: IP \_ 網路結構描述 ip 網路位址。
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK 結構 RAS
- PIP_NETWORK 結構指標 RAS
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686152"
---
# <a name="ip_network-structure"></a>IP \_ 網路結構

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**Ip \_ 網路** 結構描述 ip 網路位址。

## <a name="syntax"></a>語法


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a>成員

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

指定以電腦位元組順序表示的 ip 網路編號（以 IP 位址表示）。

</dd> <dt>

**N \_ 網路遮罩**
</dt> <dd>

指定網路遮罩。 將此遮罩套用至 IP 位址，以便將網路位址解壓縮。 網路遮罩是以電腦位元組順序排列。

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

[**RTM \_ IP \_ 路由**](rtm-ip-route.md)
</dt> </dl>

 

 





