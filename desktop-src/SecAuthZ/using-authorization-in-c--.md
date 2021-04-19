---
description: 使用授權管理員 API 來控制對應用程式資源的存取。
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: 在 c + + 中使用授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980568"
---
# <a name="using-authorization-in-c"></a>在 c + + 中使用授權

您可以使用授權管理員 API 來控制對應用程式資源的存取。

如果您有現有的存取控制解決方案，以 (Acl) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 為基礎，而且想要避免將此解決方案轉換為使用授權管理員，您可以繼續使用 acl 來控制資源的存取權。 如需使用 Acl 控制資源存取權的相關資訊，請參閱使用 [c + + 的 acl 來定義許可權](defining-permissions-with-acls-in-c--.md)、在 [c + + 中建立 SID 的用戶端內容](establishing-a-client-context-from-a-sid-in-c--.md)，以及 [使用 c + + 驗證 acl 的用戶端存取](verifying-client-access-with-acls-in-c--.md)。

> [!Note]  
> 針對大型企業，系統管理額外負荷與效能之間會有所取捨。 當安全的資源和使用者數目增加時，Acl 的管理就會變得更複雜。 效能不會受到影響，因為存取權限的所有必要資訊都會散發至安全的資源。 授權管理員的效能會受到調整影響。

 

如需其他授權工作的詳細資訊，請參閱 [在 c + + 中進行授權的支援](supporting-tasks-for-authorization-in-c--.md)工作。



| 主題                                                                                                                | 描述                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [在 c + + 中定義許可權](defining-permissions-in-c--.md)                                                       | 藉由建立授權原則存放區來定義哪些使用者可以存取哪些應用程式資源。 |
| [使用 c + + 確認用戶端對要求的資源的存取](verifying-client-access-to-a-requested-resource-in-c--.md) | 檢查用戶端是否可以存取一或多個作業。                                           |
| [委派 c + + 中的許可權定義](delegating-the-defining-of-permissions-in-c--.md)                   | 將儲存在 Active Directory 中的授權原則存放區委派給管理。          |



 

 

 
