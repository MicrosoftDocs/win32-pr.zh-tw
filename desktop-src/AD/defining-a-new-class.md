---
title: 定義新的類別
description: 當您定義新的類別時，請指定新類別的合法父類別，也就是可以包含新類別實例的類別。
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931900"
---
# <a name="defining-a-new-class"></a>定義新的類別

當您定義新的類別時，請指定新類別的合法父類別，也就是可以包含新類別實例的類別。 合法的父類別是在新類別的 **possSuperiors** 和 **systemPossSuperiors** 屬性中指定，也會在繼承自其超類的可能 superiors 中指定，但不能從輔助類別繼承。

在定義新類別的合法父類別時，請務必指定。 決定您要讓使用者建立類別實例的位置。 例如，指定 "container" 作為合法父系將可讓使用者在任何標準容器（ (**container**、 **organizationalUnit** 等）下建立實例，而) 在指定 "computer" 時，會讓實例只在 **電腦** 物件的實例底下建立。

**建立類別**

1.  選擇類別的名稱。 如需撰寫新類別的通用名稱和 LDAP 顯示名稱的詳細資訊，請參閱 [命名屬性和類別](naming-attributes-and-classes.md)。
2.  取得類別 (OID) 的物件識別碼。 如需詳細資訊，請參閱 [取得物件識別碼](obtaining-an-object-identifier.md)。
3.  選擇類別的 [預設物件類別]。 如需詳細資訊，請參閱 [物件類別和物件類別](object-class-and-object-category.md)。
4.  選擇類別的 [物件類別類別目錄]。 這會指出類別是抽象、結構化或輔助。 如需詳細資訊，請參閱 [結構化、抽象概念和輔助類別](structural-abstract-and-auxiliary-classes.md)。
5.  建立新的 **classSchema** 物件。 您可以針對 **classSchema** 物件設定許多屬性。 下列屬性對於新類別的定義而言是不可或缺的：

    -   新類別所繼承的類別： **subClassOf**、 **auxiliaryClass** 和 **systemAuxiliaryClass**
    -   新類別的名稱和識別碼： **cn**、 **lDAPDisplayName**、 **adminDisplayName**、 **schemaIDGUID**、 **governsID**
    -   新類別的可能屬性： **mustContain**、 **systemMustContain**、 **mayContain**、 **systemMayContain**
    -   新類別的可能父系： **possSuperiors**、 **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **描述** (選擇性) 

    如需詳細資訊以及這些屬性的說明，請參閱 [物件類別的特性](characteristics-of-object-classes.md)。

    請注意，當新類別寫入目錄時， **subClassOf**、 **possSuperiors**、 **systemPossSuperiors**、 **auxiliaryClass** 和 **systemAuxiliaryClass** 中指定的類別必須存在;否則， **classSchema** 物件將無法新增至目錄。 同樣地， **mustContain**、 **systemMustContain**、 **mayContain** 和 **systemMayContain** 中指定的屬性必須存在，否則類別建立作業將會失敗。

6.  將新的 **classSchema** 物件寫入目錄。

**將屬性加入至 mayContain 屬性**

1.  取得要修改之類別的 **classSchema** 物件。
2.  將新屬性新增至 **mayContain** 多重值屬性。
3.  將已變更的 **classSchema** 物件寫回目錄。

新的屬性可以和新的類別同時建立;建立新屬性和類別的順序很重要。 如需詳細資訊，請參閱 [安裝的功能](what-the-installation-must-do.md)。

**同時加入新的屬性和新的類別**

1.  先定義所有的新屬性。 如需詳細資訊，請參閱 [定義新屬性](defining-a-new-attribute.md)。
2.  在定義任何新的類別之前，請先更新架構快取。 如需詳細資訊，請參閱 [更新架構](updating-the-schema-cache.md)快取。
3.  建立新的類別。
4.  將所需的屬性新增至新的類別。
5.  重新更新架構快取。

 

 




