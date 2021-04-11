---
title: MicrosoftDNS_MFType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，代表網域 (MF) 記錄的郵件轉送代理程式。
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- MicrosoftDNS_MFType 類別 DNS
- MicrosoftDNS_MFType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104741"
---
# <a name="microsoftdns_mftype-class"></a>MicrosoftDNS \_ MFType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，代表網域 (MF) 記錄的郵件轉送代理程式。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ MFType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ MFType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 這個方法會根據方法的輸入參數中的資料具現化 MF 的 MF 類型：記錄的 DNS 伺服器名稱、網域的擁有者名稱、類別 (預設值 = IN) 、存留時間值和郵件代理程式的主機。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 這個方法會將 TTL 和 MF 主機更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                         |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ MFType** 類別具有這些屬性。

<dl> <dt>

**MFHost**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

FQDN 指定具有郵件代理程式的主機，該主機將接受郵件轉送至指定的網域。

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

[**MicrosoftDNS MFType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ MFType 類別的方法**](microsoftdns-mftype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





