---
title: MicrosoftDNS_RootHints 類別
description: MicrosoftDNS \_ RootHints 類別描述儲存在 DNS 伺服器上的快取檔案中的 RootHints。 此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints 類別 DNS
- MicrosoftDNS_RootHints 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104159"
---
# <a name="microsoftdns_roothints-class"></a>MicrosoftDNS \_ RootHints 類別

**MicrosoftDNS \_ RootHints** 類別描述儲存在 DNS 伺服器上的快取檔案中的 RootHints。 此類別簡化了 DNS 物件的內含專案的視覺化，而不是代表實際的物件。

**MicrosoftDNS \_RootHints** 是 DNS 伺服器在快取檔案中儲存之資源記錄的容器。 **MicrosoftDNS \_ RootHints** 類別的每個實例都必須只指派給一部 DNS 伺服器。 它可能會與多個 [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) 類別的實例相關聯。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ RootHints** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**MicrosoftDNS \_ RootHints** 類別具有這些方法。



| 方法                        | 描述                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | 捕獲區域的分辨名稱。 <br/> 限定詞：實作為<br/>   |
| **WriteBackRootHintDatafile** | 將 RootHints 回寫至 DNS 快取檔案。 <br/> 限定詞：實作為<br/> |



 

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

[**MicrosoftDNS RootHints 類別的 WriteBackRootHintDatafile 方法 \_**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**MicrosoftDNS RootHints 類別的 GetDistinguishedName 方法 \_**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





