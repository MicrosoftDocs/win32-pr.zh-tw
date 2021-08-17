---
description: Active Directory 提供帳戶資料庫，讓金鑰發佈中心 (KDC) 用來取得網域中安全性主體的相關資訊。
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: 帳戶資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141591"
---
# <a name="account-database"></a>帳戶資料庫

Active Directory 提供帳戶資料庫，讓 [*金鑰發佈中心*](/windows/desktop/SecGloss/k-gly) (KDC) 用來取得網域中 [*安全性主體*](/windows/desktop/SecGloss/s-gly) 的相關資訊。 每個主體都是由目錄中的帳戶物件表示。 用來與使用者、電腦或服務通訊的 [*加密*](/windows/desktop/SecGloss/e-gly) 金鑰會儲存為該安全性主體之 account 物件的屬性。

只有網域控制站 Active Directory 伺服器。 每個網域控制站都會保留目錄的可寫入複本，讓您可以在任何網域控制站上建立帳戶、重設密碼，以及修改群組成員資格。 對目錄的一個複本所做的變更會自動傳播至所有其他複本。 Windows 使用專屬的多重主要複寫通訊協定（在複寫協力電腦之間使用安全的遠端程序呼叫連接）複寫 Active Directory 的資訊存放區。 此連接會使用 [*Kerberos 驗證通訊協定*](/windows/desktop/SecGloss/k-gly) 來提供相互 [*驗證*](/windows/desktop/SecGloss/a-gly) 和加密。

帳戶資料的實體儲存體是由 [目錄服務代理程式](/windows/desktop/AD/directory-system-agent)所管理，這是一個受保護的程式，與 [*本地安全性授權*](/windows/desktop/SecGloss/l-gly) 單位整合 (LSA) 在網域控制站上。 目錄服務的用戶端永遠不會獲得資料存放區的直接存取權。 任何需要存取目錄資訊的用戶端都必須連線到目錄服務代理程式，然後搜尋、讀取和寫入目錄物件及其屬性。

存取目錄中物件或屬性的要求，會受到 Windows 存取控制機制的驗證。 和 NTFS 檔案系統中的檔案和資料夾物件一樣，Active Directory 中的物件會受到 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 的保護， (acl) 指定誰可以存取該物件，以及以何種方式存取該物件。 不過，與檔案和資料夾不同的是，Active Directory 物件的每個屬性都有 ACL。 因此，敏感性帳戶資訊的屬性可以受到比授與帳戶其他屬性的限制更多的許可權。

帳戶的最機密資訊當然就是其密碼。 雖然帳戶物件的 [密碼] 屬性會儲存衍生自密碼的加密金鑰，而不是密碼本身，但此金鑰組入侵者來說就很有用。 因此，只有帳戶持有者會授與帳戶物件的 password 屬性存取權，而不會授與其他人（甚至是系統管理員）的存取權。 只有具備受信任運算基礎許可權的進程（在 LSA 的安全性 [*內容*](/windows/desktop/SecGloss/c-gly) 中執行的進程）才能讀取或變更密碼資訊。

若要防止具有網域控制站備份磁帶存取權的人進行離線攻擊，請使用系統金鑰以第二次加密進一步保護帳戶物件的 password 屬性。 此加密金鑰可儲存在卸載式媒體上，因此可以個別保護，也可以儲存在網域控制站上，但受 dispersal 機制保護。 系統管理員可以選擇儲存系統金鑰的位置，以及使用數種演算法來加密密碼屬性。

 

 
