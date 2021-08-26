---
title: MicrosoftDNS_ISDNType 類別
description: 代表 ISDN 記錄之 MicrosoftDNS ResourceRecord 的子類別 \_ 。
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType 類別 DNS
- MicrosoftDNS_ISDNType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af06ad782b6d36213e9a1df210916f9346e1e4f8bd0a98dd619651a579dc5c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131718"
---
# <a name="microsoftdns_isdntype-class"></a>MicrosoftDNS \_ ISDNType 類別

代表 ISDN 記錄之 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 的子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ ISDNType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ ISDNType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 ISDN 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及擁有者的 ISDN 號碼和子位址。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **Modify**                         | 將 TTL、ISDN 號碼和子位址更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                   |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ ISDNType** 類別具有這些屬性。

<dl> <dt>

**ISDNNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

記錄擁有者的 ISDN 號碼和 DDI。

</dd> <dt>

**首先**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

擁有者的子位址（若已定義）。

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

[**MicrosoftDNS ISDNType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ ISDNType 類別的方法**](microsoftdns-isdntype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





