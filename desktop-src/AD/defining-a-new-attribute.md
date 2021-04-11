---
title: 定義新屬性
description: 本主題說明如何在擴充 Active Directory 架構時，定義新的屬性。
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- 定義新的屬性廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092641"
---
# <a name="defining-a-new-attribute"></a>定義新屬性

本主題說明如何在擴充 Active Directory 架構時，定義新的屬性。

在定義新的屬性時，請考慮下列事項：

-   可能的話，請使用現有的屬性。
-   請一律使用 **cn** ( 「一般名稱」 ) 屬性做為命名 (相對分辨名稱) 屬性。 這是大部分類別的預設值，包括直接從頂端衍生的類別。 **Cn** 屬性是已編制索引的屬性，並將依名稱搜尋物件，使其更有效率。
-   大量的多重值屬性在儲存和取得時成本高昂，應予以避免。 Active Directory Domain Services 會執行 LDAP 延伸模組，以啟用具有多個值的大型屬性的累加式讀取，但並非所有 LDAP 用戶端都會辨識此延伸模組。
-   請記住，屬性是平面的，這表示屬性沒有隱含的子結構。 指定類別中的所有屬性都應該直接與該類別的實例相關聯。

## <a name="creating-a-new-attribute"></a>建立新屬性

若要建立新的屬性：

-   選擇屬性的名稱。 名稱將包含在 **cn** 和 **lDAPDisplayName** 屬性中。 如需撰寫新屬性名稱的詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。
-   取得屬性 (OID) 的物件識別碼。 如需詳細資訊，請參閱 [取得根物件識別碼](obtaining-an-object-identifier.md)。
-   選擇屬性的語法。 語法是由 **oMSyntax** 和 **oMObjectClass** 屬性的組合所決定。 如需詳細資訊，請參閱 [選擇語法](choosing-a-syntax.md)。
-   決定屬性是單一或多重值。 **IsSingleValued** 屬性可判斷屬性是單一值或多重值。
-   決定是否應該根據預設來編制屬性的索引。 如需詳細資訊，請參閱 [索引屬性](indexed-attributes.md)。
-   根據預設，決定屬性是否應該在通用類別目錄中。 如需詳細資訊，請參閱 [通用類別目錄中包含的屬性](attributes-included-in-the-global-catalog.md)。
-   如果屬性是整數或字串，請決定是否需要範圍限制。 **RangeLower** 和 **rangeUpper** 屬性是用來指定範圍限制。
-   如果屬性為 DN 值，請決定是否要將屬性與另一個屬性連結。 如果是，則必須在每個屬性上適當設定 [**linkID**](/windows/desktop/ADSchema/a-linkid) 屬性;其中一個屬性必須是轉寄連結，另一個則是上一頁連結。 如需連結屬性的詳細資訊，請參閱 [連結的屬性](linked-attributes.md)。
-   在架構容器中建立新的 **attributeSchema** 物件，並為物件設定適當的屬性。 可以針對 **attributeSchema** 物件設定的屬性有很多，但下表所列的屬性對新屬性的定義而言是不可或缺的。 這些屬性的值取決於先前的步驟。 如需這些屬性的詳細資訊，請參閱 [屬性特性](characteristics-of-attributes.md)。

    | 屬性                                    | 註解                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **cn**<br/>                            | 必要。<br/>                                 |
    | **lDAPDisplayName**<br/>               | 必要。<br/>                                 |
    | **adminDisplayName**<br/>              | 必要。<br/>                                 |
    | **attributeSyntax**<br/>               | 必要。<br/>                                 |
    | **oMSyntax**<br/>                      | 必要。<br/>                                 |
    | **oMObjectClass**<br/>                 | 必要。<br/>                                 |
    | **schemaIDGUID**<br/>                  | 必要。<br/>                                 |
    | **attributeID**<br/>                   | 必要。<br/>                                 |
    | **isSingleValued**<br/>                | 必要。<br/>                                 |
    | **searchFlags**<br/>                   | 必要。<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | 必要。<br/>                                 |
    | **rangeLower**<br/>                    | 選擇性。<br/>                                 |
    | **rangeUpper**<br/>                    | 選擇性。<br/>                                 |
    | **linkID**<br/>                        | 選擇性。 連結屬性的必要參數。<br/> |
    | **description**<br/>                   | 選擇性。<br/>                                 |

    

     

-   將新的 **attributeSchema** 物件認可至架構容器。
-   視需要更新架構快取。 如需詳細資訊，請參閱 [更新架構](updating-the-schema-cache.md)快取。

 

