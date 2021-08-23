---
title: MicrosoftDNS_CNAMEType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (CNAME) 記錄的標準名稱。
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType 類別 DNS
- MicrosoftDNS_CNAMEType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e819380726fb311d3e892ff3ae1610890f87330cc3d15ac7e9459985aa775354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076842"
---
# <a name="microsoftdns_cnametype-class"></a>MicrosoftDNS \_ CNAMEType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (CNAME) 記錄的標準名稱。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ CNAMEType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ CNAMEType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 CNAME 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 CNAME 記錄的主要名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **Modify**                         | 將 TTL 和主要名稱更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                        |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ CNAMEType** 類別具有這些屬性。

<dl> <dt>

**PrimaryName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

CNAME 記錄擁有者的標準或主要名稱。

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

[**MicrosoftDNS CNAMEType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ CNAMEType 類別的方法**](microsoftdns-cnametype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





