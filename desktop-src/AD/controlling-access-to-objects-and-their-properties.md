---
title: 控制物件和其屬性的存取權
description: 若要控制應用程式物件的存取權，請使用物件安全描述項，具體而言，就是使用 (DACL) 及其存取控制 (專案清單) 的任意存取控制清單。
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- 物件 AD，控制存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182959"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="cef73-104">控制物件和其屬性的存取權</span><span class="sxs-lookup"><span data-stu-id="cef73-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="cef73-105">若要控制應用程式物件的存取權，請使用物件安全描述項，具體而言，就是使用 (DACL) 及其存取控制 (專案清單) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="cef73-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="cef73-106">建立物件時，它會接收安全描述項。</span><span class="sxs-lookup"><span data-stu-id="cef73-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="cef73-107">如需詳細資訊，以及系統用來為新物件建立 DACL 的規則描述，請參閱 [如何在新的目錄物件上設定安全描述項](how-security-descriptors-are-set-on-new-directory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="cef73-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="cef73-108">這些規則顯示您可以：</span><span class="sxs-lookup"><span data-stu-id="cef73-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="cef73-109">建立新的安全描述項，並在建立時將其附加至物件。</span><span class="sxs-lookup"><span data-stu-id="cef73-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="cef73-110">如需詳細資訊，請參閱 [建立新目錄物件的安全描述項](creating-a-security-descriptor-for-a-new-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cef73-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="cef73-111">在目錄階層中的任何時間點套用可繼承的 ACE，如此一來，就會將 ACE 繼承到樹狀結構中的物件。</span><span class="sxs-lookup"><span data-stu-id="cef73-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="cef73-112">物件可以從其父容器繼承 ACE。</span><span class="sxs-lookup"><span data-stu-id="cef73-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="cef73-113">如需詳細資訊，請參閱系統 [管理的繼承與委派](inheritance-and-delegation-of-administration.md)。</span><span class="sxs-lookup"><span data-stu-id="cef73-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="cef73-114">如果您有必要的存取權限，請在架構中指定預設 DACL 中的 ACE。</span><span class="sxs-lookup"><span data-stu-id="cef73-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="cef73-115">架構中的每個物件類別定義都包含預設的安全描述項，可以有預設的 DACL。</span><span class="sxs-lookup"><span data-stu-id="cef73-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="cef73-116">如需詳細資訊，請參閱 [預設安全描述項](default-security-descriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="cef73-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="cef73-117">此外，您可以修改現有物件的 DACL。</span><span class="sxs-lookup"><span data-stu-id="cef73-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="cef73-118">您可以：</span><span class="sxs-lookup"><span data-stu-id="cef73-118">You can:</span></span>

-   <span data-ttu-id="cef73-119">將 DACL 取代為新的 DACL。</span><span class="sxs-lookup"><span data-stu-id="cef73-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="cef73-120">讀取現有的 DACL、加以修改，並套用修改過的 DACL。</span><span class="sxs-lookup"><span data-stu-id="cef73-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="cef73-121">如需詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cef73-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="cef73-122">下列清單描述 Active Directory Domain Services 中 ACE 的最重要功能。</span><span class="sxs-lookup"><span data-stu-id="cef73-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="cef73-123">您可以使用 ACE：</span><span class="sxs-lookup"><span data-stu-id="cef73-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="cef73-124">控制可以在物件上執行特定作業的人員。</span><span class="sxs-lookup"><span data-stu-id="cef73-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="cef73-125">控制誰可以存取物件的特定屬性或屬性集。</span><span class="sxs-lookup"><span data-stu-id="cef73-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="cef73-126">控制誰可以在容器中建立子物件，包括誰可以建立特定類型的子物件。</span><span class="sxs-lookup"><span data-stu-id="cef73-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="cef73-127">針對物件類型定義私用控制存取權限，以及控制誰可以執行由私用權利保護的作業。</span><span class="sxs-lookup"><span data-stu-id="cef73-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="cef73-128">將 ACE 套用至目錄子樹系根目錄中的容器物件，讓樹狀目錄中的所有子物件都能自動繼承保護。</span><span class="sxs-lookup"><span data-stu-id="cef73-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="cef73-129">套用子樹中的特定子物件類型所自動繼承的 ACE。</span><span class="sxs-lookup"><span data-stu-id="cef73-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="cef73-130">建立可授與許可權給安全性群組，而不是單一使用者的 ACE。</span><span class="sxs-lookup"><span data-stu-id="cef73-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="cef73-131">將 ACE 套用至群組原則的物件，以控制受原則影響的帳戶和電腦。</span><span class="sxs-lookup"><span data-stu-id="cef73-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




