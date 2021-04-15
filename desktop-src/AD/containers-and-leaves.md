---
title: 容器和離開
description: Active Directory Domain Services 包含物件的階層，其中的所有物件實例（目錄階層的根目錄除外）都包含在其他物件中。
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- 容器和離開 Active Directory
- 分葉 Active Directory
- 容器 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462909"
---
# <a name="containers-and-leaves"></a>容器和離開

Active Directory Domain Services 包含物件的階層，其中的所有物件實例（目錄階層的根目錄除外）都包含在其他物件中。 此階層的結構比目錄和檔案的檔案系統更有彈性。 相反地， [Active Directory 架構](active-directory-schema.md)中的規則會決定哪些物件類別可以包含其他物件類別的實例。 例如， [**User**](/windows/desktop/ADSchema/c-user) 物件類別的預設架構定義包含 [**組織單位**](/windows/desktop/ADSchema/c-organizationalunit) 和 [**容器**](/windows/desktop/ADSchema/c-container) 物件類別，可能是 superiors;也就是 **使用者** 物件實例的可能父物件或容器。 這表示 **組織單位** 物件可以包含 **使用者** 物件，但除非 **使用者** 類別的架構定義變更，否則 **使用者** 物件不能包含另一個 **使用者** 物件。

除了架構物件（也就是定義可存在於伺服器樹系中的類別和屬性的 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 或 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件）之外，Active Directory Domain Services 中的任何物件都可以是容器。 具體而言，在物件類別定義的 [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) 或 [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) 屬性中出現的任何物件類別，都可能是容器。 如需預先定義之物件類別之容器的詳細資訊，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)。 您可以用程式設計方式系結至抽象架構，並使用 [**得到 iadsclass \_ ：： get**](/windows/desktop/api/iads/nn-iads-iadsclass) 內含專案或 [**得到 iadsclass：： get \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) 方法來取得指定類別可以包含或包含的類別。 如需詳細資訊，請參閱 [讀取抽象架構](reading-the-abstract-schema.md)。 您也可以讀取任何物件實例的 [**possibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) 屬性，以判斷物件可以包含的物件類別。 請注意， **possibleInferiors** 是一個結構化屬性，這表示它是從其他類別定義的 **possSuperiors** / **systemPossSuperiors** 值計算而來，而且實際上不會儲存在目錄中。

請注意，Active Directory 架構會定義一個 [**容器**](/windows/desktop/ADSchema/c-container) 類別。 如先前所討論，物件不需要是 **容器** 類別的實例，就是容器。 此外，也有分 [**葉**](/windows/desktop/ADSchema/c-leaf) 類別，雖然這個類別的子類別通常不是容器，但是沒有原因。

最後，您可以在與物件類別相關聯的顯示規範上設定旗標，以指出使用者介面應該一律將類別的實例顯示為「離開」而不是容器。 這有助於防止使用者介面因為太多容器而變得雜亂。 如需詳細資訊，請參閱將 [容器當作分葉節點來查看](viewing-containers-as-leaf-nodes.md)。

 

 