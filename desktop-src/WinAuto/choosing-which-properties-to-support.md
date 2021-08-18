---
title: 選擇要支援的屬性
description: IAccessible 屬性可讓伺服器開發人員描述各種不同的使用者介面元素。
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133961"
---
# <a name="choosing-which-properties-to-support"></a>選擇要支援的屬性

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性可讓伺服器開發人員描述各種不同的使用者介面元素。 但並非所有屬性都適用于每種使用者介面元素。 此外，有些屬性會提供實用但不重要的描述性資訊。

伺服器必須針對每個物件支援下列屬性和方法：

-   [**名稱**](name-property.md)
-   [**角色**](role-property.md)
-   [**狀態**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)和 [ **IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)和 [ **IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

如果下列屬性和方法適用于物件，則必須加以支援：

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**值**](value-property.md)

如果物件有子系，則必須支援下列屬性和方法：

-   [**子**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)系和 [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**焦點、選取專案**](selection-and-focus-properties-and-methods.md)和 [ **IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

下列屬性是選擇性的，但提供物件的實用描述性資訊。 會執行 [**Description**](description-property.md) 屬性來描述點陣圖和其他影像。

-   [**描述**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md)和 [ **IAccessible：： accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**説明**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




