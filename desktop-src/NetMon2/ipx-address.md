---
description: IPX \_ 位址結構會提供 ipx 通訊協定層級的位址。
ms.assetid: 06939ac3-3718-4441-b2c8-c73adfe3babe
title: 'IPX_ADDRESS 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPX_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 18645a455e780020037384a2df7173a019d71677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511240"
---
# <a name="ipx_address-structure"></a>IPX \_ 位址結構

**Ipx \_ 位址** 結構會提供 ipx 通訊協定層級的位址。

## <a name="syntax"></a>語法


```C++
typedef struct _IPX_ADDRESS {
  BYTE Subnet[4];
  BYTE Address[6];
} IPX_ADDRESS, *LPIPX_ADDRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**子網路**
</dt> <dd>

網路子網識別碼。

</dd> <dt>

**位址**
</dt> <dd>

子網 NIC 識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




