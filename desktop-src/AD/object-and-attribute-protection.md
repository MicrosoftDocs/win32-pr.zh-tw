---
title: 物件和屬性保護
description: 存取控制清單 (ACL) 保護 Active Directory Domain Services 中的所有物件。
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- 物件和屬性保護
- 安全性 AD、物件和屬性保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671263"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="b4d7b-105">物件和屬性保護</span><span class="sxs-lookup"><span data-stu-id="b4d7b-105">Object and Attribute Protection</span></span>

<span data-ttu-id="b4d7b-106">存取控制清單 (ACL) 保護 Active Directory Domain Services 中的所有物件。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="b4d7b-107">Acl 會決定誰可以查看物件、可讀取的屬性，以及每位使用者可以在物件上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="b4d7b-108">未經授權的使用者永遠看不到物件或屬性的存在。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="b4d7b-109">ACL 是存取控制專案的清單 (Ace) 與它所保護的物件一起儲存。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="b4d7b-110">在 Windows NT 和 Windows 2000 中，ACL 會儲存為二進位值，稱為安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="b4d7b-111">每個 ACE 都包含安全識別碼 (SID) ，識別套用 ACE 的主體 (使用者或群組) ，以及 ACE 授與或拒絕之存取類型的相關資料。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="b4d7b-112">目錄物件的 Acl 包含套用至物件做為整體的 Ace，以及套用至物件之個別屬性的 Ace。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="b4d7b-113">這可讓系統管理員控制哪些使用者可以看到物件，以及這些使用者可以看到的屬性。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="b4d7b-114">例如，所有使用者可能會被授與所有其他使用者的電子郵件和電話號碼屬性的讀取權限，但使用者的安全性屬性可能會被拒絕，但不是特殊安全性系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="b4d7b-115">個別使用者可能會被授與個人屬性的寫入存取權，例如自己的使用者物件上的電話和郵寄地址。</span><span class="sxs-lookup"><span data-stu-id="b4d7b-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




