---
description: 有效的功能安全描述項包含二進位格式的安全性資訊。
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: 安全描述項字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413788"
---
# <a name="security-descriptor-strings"></a>安全描述項字串

有效的功能 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 包含二進位格式的安全性資訊。 Windows API 提供在文字字串之間來回轉換二進位安全描述項的函數。 字串格式的安全描述項無法正常運作，但可能有助於儲存或傳輸安全描述項資訊。

若要將安全描述項轉換成字串格式，請呼叫 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 函數。 若要將字串格式安全描述項轉換回有效的功能安全描述項，請呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數。

如需詳細資訊，請參閱 [安全描述項定義語言](security-descriptor-definition-language.md)。

 

 
