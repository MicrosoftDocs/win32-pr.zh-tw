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
ms.openlocfilehash: 23a590679fd2b4a147a8bc0f92a4d4c7b4afb8c746526de9fba7cfc388e4e1c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742198"
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



 

 




