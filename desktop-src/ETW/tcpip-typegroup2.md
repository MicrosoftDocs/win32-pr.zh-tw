---
description: 此類別是 IPv4 TCP/IP 連接和接受事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 316daec5b6bb186756f8597a63ee35d18125181b6575ae24c8ba8fae63f53d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814498"
---
# <a name="tcpip_typegroup2-class"></a>TcpIp \_ TypeGroup2 類別

此類別是 IPv4 TCP/IP 連接和接受事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>成員

**TcpIp \_ TypeGroup2** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TcpIp \_ TypeGroup2** 類別具有這些屬性。

<dl> <dt>

**connid**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (15)**， **指標**
</dt> </dl>

唯一的連接識別碼，可讓屬於相同連接的事件相互關聯。

</dd> <dt>

**daddr**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (3)**， **副檔名 ( "IPAddrV4" )**
</dt> </dl>

目的地 IP 位址。

</dd> <dt>

**dport**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (5)**， **擴充 ( "Port" )**
</dt> </dl>

目的地埠號碼。

</dd> <dt>

**Mss**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (7)**
</dt> </dl>

區段大小上限。

</dd> <dt>

**PID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (1)**
</dt> </dl>

與要求相關聯之進程的識別碼。

</dd> <dt>

**rcvwin**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (11)**
</dt> </dl>

TCP 接收視窗大小。

</dd> <dt>

**rcvwinscale**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (12)**
</dt> </dl>

TCP 接收視窗調整係數。

</dd> <dt>

**sackopt**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (8)**
</dt> </dl>

TCP 標頭中的選擇性確認 (SACK) 選項。

</dd> <dt>

**saddr**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (4)**， **副檔名 ( "IPAddrV4" )**
</dt> </dl>

來源 IP 位址。

</dd> <dt>

**seqnum**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (14)**
</dt> </dl>

序號。

</dd> <dt>

**size**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (2)**
</dt> </dl>

封包的大小。

</dd> <dt>

**sndwinscale**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (13)**
</dt> </dl>

TCP 傳送視窗調整係數。

</dd> <dt>

**運動**
</dt> <dd> <dl> <dt>

資料類型： **物件**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (6)**， **擴充 ( "Port" )**
</dt> </dl>

來源埠號碼。

</dd> <dt>

**tsopt**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (9)**
</dt> </dl>

TCP 標頭中的時間戳記選項。

</dd> <dt>

**wsopt**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId (10)**
</dt> </dl>

TCP 標頭中的視窗調整選項。

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

 

 




