---
description: 使用 GetSecurityInfo 和 GetNamedSecurityInfo 函式，以取得物件安全描述項的指標。
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: 安全描述項作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5574a504468a4f4bb7dc14effe1f4717d695846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113789"
---
# <a name="security-descriptor-operations"></a>安全描述項作業

Windows API 提供的函式可用來取得和設定與安全物件相關聯之 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 的元件。 使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 和 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 函式，以取得物件安全描述項的指標。 這些函式也可以取得安全描述項之個別元件的指標： DACL、SACL、擁有者 SID 和主要群組 SID。 您可以使用 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) 和 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數來設定物件安全描述項的元件。

一般情況下，您應該使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 和 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) 搭配控制碼所識別的物件，並使用名稱所識別的物件 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 和 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 。 如需使用各種物件類型時所要使用之特定函式的詳細資訊，請參閱 [安全物件](securable-objects.md)。

Windows API 提供其他函式來操作安全描述項的元件。 如需使用 (Dacl 或 Sacl) 之存取控制清單的詳細資訊，請參閱 [從 Acl 取得資訊](getting-information-from-an-acl.md) 和 [建立或修改 acl](creating-or-modifying-an-acl.md)。 如需 Sid 的詳細資訊，請參閱 (Sid) 的 [安全性識別碼](security-identifiers.md) 。

若要取得安全描述項中的控制項資訊，請呼叫 [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) 函數。 若要設定與自動 ACE 繼承相關的控制項位，請呼叫 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函數。 其他控制位是由設定安全描述項元件的各種函數所設定。 例如，如果您使用 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) 來變更物件的 DACL，則函式會適當地設定或清除位，以指出安全描述項是否具有 DACL、是否為預設的 dacl 等等。 另一個範例是 [*資源管理員*](/windows/desktop/SecGloss/r-gly) (RM) 控制位包含在安全描述項中。 系統會根據資源管理員的執行來使用這些位，而且會透過 [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) 和 [**SetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol) 函數來存取。

 

 
