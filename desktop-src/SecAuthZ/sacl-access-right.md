---
description: 存取 \_ 系統 \_ 安全性存取權限可控制在物件安全描述項中取得或設定 SACL 的能力。 如果在 \_ \_ 要求的執行緒的存取權杖中啟用了 SE 安全性名稱許可權，系統就會授與此存取權。
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: SACL 存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780513"
---
# <a name="sacl-access-right"></a>SACL 存取權限

存取 \_ 系統 \_ 安全性存取權限可控制在物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中取得或設定 SACL 的能力。 只有在 \_ \_ 要求的執行緒的 [*存取權杖*](/windows/desktop/SecGloss/a-gly)中啟用了 SE 安全性名稱許可權時，系統才會授與此存取權限。

**存取物件的 SACL**

1.  呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)函數，以啟用 SE 的 \_ 安全性 \_ 名稱許可權。
2.  \_ \_ 當您開啟物件的控制碼時，要求存取系統安全性存取權限。
3.  使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 或 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)等函數來取得或設定物件的 SACL。
4.  呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)以停用 SE \_ 安全性 \_ 名稱許可權。

若要使用 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)或 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)函數存取 SACL，請啟用 SE 的 \_ 安全性 \_ 名稱許可權。 函數會在內部要求存取權限。

存取 \_ 系統 \_ 安全性存取權限在 dacl 中無效，因為 dacl 無法控制 SACL 的存取權。 不過，您可以使用 SACL 中的「存取 \_ 系統安全性」存取權限， \_ 來審查使用存取權限的嘗試。

 

 
