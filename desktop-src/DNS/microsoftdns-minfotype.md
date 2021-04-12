---
title: MicrosoftDNS_MINFOType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (MINFO) 記錄的郵件資訊。
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- MicrosoftDNS_MINFOType 類別 DNS
- MicrosoftDNS_MINFOType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105936"
---
# <a name="microsoftdns_minfotype-class"></a>MicrosoftDNS \_ MINFOType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (MINFO) 記錄的郵件資訊。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ MINFOType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ MINFOType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 MINFO 類型的 RR：記錄的 DNS 伺服器名稱、功能變數名稱、郵寄清單/box 的擁有者名稱、類別 (預設值 =) 、存留時間值以及負責任和錯誤信箱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 這個方法會將 TTL、負責任的信箱和錯誤信箱更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>    |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ MINFOType** 類別具有這些屬性。

<dl> <dt>

**ErrorMailbox**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

FQDN，指定信箱以接收與郵寄清單相關的錯誤訊息，或 MINFO 記錄的擁有者名稱所指定的信箱。

</dd> <dt>

**ResponsibleMailbox**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

FQDN，指定負責記錄的擁有者名稱中所指定之郵寄清單或信箱的信箱。

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

[**MicrosoftDNS MINFOType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ MINFOType 類別的方法**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





