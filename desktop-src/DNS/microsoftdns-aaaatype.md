---
title: MicrosoftDNS_AAAAType 類別
description: '\_代表 IPv6 位址 (AAAA) 記錄的 MicrosoftDNS ResourceRecord 子類別。 AAAA 記錄通常會發音為 0034; 四-a 記錄 \ 0034;。'
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType 類別 DNS
- MicrosoftDNS_AAAAType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90628ba4ceedffe9628aca0b96b624377ae7a8ab2351cfe6ae6b43ba8a381235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587568"
---
# <a name="microsoftdns_aaaatype-class"></a>MicrosoftDNS \_ AAAAType 類別

代表 IPv6 位址 (AAAA) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。 AAAA 記錄通常會發音為「四 a 記錄」。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ AAAAType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ AAAAType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料來具現化 ' AAAA ' 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/主機名稱、類別 (預設值 = IN) 、存留時間值和 IPv6 位址。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **Modify**                         | 將 TTL 和 IPv6 位址更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>      |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ AAAAType** 類別具有這些屬性。

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

主機的 IPv6 位址。

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

[**MicrosoftDNS AAAAType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ AAAAType 類別的方法**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





