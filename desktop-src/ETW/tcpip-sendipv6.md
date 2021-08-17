---
description: 此類別是 IPv6 TCP/IP 傳送事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: TcpIp_SendIPV6 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f9314688bce48f48274131a2b1dd605d8a555e3e31c205a67a07d2895e55c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069628"
---
# <a name="tcpip_sendipv6-class"></a>TcpIp \_ SendIPV6 類別

此類別是 IPv6 TCP/IP 傳送事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>成員

**TcpIp \_ SendIPV6** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TcpIp \_ SendIPV6** 類別具有這些屬性。

<dl> <dt>

connid
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (10) ，指標
</dt> </dl>

唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) ，副檔名 ( "IPAddrV6" ) 
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

**endtime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (8) 
</dt> </dl>

結束傳送要求時間。

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

限定詞： WmiDataId (4) ，副檔名 ( "IPAddrV6" ) 
</dt> </dl>

來源 IP 位址。

</dd> <dt>

seqnum
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (9) 
</dt> </dl>

序號。

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

</dd> <dt>

**startime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 
</dt> </dl>

開始傳送要求時間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Tcpip.sys**](tcpip.md)
</dt> </dl>

 

 




