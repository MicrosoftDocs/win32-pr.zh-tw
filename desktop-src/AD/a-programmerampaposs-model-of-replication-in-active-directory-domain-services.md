---
title: 程式設計人員在 Active Directory Domain Services 中的複寫模型
description: 以下是 Active Directory Domain Services 的複寫模型描述。
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- 程式設計師的 Active Directory 複寫 AD 模型
- 程式設計人員在 Active Directory Domain Services 中的複寫模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b758a31913d0c306105d0d3ce51e72607530e314d79601e8e5230495458d9793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841228"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>程式設計人員在 Active Directory Domain Services 中的複寫模型

以下是 Active Directory Domain Services 的複寫模型描述。

Active Directory 網網域控制站 (DC) 的所有更新都會使用 LDAP 要求來執行，以針對每個要求建立、修改或刪除一個物件。 單一要求可以設定或修改物件上的多個屬性。

更新要求會在某個 DC 上以不可部分完成的交易形式處理。 發生整個更新或不執行任何動作。 如果要求者收到更新要求的成功回應，則表示整個要求已成功 (認可) 。 這稱為「原始寫入」。 多個 LDAP 要求無法分組為一個較大的交易。

在原始寫入中，DC 會針對每個新的或已修改的屬性值計算「戳記」，並將此戳記附加至值，因此當複寫值時，戳記也會進行複寫。 新的戳記是唯一的，而且在更新時，新的戳記會大於該 DC 上舊值的戳記。

在此情況下，DC 會選取上次執行複寫之後變更的物件集合。 然後，針對每個物件，它會將單一訊息傳送至所有其他 Dc，其中包含自上次複寫物件之後變更的所有屬性值。 複寫訊息是可靠的，並且會依序傳遞，但可能需要更多時間才能傳遞。

當某個 DC 接收來自另一個 DC 的複寫訊息時，它會依照下列方式處理它：針對每個修改的屬性，如果複寫訊息中值的戳記大於目前值的戳記，則 DC 會套用更新;否則 DC 會捨棄更新。 每個複寫訊息都會套用為不可部分完成的交易，就像原始寫入一樣。

這是 Active Directory Domain Services 複寫模型。 此模型的重要屬性包括：

-   單一物件的原始寫入是不可部分完成的。
-   複寫變更時，會傳送原始寫入所做的所有變更，或不是任何變更。
-   單一物件的複寫寫入是不可部分完成的，但衝突則是依屬性解析。

模型不保證對不同物件所做之變更的複寫順序。 請勿撰寫採用原始寫入順序來複寫變更的應用程式。 模型不保證如果物件的屬性變更兩次，則會複寫兩個值;複寫時只會傳送目前的值。

這種模型與現實的不同之處在于，它只會影響效能。 例如，Active Directory 伺服器會將包含變更的複寫訊息傳送至多個物件，但會處理這類多物件訊息的內容，就像是一系列的單一物件訊息一樣。 Active Directory 伺服器不會執行模型中所述的點對點複寫，而是會執行功能相當於模型的更複雜且更有效率的可轉移複寫。

 

 




