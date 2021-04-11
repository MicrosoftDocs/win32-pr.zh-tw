---
description: 使用低層級的函式來建立存取控制清單 (ACL) 、配置 ACL 的緩衝區，然後藉由呼叫 InitializeAcl 函數將它初始化。
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: 低層級 ACL 和 ACE 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851688"
---
# <a name="low-level-acl-and-ace-functions"></a>低層級 ACL 和 ACE 函式

若要使用低層級函式來建立 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) (acl) ，請配置 acl 的緩衝區，然後藉由呼叫 [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) 函式將它初始化。 若要將 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 加入 (ace) 至 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 的結尾 (DACL) ，請使用 [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) 和 [**AddAccessDeniedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) 函數。 [**AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace)函式會將 ACE 新增至 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)的結尾， (SACL) 。 您可以使用 [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) 函式，在 ACL 中的指定位置新增一或多個 ace。 **AddAce** 函式也可讓您將可繼承的 ACE 新增至 ACL。 [**DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace)函式會從 ACL 中指定的位置移除 ACE。 [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace)函式會從 ACL 中指定的位置抓取 ACE。 [**FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace)函式會捕獲 ACL 中第一個可用位元組的指標。

若要修改物件 [*安全描述項*](/windows/desktop/SecGloss/s-gly)中的現有 acl，請使用 [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) 或 [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) 函數來取得現有的 acl。 您可以使用 [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) 函數，從現有的 ACL 複製 ace。 配置並初始化新的 ACL 之後，請使用 [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) 和 [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) 之類的函式來新增 ace。 當您完成建立新的 ACL 時，請使用 [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) 或 [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) 函數將新的 acl 新增至物件的安全描述項。

您可以使用 [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace)、 [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)或 [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) 函式，將 [特定物件的 ace](object-specific-aces.md) 新增至 ACL 的結尾。

 

 
