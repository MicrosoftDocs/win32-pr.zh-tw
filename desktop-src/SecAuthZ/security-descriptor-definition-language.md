---
description: 說明 (SDDL) 的安全描述項定義語言。
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: 安全描述項定義語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b72e74f49d34577251aef3d875a3c0e9aede07556be1b918ad532f3987c54d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907408"
---
# <a name="security-descriptor-definition-language"></a>安全描述項定義語言

安全描述項定義語言 (SDDL) 定義 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數用來將 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 描述為文字字串的字串格式。 此語言也會定義字串元素，以描述安全描述項元件中的資訊。

> [!Note]  
> 條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 具有與其他 ACE 類型不同的 SDDL 格式。 針對 Ace，請參閱 [Ace 字串](ace-strings.md)。 針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[安全描述項字串格式](security-descriptor-string-format.md)
</dt> <dt>

[條件式 Ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[ACE 字串](ace-strings.md)
</dt> <dt>

[SID 字串](sid-strings.md)
</dt> <dt>

[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
