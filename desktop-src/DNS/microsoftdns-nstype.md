---
title: MicrosoftDNS_NSType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (NS) 記錄的名稱伺服器。
ms.assetid: 8d229acd-bc47-4a32-b6f1-b784a48dc91a
keywords:
- MicrosoftDNS_NSType 類別 DNS
- MicrosoftDNS_NSType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
- MicrosoftDNS_NSType.Modify
- MicrosoftDNS_NSType.NSHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07155c36089e60b12aeea214b19cb8aca146005a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935149"
---
# <a name="microsoftdns_nstype-class"></a>MicrosoftDNS \_ NSType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (NS) 記錄的名稱伺服器。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_NSType : MicrosoftDNS_ResourceRecord
{
  string NSHost;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ NSType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ NSType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 DNS NS 資源記錄：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值以及具有網域授權單位的主機。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/> |
| **修改**                         | 將 TTL 和 NS 主機更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/>                               |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ NSType** 類別具有這些屬性。

<dl> <dt>

**NSHost**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網域的授權主機。

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

[**MicrosoftDNS NSType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-nstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ NSType 類別的方法**](microsoftdns-nstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





