---
description: 已淘汰，不應該使用。
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: 'ADDRESS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999901"
---
# <a name="address-structure"></a>位址結構

**位址** 結構已過時，不應該使用。

## <a name="syntax"></a>語法


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

地址類型。 它可以是下列其中一個值：

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**MACAddress**
</dt> <dd>

以原始 MAC 位址表示的資料。

</dd> <dt>

**IPAddress**
</dt> <dd>

以原始 IP 位址表示的資料。

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

以原始 IPX 位址表示的資料。

</dd> <dt>

**IPXAddress**
</dt> <dd>

查看以解碼的 IPX 位址值表示的資料。

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

以原始 Vines IP 位址表示的資料。

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

以解碼的 Vines IP 位址表示的資料。

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

以 Ethernet 來源位址表示的資料。

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

以乙太網路目的地位址表示的資料。

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

以 token 環形來源位址顯示的資料。

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

作為權杖響鈴目的地位址的資料檢視。

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

查看以 FDDI 來源位址表示的資料。

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

查看以 FDDI 目的地位址表示的資料。

</dd> <dt>

**旗標**
</dt> <dd>

修改位址屬性的一組旗標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




