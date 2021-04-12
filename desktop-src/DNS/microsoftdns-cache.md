---
title: MicrosoftDNS_Cache 類別
description: MicrosoftDNS \_ cache 類別描述 DNS 伺服器上現有的快取。
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache 類別 DNS
- MicrosoftDNS_Cache 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025106"
---
# <a name="microsoftdns_cache-class"></a>MicrosoftDNS \_ Cache 類別

**MicrosoftDNS \_ cache** 類別描述 DNS 伺服器上現有的快取。 此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。 **MicrosoftDNS \_ Cache** 類別是 DNS 伺服器所快取之資源記錄的容器。 請勿將此與包含根提示的快取檔案混淆。

類別 MicrosoftDNS 快取的 **每 \_** 個實例都必須只指派給一部 DNS 伺服器。 它可能會與多個 [**MicrosoftDNS \_ 網域**](microsoftdns-domain.md) 或 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ Cache** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**MicrosoftDNS \_ Cache** 類別有這些方法。



| 方法                   | 描述                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | 清除資源記錄的 DNS 伺服器快取。 <br/> 限定詞：實作為<br/> |
| **GetDistinguishedName** | 捕獲區域的分辨名稱。 <br/> 限定詞：實作為<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS \_ 網域**](microsoftdns-domain.md)
</dt> <dt>

[**MicrosoftDNS Cache 類別的 ClearCache 方法 \_**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**MicrosoftDNS Cache 類別的 GetDistinguishedName 方法 \_**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





