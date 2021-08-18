---
title: 命名屬性和類別
description: 本主題包含命名屬性和類別的指導方針。
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- 命名屬性和類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e042decaf7d3dd15606ea7e138d9e6315d4200f2a641c10381951f2657a5aafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185995"
---
# <a name="naming-attributes-and-classes"></a>命名屬性和類別

本主題包含命名屬性和類別的指導方針。

若要建立新的類別或屬性，請遵循下列命名規則：

-   新 **attributeSchema** 或 **classSchema** 物件的 **cn** 和 **lDAPDisplayName** 屬性都使用相同的名稱。
-   在名稱的第一個區段中，識別具有小寫前置詞的公司。 這個前置詞可以是 DNS 名稱、縮略字或可唯一識別該公司的其他字串。 前置詞可確保在流覽架構時，會連續顯示特定公司的所有屬性和類別。
-   如果您要將架構延伸開發為獨立軟體廠商，請新增前置詞的產品名稱縮寫。 這會增加多個包含 LDAP 架構延伸的產品之間的差異。
-   使用連字號作為前置詞後面的下一個字元。
-   在連字號之後的公司屬性中，指定唯一的屬性或類別名稱。 一般名稱的這個部分應該是描述性的。 請勿使用對架構開發人員和檢視器沒有意義的顯得不合理名稱。

例如，假設虛構的 Fabrikam 公司藉由新增用來儲存語音信箱識別碼的屬性來延伸架構，則新屬性的 **cn** 和 **lDAPDisplayName** 可能是 "Fabrikam-VoiceMailID"。

如果未指定屬性或類別的 **lDAPDisplayName** ，系統會使用 **cn** 來產生一或多個。 不過，產生名稱的系統演算法可能會導致名稱衝突或難以讀取的名稱。 若要避免這些問題，建議您為所有屬性和類別明確指定 **lDAPDisplayName** 。

針對開發和測試目的，您可能會想要將版本尾碼附加到 **cn** 和 **lDAPDisplayName**，例如 "fabrikam-VoiceMailID-001"。 在分散式開發/測試環境中，版本尾碼可讓開發人員同時執行其軟體的多個版本。 測試完成之後，請重新命名屬性或類別以移除尾碼。

您無法刪除架構延伸模組的無用版本，但可以將其停用，然後以隱匿的名稱重新命名。 如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。

 

 




