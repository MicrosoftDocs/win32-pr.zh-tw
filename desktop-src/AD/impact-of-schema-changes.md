---
title: 架構變更的影響
description: 本主題說明架構延伸如何影響 Active Directory 樹系。
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- 架構變更的影響 AD
- 架構 AD，變更架構的影響
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa9cc0ee4cdcd0da3581d6bf009837799387949e43dc68989612442352df591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187717"
---
# <a name="impact-of-schema-changes"></a>架構變更的影響

架構延伸會影響以數種方式 Active Directory Domain Services 所控制的網域樹系：

-   架構變更是全域的。 整個樹系都有一個架構。 架構會全域複寫：樹系中的每個 DC 上都有架構的複本。 當您擴充架構時，它會針對整個樹系進行延伸。
-   無法反轉架構物件的新增專案。 當新的類別或屬性物件加入至架構時，就無法將它移除。 現有的屬性或類別可以停用，但不能移除。 如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。 停用類別或屬性不會影響現有的類別或屬性實例，但是會防止建立新的實例。 如果屬性包含在未停用的任何類別中，就無法停用屬性。
-   Oid 必須是唯一的。 當屬性或類別加入至架構時，不能加入具有相同 OID 的屬性或類別。 即使已停用類別或屬性，也是如此。 基於這個理由，您必須使用有效的 Oid。 請勿合成 OID，也不會重複使用現有的 OID。 如需取得有效 OID 的詳細資訊，請參閱 [取得根物件識別碼](obtaining-an-object-identifier.md)。
-   建立之後，您可以進行一些變更：

    -   針對類別1或類別2類別，您可以在 **possSuperiors** 屬性中新增或移除值。 **PossSuperiors** 值會指定可包含類別的物件類別。
    -   針對類別1或類別2類別，您可以在 **mayContain** 屬性中新增或移除值。 **MayContain** 值會指定選擇性屬性，但可能存在於類別的實例中。

-   類別2類別或屬性的 **lDAPDisplayName** 在建立之後可以變更。 一般來說，您不應該變更 **lDAPDisplayName**。 不過，變更 LDAP 名稱有一個合法的原因，也就是如果您在定義屬性或類別時犯了錯誤，必須建立一個新的，以取代舊的名稱。 您不需要重新命名屬性或類別架構 (RDN) 的相對辨別名稱即可完成這項作業。 當 LDAP 名稱變更時，這可讓您解決錯誤，而不是重建整個 Windows 2000 基礎結構。 如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。

    預先定義 (類別 1) 類別或屬性的 **lDAPDisplayName** 無法變更。 如需類別1和2架構物件的詳細資訊，請參閱 [架構延伸的限制](restrictions-on-schema-extension.md)。

 

 




