---
title: 系結至架構的指導方針
description: 有兩種方式可系結至 Active Directory 架構系結直接系結至架構容器，或系結至架構容器中的 classSchema 或 attributeSchema 物件。
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- 系結至架構 AD 的指導方針
- 架構 AD，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188682"
---
# <a name="guidelines-for-binding-to-the-schema"></a>系結至架構的指導方針

有兩種方式可以系結至 Active Directory 架構：

-   直接系結至架構容器，或系結至架構容器中的 **classSchema** 或 **attributeSchema** 物件。 **ClassSchema** 或 **attributeSchema** 物件包含可存在於 Active Directory 網域樹系中的每個類別和屬性的完整正式定義。 如需詳細資訊，請參閱 [讀取 attributeSchema 和 ClassSchema 物件](reading-attributeschema-and-classschema-objects.md)。
-   系結至抽象架構或抽象架構中的類別或屬性專案。 抽象架構只包含每個類別和屬性的資料子集，但是資料的格式很容易取得和使用。 如需詳細資訊，請參閱 [抽象架構](the-abstract-schema.md) 和 [讀取抽象架構](reading-the-abstract-schema.md)。

若要修改或延伸架構，請直接系結至架構容器。 若要讀取類別和屬性定義，通常可以更輕鬆地從抽象架構中讀取。

基於下列原因，您可以更輕鬆地讀取抽象架構：

-   ADSI 提供特殊的系結技巧，以及一組可讀取抽象架構的介面。
-   使用抽象架構的 ADSI 介面會傳回適當格式的資料，以供其他 ADSI 介面使用。 例如， [**得到 iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) 和 [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) 通常會使用 **lDAPDisplayName** 字串來報告屬性和類別名稱，即使這項資料是以物件識別碼形式儲存在目錄中， (oid) 也是一樣。 **LDAPDisplayName** 格式很方便，因為其他 ADSI 介面會使用它來參考搜尋篩選和其他位置中的類別和屬性。
-   物件類別的抽象架構專案包含從多個 **classSchema** 物件收集而來的資料。 例如，物件類別的可能父系、強制屬性和選擇性屬性，是這些屬性與類別的超類和輔助類別的聯集。 如果您從實際的架構容器讀取，則需要從衍生類別的各種 **classSchema** 物件中收集資料。 如果您是從抽象架構讀取，資料就會在同一個位置。

在下列情況下，您應該直接系結至架構容器，而不是使用抽象架構：

-   取得未在抽象架構中公開的特定屬性。 例如， **oMSyntax**、 **attributeSchema**、 **defaultSecurityDescriptor** 和其他屬性不會在抽象架構中公開。
-   查詢 **attributeSchema** 和 **classSchema** 物件。 若要搜尋符合指定之篩選準則的類別或屬性，請系結至架構容器並執行一層級的搜尋。
-   加入或修改屬性或類別。 抽象架構是唯讀的;您無法使用它來修改或擴充架構。 請注意，必須在架構主機的網域控制站上進行修改。 如需詳細資訊，請參閱 [安裝架構延伸模組的必要條件](prerequisites-for-installing-a-schema-extension.md)。

 

 