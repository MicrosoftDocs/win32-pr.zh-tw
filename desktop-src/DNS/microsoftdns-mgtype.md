---
title: MicrosoftDNS_MGType 類別
description: '\_代表郵件群組 (MG) 記錄的 MicrosoftDNS ResourceRecord 子類別。'
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType 類別 DNS
- MicrosoftDNS_MGType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4a9b1f88a3d7e2752d2e4c199c261b49364ab7bdcbf4543e852f5218111491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692598"
---
# <a name="microsoftdns_mgtype-class"></a>MicrosoftDNS \_ MGType 類別

代表郵件群組 (MG) 記錄的 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 子類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ MGType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ MGType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 這個方法會根據方法的輸入參數中的資料具現化以 MG 類型的 RR：記錄的 DNS 伺服器名稱、容器名稱、郵件群組的擁有者名稱、類別 (預設值 = IN) 、存留時間值和信箱名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **Modify**                         | 這個方法會將 TTL 和 MG 信箱更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ MGType** 類別具有這些屬性。

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

FQDN，指定隸屬于記錄擁有者名稱所指定之郵件群組成員的信箱。

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

[**MicrosoftDNS MGType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ MGType 類別的方法**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





