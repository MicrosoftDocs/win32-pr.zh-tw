---
title: 架構介面
description: 架構介面
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- 架構介面 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931831"
---
# <a name="schema-interfaces"></a>架構介面

架構容器包含一組架構定義，這些定義會附加至提供者的命名空間樹狀結構的一部分。 一般而言，命名空間的每個實例都有自己的架構。 例如，在下圖中，ADSI 範例提供者會在每個根節點「西雅圖」和「多倫多」中定義架構容器。

![架構內含專案](images/schemacont.png)

若要建立提供者的 ADSI 執行，您需要提供架構管理物件，以反映提供者的基礎命名空間，並支援 ADSI 架構介面。 以下是包含在架構容器中的 ADSI 架構介面清單。

-   [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 代表目錄服務類別。
-   [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) 代表具有單一或多個值的目錄服務屬性。
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) 代表單一 VARIANT 型別。

ADSI 所定義的介面可以支援提供者的特定屬性和語法。 提供者可以選擇使用建立和存取屬性的方法來擴充 ADSI 定義，例如，您可以使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面的方法，例如 [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get)、 [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex)、 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 和 [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)。 提供者也可以透過其他介面支援其他屬性。 如需 ADSI 介面的完整清單，請參閱 [Adsi 介面](adsi-interfaces.md)。

具有複雜命名空間的 ADSI 提供者元件可能會允許多個架構存在於命名空間實例中，每個都位於樹狀結構的不同部分。 不過，物件的 [**IADs：： Schema**](iads-property-methods.md) 屬性一律會命名它自己的架構定義。

 

 




