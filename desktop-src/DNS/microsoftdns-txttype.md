---
title: MicrosoftDNS_TXTType 類別
description: '\_代表文字 (TXT) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- MicrosoftDNS_TXTType 類別 DNS
- MicrosoftDNS_TXTType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969201"
---
# <a name="microsoftdns_txttype-class"></a>MicrosoftDNS \_ TXTType 類別

代表文字 (TXT) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ TXTType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ TXTType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 TXT 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及記錄的文字。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/>        |
| **修改**                         | 將 TTL 和描述性文字更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/> |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ TXTType** 類別具有這些屬性。

<dl> <dt>

**DescriptiveText**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述性文字，相依于擁有者網域的語法。

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

[**MicrosoftDNS TXTType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ TXTType 類別的方法**](microsoftdns-txttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





