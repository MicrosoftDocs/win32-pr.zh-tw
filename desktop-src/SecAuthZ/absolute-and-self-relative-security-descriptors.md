---
description: 若要判斷安全描述項是否為自我或絕對安全描述項，請呼叫 GetSecurityDescriptorControl 函式，並檢查 \_ \_ 安全 \_ 描述項控制參數的 SE 自我相對旗標 \_ 。
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: 絕對和 Self-Relative 的安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2639d1f17527b92116eabcaca96b637012253bbafc42198e37c9867fc585c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914720"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>絕對和 Self-Relative 的安全描述項

[*安全描述項*](/windows/desktop/SecGloss/s-gly)可以是 [*絕對*](/windows/desktop/SecGloss/a-gly)或 [*自我相關*](/windows/desktop/SecGloss/s-gly)的格式。 在絕對格式中，安全描述項包含其資訊的指標，而不是資訊本身。 在自我相關的格式中，安全描述項會將 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) 結構和相關聯的安全性資訊儲存在連續的記憶體區塊中。 若要判斷安全描述項是否為自我或絕對安全描述項，請呼叫 [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)函式，並檢查 \_ \_ [**安全 \_ 描述項 \_ 控制**](security-descriptor-control.md)參數的 SE 自我相對旗標。 您可以使用 [**MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) 和 [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) 函數來轉換這兩種格式。

當您要建立安全描述項並且具有所有元件的指標時（例如，擁有者、群組和任意 ACL 的預設設定可用時），絕對格式會很有用。 在此情況下，您可以呼叫 [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) 函式來初始化 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) 結構，然後呼叫 [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) 之類的函式，將 ACL 和 SID 指標指派給安全描述項。

在自我相關的格式中，安全描述項的開頭一律是 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) 結構，但安全描述項的其他元件可以依照任何順序遵循結構。 安全描述項的元件是由描述項開頭的位移來識別，而不是使用記憶體位址。 當安全描述項必須儲存在磁片上、透過通訊協定傳輸，或複製到記憶體時，此格式會很有用。

除了 [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd)以外，傳回安全描述項的所有函式都會使用自我相關格式來進行。 以引數形式傳遞至函式的安全描述項可以是自我或絕對形式。 如需詳細資訊，請參閱函式的檔。

 

 
