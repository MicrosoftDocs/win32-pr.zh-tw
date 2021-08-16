---
title: MicrosoftDNS_ResourceRecord 類別
description: MicrosoftDNS \_ ResourceRecord 類別代表 DNS RR 的一般屬性。以下是從 MOF 程式碼簡化的語法。
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord 類別 DNS
- MicrosoftDNS_ResourceRecord 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874798"
---
# <a name="microsoftdns_resourcerecord-class"></a>MicrosoftDNS \_ ResourceRecord 類別

**MicrosoftDNS \_ ResourceRecord** 類別代表 DNS RR 的一般屬性。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ ResourceRecord** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ ResourceRecord** 類別具有這些方法。



| 方法                                   | 描述                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | 剖析 TextRepresentation 字串中的 RR，以及輸入 DNS 伺服器和容器名稱、定義和具現化 ResourceRecord 物件。 方法會將新物件的參考傳回做為輸出參數。 <br/> 限定詞︰無<br/> |
| **GetObjectByTextRepresentation**        | 抓取 MicrosoftDns ResourceRecord 子類別的現有實例 \_ ，並以 TextRepresentation 字串和 DNS 伺服器和容器名稱表示。 <br/> 限定詞︰無<br/>                                                        |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ ResourceRecord** 類別具有這些屬性。

<dl> <dt>

**容器**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出包含 RR 之區域、快取或 RootHints 實例的容器名稱。

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出包含 RR 之 DNS 伺服器的 FQDN 或 IP 位址。

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

代表包含 RR 之網域的 FQDN。 這個屬性可能包含字串 \\ 。Cache \\ 或 \\ .。。RootHints \\ ，如果內部快取或 RootHints 分別包含 RR。

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RR 的擁有者名稱。

</dd> <dt>

**RecordClass = 1**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

* * Windows Server 2003： * *

這個字串代表資源記錄的類別。 有效值包括：

1：在 (網際網路) 

2： CS (CSNET) 

3： CH (混亂) 

4： HS (Hesiod) 

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源記錄資料。

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

整個 RR 的文字標記法。

</dd> <dt>

**時間 戳**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次重新整理 RR 的時間，以1601年1月1日起的經過時程表示，格林尼治平均時間 (GMT) 。

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

DNS [*解析程式*](r-gly.md)可以快取 RR 的時間（以秒為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS ResourceRecord 類別的 CreateInstanceFromTextRepresentation 方法 \_**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**MicrosoftDNS ResourceRecord 類別的 GetObjectByTextRepresentation 方法 \_**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





