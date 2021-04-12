---
description: VINES \_ ip \_ 位址結構是 VINES 網路上的 ip 位址。
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: 'VINES_IP_ADDRESS 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319495"
---
# <a name="vines_ip_address-structure"></a>VINES \_ IP \_ 位址結構

**VINES \_ ip \_ 位址** 結構是 VINES 網路上的 ip 位址。

## <a name="syntax"></a>語法


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a>成員

<dl> <dt>

**NetID**
</dt> <dd>

特定子網上特定電腦的識別碼。

</dd> <dt>

**SubnetID**
</dt> <dd>

整個網路上特定子網的識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




