---
title: MicrosoftDNS_WINSRType 類別
description: '\_代表 WINS 反向查閱 (WINSR) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: e611dc63-838f-4a79-baca-febd27612111
keywords:
- MicrosoftDNS_WINSRType 類別 DNS
- MicrosoftDNS_WINSRType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSRType.Modify
- MicrosoftDNS_WINSRType.MappingFlag
- MicrosoftDNS_WINSRType.LookupTimeout
- MicrosoftDNS_WINSRType.CacheTimeout
- MicrosoftDNS_WINSRType.ResultDomain
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89c9545c73a4dbd5a01ff401c7b5587cf448553fcafcf4d698e3aeb17ed8722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912818"
---
# <a name="microsoftdns_winsrtype-class"></a>MicrosoftDNS \_ WINSRType 類別

代表 WINS 反向查閱 (WINSR) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_WINSRType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string ResultDomain;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ WINSRType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ WINSRType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料來具現化 WINSR 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時和要附加的功能變數名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **Modify**                         | 將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                        |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ WINSRType** 類別具有這些屬性。

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用 WINS 查詢的 DNS 伺服器可能會快取 WINS 伺服器的回應時間（以秒為單位）。

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

使用 WINS 反向查閱之 DNS 伺服器的超時時間（以秒為單位）。

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

WINSR 對應旗標，指定是否必須將記錄包含在區域複寫中。 它只能有兩個值：對應于複寫的0x80000000 和0x00010000，以及) 旗標的 (本機記錄。

</dd> <dt>

**ResultDomain**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要附加至所傳回 NetBIOS 名稱的功能變數名稱。

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

[**MicrosoftDNS WINSRType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ WINSRType 類別的方法**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





