---
title: 預設安全描述項
description: 使用 Active Directory Domain Services，您也可以為每種類型的物件指定預設的安全性。
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- 預設安全描述項 AD
- 安全描述項 AD、預設
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023261"
---
# <a name="default-security-descriptor"></a><span data-ttu-id="4d549-105">預設安全描述項</span><span class="sxs-lookup"><span data-stu-id="4d549-105">Default Security Descriptor</span></span>

<span data-ttu-id="4d549-106">使用 Active Directory Domain Services，您也可以為每種類型的物件指定預設的安全性。</span><span class="sxs-lookup"><span data-stu-id="4d549-106">With Active Directory Domain Services, you can also specify default security for each type of object.</span></span> <span data-ttu-id="4d549-107">這是在 [Active Directory 架構](active-directory-schema.md)中 [**classSchema**](/windows/desktop/ADSchema/c-classschema)物件定義的 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor)屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="4d549-107">This is specified in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) attribute in the [**classSchema**](/windows/desktop/ADSchema/c-classschema) object definition in the [Active Directory schema](active-directory-schema.md).</span></span> <span data-ttu-id="4d549-108">如果在建立物件期間未指定任何安全描述項，則會使用這個安全描述項來提供物件的預設保護。</span><span class="sxs-lookup"><span data-stu-id="4d549-108">This security descriptor is used to provide default protection on the object if there is no security descriptor specified during the creation of the object.</span></span>

> [!Note]  
> <span data-ttu-id="4d549-109">預設安全描述項中的 Ace 會以在建立物件時所指定的方式來處理。</span><span class="sxs-lookup"><span data-stu-id="4d549-109">ACEs from a default security descriptor are handled as if they were specified as part of object creation.</span></span> <span data-ttu-id="4d549-110">因此，預設 Ace 會放置在繼承的 Ace 前面，並視需要加以覆寫。</span><span class="sxs-lookup"><span data-stu-id="4d549-110">Therefore, the default ACEs are placed preceding inherited ACEs and override them as appropriate.</span></span> <span data-ttu-id="4d549-111">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="4d549-111">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="4d549-112">[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor)是使用 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) 以特殊字元串格式指定。</span><span class="sxs-lookup"><span data-stu-id="4d549-112">The [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) is specified in a special string format using the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="4d549-113">您可以使用兩個函式，將安全描述項的二進位形式轉換成字串格式，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="4d549-113">Two functions can be used to convert binary form of the security descriptor to string format and vice versa.</span></span> <span data-ttu-id="4d549-114">這些函式是：</span><span class="sxs-lookup"><span data-stu-id="4d549-114">These functions are:</span></span>

-   [<span data-ttu-id="4d549-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="4d549-115">ConvertSecurityDescriptorToStringSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [<span data-ttu-id="4d549-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="4d549-116">ConvertStringSecurityDescriptorToSecurityDescriptor</span></span>](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

<span data-ttu-id="4d549-117">如需預先定義之物件類別的詳細資訊和預設安全描述項，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)的 Active Directory 架構參考中的類別參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4d549-117">For more information and the default security descriptors of the predefined object classes, see the class reference pages in the Active Directory Schema Reference of the [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="4d549-118">如需讀取或修改物件類別之 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) 屬性的詳細資訊和程式碼範例，請參閱 [讀取物件類別的 DefaultSecurityDescriptor](reading-the-defaultsecuritydescriptor-for-an-object-class.md) ，以及 [修改物件類別的 defaultSecurityDescriptor](modifying-the-defaultsecuritydescriptor-for-an-object-class.md)。</span><span class="sxs-lookup"><span data-stu-id="4d549-118">For more information and a code example that reads or modifies the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) property of an object class, see [Reading the defaultSecurityDescriptor for an Object Class](reading-the-defaultsecuritydescriptor-for-an-object-class.md) and [Modifying the defaultSecurityDescriptor for an Object Class](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).</span></span>

 

 