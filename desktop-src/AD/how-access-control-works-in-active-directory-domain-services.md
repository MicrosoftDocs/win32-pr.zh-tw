---
title: 存取控制在 Active Directory Domain Services 中的運作方式
description: Active Directory Domain Services 中物件的存取控制是以 Windows NT 和 Windows 2000 存取控制模型為基礎。
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services、安全性、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933063"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a><span data-ttu-id="46993-104">存取控制在 Active Directory Domain Services 中的運作方式</span><span class="sxs-lookup"><span data-stu-id="46993-104">How Access Control Works in Active Directory Domain Services</span></span>

<span data-ttu-id="46993-105">Active Directory Domain Services 中物件的存取控制是以 Windows NT 和 Windows 2000 存取控制模型為基礎。</span><span class="sxs-lookup"><span data-stu-id="46993-105">Access control for objects in Active Directory Domain Services is based on Windows NT and Windows 2000 access-control models.</span></span> <span data-ttu-id="46993-106">如需此模型及其元件（如安全描述項、存取權杖、Sid、Acl 和 Ace）的詳細資訊和詳細說明，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。</span><span class="sxs-lookup"><span data-stu-id="46993-106">For more information and a detailed description of this model and its components such as security descriptors, access tokens, SIDs, ACLs, and ACEs, see [Access Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="46993-107">Active Directory Domain Services 中資源的存取權限通常會透過使用 (ACE) 的存取控制專案來授與。</span><span class="sxs-lookup"><span data-stu-id="46993-107">Access privileges for resources in Active Directory Domain Services are usually granted through the use of an access control entry (ACE).</span></span> <span data-ttu-id="46993-108">ACE 會定義特定使用者或群組之物件的存取權或審核許可權。</span><span class="sxs-lookup"><span data-stu-id="46993-108">An ACE defines an access or audit permission on an object for a specific user or group.</span></span> <span data-ttu-id="46993-109"> (ACL) 的存取控制清單，是針對物件所定義之存取控制專案的已排序集合。</span><span class="sxs-lookup"><span data-stu-id="46993-109">An access-control list (ACL) is the ordered collection of access control entries defined for an object.</span></span> <span data-ttu-id="46993-110">安全描述項支援可建立和管理 Acl 的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="46993-110">A security descriptor supports properties and methods that create and manage ACLs.</span></span> <span data-ttu-id="46993-111">如需安全性模型的詳細資訊，請參閱 [安全性](/windows/desktop/SecAuthZ/access-control) 或 *Windows 2000 伺服器資源套件*。</span><span class="sxs-lookup"><span data-stu-id="46993-111">For more information about security models, see [Security](/windows/desktop/SecAuthZ/access-control) or the *Windows 2000 Server Resource Kit*.</span></span> <span data-ttu-id="46993-112"> (此資源可能無法在某些語言及國家或地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="46993-112">(This resource may not be available in some languages and countries or regions.)</span></span>

<span data-ttu-id="46993-113">安全性模型的基本大綱是：</span><span class="sxs-lookup"><span data-stu-id="46993-113">The basic outline of the security model is:</span></span>

-   <span data-ttu-id="46993-114">安全描述項。</span><span class="sxs-lookup"><span data-stu-id="46993-114">Security descriptor.</span></span> <span data-ttu-id="46993-115">每個目錄物件都有自己的安全描述項，其中包含保護物件的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="46993-115">Each directory object has its own security descriptor that contains security data that protects the object.</span></span> <span data-ttu-id="46993-116">安全描述項可包含 (DACL) 的任意存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="46993-116">The security descriptor can contain a discretionary access-control list (DACL).</span></span> <span data-ttu-id="46993-117">DACL 包含 Ace 的清單。</span><span class="sxs-lookup"><span data-stu-id="46993-117">A DACL contains a list of ACEs.</span></span> <span data-ttu-id="46993-118">每個 ACE 都授與或拒絕使用者或群組的一組存取權限。</span><span class="sxs-lookup"><span data-stu-id="46993-118">Each ACE grants or denies a set of access rights to a user or group.</span></span> <span data-ttu-id="46993-119">存取權限會對應到可以在物件上執行的作業，例如讀取和寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="46993-119">The access rights correspond to the operations, such as reading and writing properties, that can be performed on the object.</span></span>
-   <span data-ttu-id="46993-120">安全性內容。</span><span class="sxs-lookup"><span data-stu-id="46993-120">Security context.</span></span> <span data-ttu-id="46993-121">存取目錄物件時，應用程式會指定進行存取嘗試的安全性主體認證。</span><span class="sxs-lookup"><span data-stu-id="46993-121">When a directory object is accessed, the application specifies the credentials of the security principal that is making the access attempt.</span></span> <span data-ttu-id="46993-122">經過驗證後，這些認證會決定應用程式的安全性內容，包括與安全性主體相關聯的群組成員資格和許可權。</span><span class="sxs-lookup"><span data-stu-id="46993-122">When authenticated, these credentials determine the application's security context, which includes the group memberships and privileges associated with the security principal.</span></span> <span data-ttu-id="46993-123">如需安全性環境的詳細資訊，請參閱 [安全性內容和 Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="46993-123">For more information about security contexts, see [Security Contexts and Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).</span></span>
-   <span data-ttu-id="46993-124">存取檢查。</span><span class="sxs-lookup"><span data-stu-id="46993-124">Access check.</span></span> <span data-ttu-id="46993-125">只有當物件的安全描述項將必要的存取權限授與嘗試操作 (的安全性主體，或安全性主體所屬的群組) 時，系統才會授與物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="46993-125">The system grants access to an object only if the object's security descriptor grants the necessary access rights to the security principal attempting the operation (or to groups to which the security principal belongs).</span></span>

<span data-ttu-id="46993-126">下表列出用來操作 Active Directory Domain Services 之存取控制功能的 ADSI 介面。</span><span class="sxs-lookup"><span data-stu-id="46993-126">The following table lists ADSI interfaces used to manipulate the access control features of Active Directory Domain Services.</span></span>



| <span data-ttu-id="46993-127">介面</span><span class="sxs-lookup"><span data-stu-id="46993-127">Interface</span></span>                                                 | <span data-ttu-id="46993-128">描述</span><span class="sxs-lookup"><span data-stu-id="46993-128">Description</span></span>                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="46993-129">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="46993-129">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | <span data-ttu-id="46993-130">用來讀取和寫入目錄服務物件的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="46993-130">Used to read and write security properties of a directory service object.</span></span> |
| [<span data-ttu-id="46993-131">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="46993-131">**IADsAccessControlList**</span></span>](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | <span data-ttu-id="46993-132">用來管理和列舉目錄服務物件的所有 Ace。</span><span class="sxs-lookup"><span data-stu-id="46993-132">Used to manage and enumerate all ACEs for a directory service object.</span></span>     |
| [<span data-ttu-id="46993-133">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="46993-133">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | <span data-ttu-id="46993-134">用來讀取和寫入 ACE 屬性。</span><span class="sxs-lookup"><span data-stu-id="46993-134">Used to read and write ACE properties.</span></span>                                    |



 

 

 