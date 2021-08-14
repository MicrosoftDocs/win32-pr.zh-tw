---
description: SetNamedSecurityInfo 和 SetSecurityInfo 函式支援將可繼承的存取控制專案自動傳播 (Ace) 。
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: 自動傳播可繼承的 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257c038174549eebb8d960f8f4bc0601f95a928478e2a783f93f4a1444a22d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783715"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>自動傳播可繼承的 Ace

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)和 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)函式支援將可繼承的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)自動傳播 (ace) 。 例如，如果您使用這些函式將可繼承的 ACE 新增至 NTFS 中的目錄，系統會適當地將 ACE 套用至 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) ， (acl) 任何現有的子目錄或檔案。

直接套用的 Ace 優先于繼承的 Ace。 系統會在任意的存取控制清單中將直接套用的 Ace 放在 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 中，以實作為此優先順序。 當您呼叫 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 和 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) 函式來設定物件的安全性資訊時，系統會將目前的繼承模型強加在階層中所有物件的 acl 上（目標物件底下）。 如果物件已轉換為目前的繼承模型，則 \_ \_ \_ \_ \_ \_ 會在物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)的控制項欄位中設定 SE DACL 自動繼承和 SE SACL 自動繼承的位。

當您建立新的安全描述項以反映目前的繼承模型時，請小心不要變更安全描述項的語法。 如此一來，「允許」和「拒絕」 Ace 永遠不會彼此移動。 如果需要這類移動 (例如，將所有 noninherited Ace 放在 ACL) 的前方，ACL 會標示為受保護，以防止語義變更。

將繼承的 Ace 傳播到子物件時，系統會使用下列規則：

-   如果沒有 DACL 的子物件繼承 ACE，則結果會是具有 DACL 的子物件，其中只包含繼承的 ACE。
-   如果具有空白 DACL 的子物件繼承 ACE，則結果會是具有 DACL 的子物件，其中只包含繼承的 ACE。
-   如果您從父物件移除可繼承的 ACE，自動繼承會移除子物件所繼承之任何 ACE 的複本。
-   如果自動繼承會導致從子物件的 DACL 移除所有 Ace，則子物件具有空白的 DACL，而不是 DACL。

這些規則可能會導致無法預期的結果，將沒有 DACL 的物件轉換為具有空白 DACL 的物件。 沒有 DACL 的物件允許完整存取，但是具有空白 DACL 的物件不允許存取。 例如，假設您將可繼承的 ACE 新增至物件樹狀結構的根物件，就可以使用這些規則來建立空白的 DACL。 自動繼承會將可繼承的 ACE 傳播至樹狀結構中的所有物件。 以沒有 DACL 啟動的子物件現在具有繼承 ACE 的 DACL。 如果您從根物件移除可繼承的 ACE，系統會自動將變更傳播到子物件。 啟動但沒有 DACL 的子物件 (允許完整存取) 現在有空白的 DACL (不允許存取) 。

若要確保沒有 DACL 的子物件不會受到可繼承 ace 的影響，請 \_ \_ 在物件的安全描述項中設定 SE dacl 保護旗標。

如需有關如何正確建立 DACL 的詳細資訊，請參閱 [建立 dacl](/windows/desktop/SecBP/creating-a-dacl)。

 

 
