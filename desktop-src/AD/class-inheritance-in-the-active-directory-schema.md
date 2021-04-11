---
title: Active Directory 架構中的類別繼承
description: Active Directory 目錄服務架構中的所有物件類別都是衍生自特殊類別 top。
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023282"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Active Directory 架構中的類別繼承

Active Directory 目錄服務架構中的所有物件類別都是衍生自特殊類別 [**top**](/windows/desktop/ADSchema/c-top)。 除了 **top** 之外，所有物件類別都是另一個物件類別的子類別。 例如， [**contact**](/windows/desktop/ADSchema/c-contact) 是 [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)的子類別; **organizationalPerson** 是 [**person**](/windows/desktop/ADSchema/c-person)的子類別; **person** 是 **top** 的子類別。 [**ClassSchema**](/windows/desktop/ADSchema/c-classschema)物件的 [**subClassOf**](/windows/desktop/ADSchema/a-subclassof)屬性是單一值屬性，指出類別的直屬超類別。

某些定義類別的屬性值會繼承自其超類。 因此 [**contact**](/windows/desktop/ADSchema/c-contact) 類別會繼承其超類的值，也就是 [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)、 [**person**](/windows/desktop/ADSchema/c-person)和 [**top**](/windows/desktop/ADSchema/c-top) 類別。 類別會繼承其超類中的下列資料：

-   可能的屬性： [**classSchema**](/windows/desktop/ADSchema/c-classschema)物件的 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain)、 [**mayContain**](/windows/desktop/ADSchema/a-maycontain)、 [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)和 [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain)屬性的值會定義可以在物件類別的實例上設定之屬性的完整清單。 針對每個物件類別，這些屬性的值會包含繼承自其超類的所有值，以及針對物件類別本身明確設定的任何值。 因此， [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)類別的 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain)屬性會包含繼承自 [**person**](/windows/desktop/ADSchema/c-person)和 [**top**](/windows/desktop/ADSchema/c-top)類別的所有 **mustContain** 值，以及在 **organizationalPerson** 類別上明確設定的任何 **mustContain** 值。
-   目錄階層中可能的父系： [**classSchema**](/windows/desktop/ADSchema/c-classschema)物件的 [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors)和 [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors)屬性值會定義可包含物件類別之實例的物件類別完整清單。 針對每個物件類別，值會包含繼承自其超類的值，以及針對物件類別本身明確設定的值。

請注意，物件類別也可以有許多輔助類別，這些類別是在 **classSchema** 物件的 [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass)和 [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass)屬性中指定。 物件類別會繼承其輔助類別中的 [**mustContain**](/windows/desktop/ADSchema/a-mustcontain)、 [**mayContain**](/windows/desktop/ADSchema/a-maycontain)、 [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)和 [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) 值。

 

 