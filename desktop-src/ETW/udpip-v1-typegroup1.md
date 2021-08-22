---
description: UdpIp_V1_TypeGroup1 類別-這個類別是 UDP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2c4a16dc8e0d08ab70a15b1d6a887ff8863a1b81c46c4318421df2169fd5d196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069338"
---
# <a name="udpip_v1_typegroup1-class"></a>UdpIp \_ V1 \_ TypeGroup1 類別

此類別是 UDP/IP 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>成員

**UdpIp \_ V1 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**UdpIp \_ V1 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，副檔名 ( "IPAddr" ) 
</dt> </dl>

目的地 IP 位址。

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) ，擴充 ( "Port" ) 
</dt> </dl>

目的地埠號碼。

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

與要求相關聯之進程的識別碼。

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，副檔名 ( "IPAddr" ) 
</dt> </dl>

來源 IP 位址。

</dd> <dt>

{1}size{2}
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

封包的大小。

</dd> <dt>

運動
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) ，擴充 ( "Port" ) 
</dt> </dl>

來源埠號碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




