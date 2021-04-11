---
description: 有效的功能安全描述項包含二進位格式的安全性資訊。
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: 安全描述項字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113785"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="f986e-103">安全描述項字串</span><span class="sxs-lookup"><span data-stu-id="f986e-103">Security Descriptor Strings</span></span>

<span data-ttu-id="f986e-104">有效的功能 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 包含二進位格式的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="f986e-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="f986e-105">Windows API 提供將二進位安全描述項轉換成文字字串和從中轉換的函式。</span><span class="sxs-lookup"><span data-stu-id="f986e-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="f986e-106">字串格式的安全描述項無法正常運作，但可能有助於儲存或傳輸安全描述項資訊。</span><span class="sxs-lookup"><span data-stu-id="f986e-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="f986e-107">若要將安全描述項轉換成字串格式，請呼叫 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 函數。</span><span class="sxs-lookup"><span data-stu-id="f986e-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="f986e-108">若要將字串格式安全描述項轉換回有效的功能安全描述項，請呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函數。</span><span class="sxs-lookup"><span data-stu-id="f986e-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="f986e-109">如需詳細資訊，請參閱 [安全描述項定義語言](security-descriptor-definition-language.md)。</span><span class="sxs-lookup"><span data-stu-id="f986e-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
