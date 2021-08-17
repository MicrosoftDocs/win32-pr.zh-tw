---
description: TcpIp_V0_TypeGroup1 類別-這個類別是 TCP/IP 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 29211ae7a5aca5abc33af545ba581c4baf82f1dac51c72b910f8251560ea92d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069568"
---
# <a name="tcpip_v0_typegroup1-class"></a>TcpIp \_ V0 \_ TypeGroup1 類別

這個類別是 TCP/IP 事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a>成員

**TcpIp \_ V0 \_ TypeGroup1** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TcpIp \_ V0 \_ TypeGroup1** 類別具有這些屬性。

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，副檔名 ( "IPAddr" ) 
</dt> </dl>

目的地 IP 位址。

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，擴充 ( "Port" ) 
</dt> </dl>

目的地埠號碼。

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 
</dt> </dl>

與要求相關聯之進程的識別碼。

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) ，副檔名 ( "IPAddr" ) 
</dt> </dl>

來源 IP 位址。

</dd> <dt>

{1}size{2}
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 
</dt> </dl>

封包的大小。

</dd> <dt>

運動
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) ，擴充 ( "Port" ) 
</dt> </dl>

來源埠號碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> </dl>

 

 




