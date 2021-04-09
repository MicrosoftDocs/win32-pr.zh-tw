---
title: MicrosoftDNS_RTType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示透過 (RT) 記錄的路由。
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType 類別 DNS
- MicrosoftDNS_RTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934527"
---
# <a name="microsoftdns_rttype-class"></a>MicrosoftDNS \_ RTType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示透過 (RT) 記錄的路由。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ RTType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ RTType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 RT 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者/主機名稱、類別 (預設值 = IN) 、存留時間值、記錄喜好設定和轉送主機名。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 將 TTL、喜好設定和轉送主機更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>        |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ RTType** 類別具有這些屬性。

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

FQDN，指定主機做為中繼，以達到擁有者指定的主機。

</dd> <dt>

**偏好**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在相同擁有者的其他專案中提供給此 RR 的喜好設定。 偏好較低的值。

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

[**MicrosoftDNS RTType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ RTType 類別的方法**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





