---
description: 說明 (SDDL) 的安全描述項定義語言。
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: 安全描述項定義語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848238"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="55e7c-103">安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="55e7c-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="55e7c-104">安全描述項定義語言 (SDDL) 定義 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數用來將 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 描述為文字字串的字串格式。</span><span class="sxs-lookup"><span data-stu-id="55e7c-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="55e7c-105">此語言也會定義字串元素，以描述安全描述項元件中的資訊。</span><span class="sxs-lookup"><span data-stu-id="55e7c-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="55e7c-106">條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 具有與其他 ACE 類型不同的 SDDL 格式。</span><span class="sxs-lookup"><span data-stu-id="55e7c-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="55e7c-107">針對 Ace，請參閱 [Ace 字串](ace-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="55e7c-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="55e7c-108">針對條件式 Ace，請參閱 [條件式 ace 的安全描述項定義語言](security-descriptor-definition-language-for-conditional-aces-.md)。</span><span class="sxs-lookup"><span data-stu-id="55e7c-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="55e7c-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="55e7c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55e7c-110">安全描述項字串格式</span><span class="sxs-lookup"><span data-stu-id="55e7c-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="55e7c-111">條件式 Ace 的安全描述項定義語言</span><span class="sxs-lookup"><span data-stu-id="55e7c-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="55e7c-112">ACE 字串</span><span class="sxs-lookup"><span data-stu-id="55e7c-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="55e7c-113">SID 字串</span><span class="sxs-lookup"><span data-stu-id="55e7c-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="55e7c-114">[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="55e7c-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
