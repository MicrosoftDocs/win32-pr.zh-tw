---
description: 安全描述項包含與安全物件相關聯的安全性資訊。
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: 安全性描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848235"
---
# <a name="security-descriptors"></a>安全性描述項

[*安全描述項*](/windows/desktop/SecGloss/s-gly)包含與安全 [物件](securable-objects.md)相關聯的安全性資訊。 安全描述項是由 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) 結構與其相關聯的安全性資訊所組成。 安全描述項可包含下列安全性資訊：

-   物件的擁有者和主要群組 (Sid) 的[安全識別碼](security-identifiers.md)。
-   [DACL](access-control-lists.md) ，指定允許或拒絕特定使用者或群組的存取權。
-   [SACL](access-control-lists.md) ，指定產生物件之審核記錄的存取嘗試類型。
-   限定安全描述項或其個別成員意義的一組控制位。

應用程式不能直接操作安全描述項的內容。 Windows API 提供的函式可設定和取得物件安全描述項中的安全性資訊。 此外，還有一些函數可用於建立及初始化新物件的安全描述項。

使用 Active Directory 物件上安全描述項的應用程式可以使用 Windows 安全性函式或 Active Directory 服務介面所提供的安全性介面 (ADSI) 。 如需 ADSI 安全性介面的詳細資訊，請參閱 [Active Directory 中的存取控制的運作方式](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services)。

 

 
