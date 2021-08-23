---
title: 架構執行
description: 在 Active Directory Domain Services 中，類別和屬性定義會分別儲存在目錄中，做為 classSchema 和 attributeSchema 類別的實例。
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025016"
---
# <a name="schema-implementation"></a>架構執行

在 Active Directory Domain Services 中，類別和屬性定義會分別儲存在目錄中，做為 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 和 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 類別的實例。 **classSchema** 和 **attributeSchema** 是架構中定義的類別。 若要操作 Active Directory 架構，請使用用來操作其他物件的相同 LDAP 作業。 因為架構是影響整個樹系之目錄的重要部分，所以會將特殊限制套用至架構延伸。 如需有關限制的詳細資訊，請參閱 [架構延伸的限制](restrictions-on-schema-extension.md)。

若要摘要架構的執行：

-   [**ClassSchema**](/windows/desktop/ADSchema/c-classschema)類別的實例會定義 Active Directory Domain Services 所支援的每個物件類別。 **ClassSchema** 物件的屬性（例如，其 [**mayContain**](/windows/desktop/ADSchema/a-maycontain)和 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain)屬性）描述物件類別，方式與使用者物件的屬性（例如，其 [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)和 [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)屬性）描述該使用者的方式相同。 如需詳細資訊，請參閱 [物件類別的特性](characteristics-of-object-classes.md)。
-   [**AttributeSchema**](/windows/desktop/ADSchema/c-attributeschema)類別的實例是用來定義 Active Directory Domain Services 所支援的每個屬性。 **AttributeSchema** 物件的屬性，例如其 **attributeSyntax** 和 **isSingleValued** 屬性、描述屬性，與使用者物件的屬性描述該使用者的方式相同。 如需詳細資訊，請參閱 [屬性的特性](characteristics-of-attributes.md)。
-   [**AttributeSchema**](/windows/desktop/ADSchema/c-attributeschema)和 [**classSchema**](/windows/desktop/ADSchema/c-classschema)類別的實例會儲存在目錄的已知位置，也就是架構容器。 架構容器一律具有下列格式的辨別名稱：

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    其中 " &lt; dc = forestroot &gt; " 是樹系根的辨別名稱，例如 "Dc = FABRIKAM，DC = Com"。

    若要取得架構容器的辨別名稱，請讀取 rootDSE 的 **schemaNamingCoNtext** 屬性。 如需 rootDSE 及其屬性的詳細資訊，請參閱 [無伺服器系結和 rootdse](serverless-binding-and-rootdse.md)。

考慮架構時，請記住：

-   架構變更是全域的。 整個樹系都有一個架構。 架構會進行全域複寫：樹系中的每個網域控制站上都有架構的複本。 當您擴充架構時，您可以為整個樹系進行此作業。
-   無法還原架構新增專案。 當新的類別或屬性加入至架構時，就無法將它移除。 現有的屬性或類別可以停用，但不能移除。 如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。
-   停用類別或屬性不會影響現有的類別或屬性實例，但是會防止建立新的實例。 如果屬性包含在未停用的任何類別中，就無法停用屬性。

 

 