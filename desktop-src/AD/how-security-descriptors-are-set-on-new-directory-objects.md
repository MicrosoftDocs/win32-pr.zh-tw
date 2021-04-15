---
title: 如何在新的目錄物件上設定安全描述項
description: 當您在 Active Directory Domain Services 中建立新的物件時，您可以明確建立安全描述項，然後將該安全描述項設定為物件的 nTSecurityDescriptor 屬性。
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- 物件 AD，如何在新的目錄物件上設定安全描述項
- 安全性描述項 AD，如何設定新的目錄物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462856"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a><span data-ttu-id="ca65a-105">如何在新的目錄物件上設定安全描述項</span><span class="sxs-lookup"><span data-stu-id="ca65a-105">How Security Descriptors are Set on New Directory Objects</span></span>

<span data-ttu-id="ca65a-106">當您在 Active Directory Domain Services 中建立新的物件時，您可以明確建立安全描述項，然後將該安全描述項設定為物件的 **nTSecurityDescriptor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca65a-106">When you create a new object in Active Directory Domain Services, you can explicitly create a security descriptor and then set that security descriptor as the object's **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="ca65a-107">如需詳細資訊，請參閱 [建立新目錄物件的安全描述項](creating-a-security-descriptor-for-a-new-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="ca65a-107">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>

<span data-ttu-id="ca65a-108">Active Directory Domain Services 使用下列規則來設定新物件的安全描述項中的 DACL：</span><span class="sxs-lookup"><span data-stu-id="ca65a-108">Active Directory Domain Services use the following rules to set the DACL in the new object's security descriptor:</span></span>

-   <span data-ttu-id="ca65a-109">如果您在建立物件時明確指定安全描述項，系統會將來自父物件的任何可繼承 Ace 合併為指定的 DACL，除非已在安全描述項的控制位中設定 **SE \_ DACL \_ 保護** 的位。</span><span class="sxs-lookup"><span data-stu-id="ca65a-109">If you explicitly specify a security descriptor when you create the object, the system merges any inheritable ACEs from the parent object into the specified DACL unless the **SE\_DACL\_PROTECTED** bit is set in the security descriptor's control bits.</span></span>
-   <span data-ttu-id="ca65a-110">如果您未指定安全描述項，系統會將父物件的任何可繼承 Ace，從物件類別的 **classSchema** 物件合併到預設 dacl，以建立物件的 dacl。</span><span class="sxs-lookup"><span data-stu-id="ca65a-110">If you do not specify a security descriptor, the system builds the object's DACL by merging any inheritable ACEs from the parent object into the default DACL from the **classSchema** object for the object's class.</span></span>
-   <span data-ttu-id="ca65a-111">如果架構沒有預設的 DACL，則物件的 DACL 是建立者之主要或模擬權杖中的預設 DACL。</span><span class="sxs-lookup"><span data-stu-id="ca65a-111">If the schema does not have a default DACL, the object's DACL is the default DACL from the primary or impersonation token of the creator.</span></span>
-   <span data-ttu-id="ca65a-112">如果沒有指定、繼承或預設的 DACL，系統就會建立沒有 DACL 的物件，讓每個人都能完全存取該物件。</span><span class="sxs-lookup"><span data-stu-id="ca65a-112">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="ca65a-113">系統會使用類似的演算法來建立目錄服務物件的 SACL。</span><span class="sxs-lookup"><span data-stu-id="ca65a-113">The system uses a similar algorithm to build a SACL for a directory service object.</span></span>

<span data-ttu-id="ca65a-114">當您建立物件時，新物件安全描述項中的擁有者和主要群組會設定為您在 **nTSecurityDescriptor** 屬性中指定的值。</span><span class="sxs-lookup"><span data-stu-id="ca65a-114">The owner and primary group in the new object's security descriptor are set to the values you specify in the **nTSecurityDescriptor** property when you create the object.</span></span> <span data-ttu-id="ca65a-115">如果您未設定這些值，Active Directory Domain Services 會使用下表所列的規則來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="ca65a-115">If you do not set these values, Active Directory Domain Services use the rules listed in the following table to set them.</span></span>



| <span data-ttu-id="ca65a-116">規則</span><span class="sxs-lookup"><span data-stu-id="ca65a-116">Rule</span></span>          | <span data-ttu-id="ca65a-117">描述</span><span class="sxs-lookup"><span data-stu-id="ca65a-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca65a-118">擁有者</span><span class="sxs-lookup"><span data-stu-id="ca65a-118">Owner</span></span>         | <span data-ttu-id="ca65a-119">預設安全描述項中的擁有者會從建立進程的主要或模擬權杖設定為預設擁有者 SID。</span><span class="sxs-lookup"><span data-stu-id="ca65a-119">The owner in a default security descriptor is set to the default owner SID from the primary or impersonation token of the creating process.</span></span> <span data-ttu-id="ca65a-120">對於大部分的使用者而言，預設擁有者 SID 與識別使用者帳戶的 SID 相同。</span><span class="sxs-lookup"><span data-stu-id="ca65a-120">For most users, the default owner SID is the same as the SID that identifies the user's account.</span></span> <span data-ttu-id="ca65a-121">請注意，對於屬於內建 administrators 群組成員的使用者，系統會自動將存取權杖中的預設擁有者 SID 設定為系統管理員群組;因此，由 administrators 群組成員建立的物件通常是由 administrators 群組所擁有。</span><span class="sxs-lookup"><span data-stu-id="ca65a-121">Be aware that for users who are members of the built-in administrators group, the system automatically sets the default owner SID in the access token to the administrators group; therefore, objects created by a member of the administrators group are typically owned by the administrators group.</span></span> <span data-ttu-id="ca65a-122">若要取得或設定存取權杖中的預設擁有者，請使用 [**權杖 \_ 擁有**](/windows/desktop/api/winnt/ns-winnt-token_owner)者結構來呼叫 [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)或 [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation)函數。</span><span class="sxs-lookup"><span data-stu-id="ca65a-122">To get or set the default owner in an access token, call the [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/winnt/ns-winnt-token_owner) structure.</span></span> |
| <span data-ttu-id="ca65a-123">主要群組</span><span class="sxs-lookup"><span data-stu-id="ca65a-123">Primary Group</span></span> | <span data-ttu-id="ca65a-124">預設安全描述項中的主要群組會設定為來自建立者主要或模擬權杖的預設主要群組。</span><span class="sxs-lookup"><span data-stu-id="ca65a-124">The primary group in a default security descriptor is set to the default primary group from the creator's primary or impersonation token.</span></span> <span data-ttu-id="ca65a-125">請注意，主要群組不會用於 Active Directory Domain Services 的內容中。</span><span class="sxs-lookup"><span data-stu-id="ca65a-125">Be aware that primary group is not used in the context of Active Directory Domain Services.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="ca65a-126">如需 ACE 繼承的詳細資訊，請參閱系統 [管理的繼承與委派](inheritance-and-delegation-of-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="ca65a-126">For more information about ACE inheritance, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>

<span data-ttu-id="ca65a-127">如需有關架構中預設安全描述項的詳細資訊，請參閱 [預設安全描述項](default-security-descriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="ca65a-127">For more information about the default security descriptors in the schema, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="ca65a-128">如需 **classSchema** 物件的詳細資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="ca65a-128">For more information about **classSchema** objects, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 