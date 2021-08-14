---
description: 就像系統使用安全描述項來控制安全物件的存取一樣，伺服器也可以使用安全描述項來控制其私用物件的存取權。 如需 Windows 安全性模型的詳細資訊，請參閱存取控制模型。
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: 以 ACL 為基礎的存取控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52867b78114474e1b7827bddf8fd17cd2f3fd71cd88b62cff25397e8bab9b4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785163"
---
# <a name="acl-based-access-control"></a>以 ACL 為基礎的存取控制

就像系統使用 [安全描述項](security-descriptors.md) 來控制安全物件的存取一樣，伺服器也可以使用安全描述項來控制其私用物件的存取權。 如需 Windows 安全性模型的詳細資訊，請參閱[存取控制模型](access-control-model.md)。

受保護的伺服器可以使用 DACL [建立安全描述項](security-descriptors-for-private-objects.md) ，以 [指定各種受](trustees.md)信任者允許的存取類型。 在簡單的情況下，伺服器可以建立單一安全描述項來 [控制所有伺服器資料和功能的存取](checking-access-to-private-objects.md)。 為了提供更精細的保護，伺服器可以為每個私用物件或不同類型的功能建立安全描述項。

例如，當用戶端要求伺服器在資料庫中建立新的物件時，伺服器可以為新的私用物件建立安全描述項。 然後，伺服器可以將安全描述項與私用物件儲存在資料庫中。 當用戶端嘗試存取物件時，伺服器會抓取安全描述項來檢查用戶端的存取權限。 請務必注意，安全描述項中沒有任何相關聯的安全性描述項會將它與所保護的物件或功能產生關聯。 相反地，它是由受保護的伺服器負責維護關聯。

也可以審核私用物件的存取權。 Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.

 

 



