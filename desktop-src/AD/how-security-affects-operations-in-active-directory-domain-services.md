---
title: 安全性如何影響 Active Directory Domain Services 中的作業
description: Active Directory Domain Services 根據執行存取嘗試的使用者身分識別，使用存取控制來授與或拒絕物件、屬性和作業的存取權。
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory 中的安全性效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839307"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>安全性如何影響 Active Directory Domain Services 中的作業

Active Directory Domain Services 根據執行存取嘗試的使用者身分識別，使用存取控制來授與或拒絕物件、屬性和作業的存取權。 當您的應用程式系結至目錄時，它會系結至特定的使用者認證。 經過驗證後，這些認證會決定您應用程式的安全性內容。 無論認證是登入的使用者、指定的使用者、服務帳戶、電腦帳戶或未驗證的使用者 (Guest/Everyone) ，Active Directory 伺服器都會先確認使用者存取物件的許可權，然後再對該物件執行任何操作。 使用者不一定可以存取特定物件、其子系、屬性或該物件上的作業，這表示您的應用程式必須處理拒絕存取所造成的潛在錯誤。

如需有關各種作業的安全性內容和存取控制影響的詳細資訊，請參閱：

-   [存取控制和讀取作業](access-control-and-read-operations.md)
-   [存取控制和寫入作業](access-control-and-write-operations.md)
-   [存取控制和物件建立](access-control-and-object-creation.md)
-   [存取控制和物件刪除](access-control-and-object-deletion.md)

 

 




