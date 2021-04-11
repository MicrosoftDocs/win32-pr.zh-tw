---
description: 存取控制編輯器可以包含 [審核] 屬性頁，讓使用者在 [物件系統存取控制清單] 中， (SACL)  (Ace) ，來查看和編輯存取控制專案。 如需 Sacl 的詳細資訊，請參閱 (Acl) 的存取控制清單。
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: '[審核] 屬性頁'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193663"
---
# <a name="auditing-property-page"></a><span data-ttu-id="cbc58-104">[審核] 屬性頁</span><span class="sxs-lookup"><span data-stu-id="cbc58-104">Auditing Property Page</span></span>

<span data-ttu-id="cbc58-105">存取控制編輯器可以包含 [**審核**] 屬性頁，讓使用者可以在物件的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)中， (SACL)  (ace) ，來查看和編輯 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。</span><span class="sxs-lookup"><span data-stu-id="cbc58-105">The access control editor can include an **Auditing** property page that enables the user to view and edit the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in an object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="cbc58-106">如需 Sacl 的詳細資訊，請參閱 (Acl) 的 [存取控制清單](access-control-lists.md) 。</span><span class="sxs-lookup"><span data-stu-id="cbc58-106">For more information about SACLs, see [Access Control Lists](access-control-lists.md) (ACLs).</span></span>

<span data-ttu-id="cbc58-107">**若要查看 [審核] 屬性頁**</span><span class="sxs-lookup"><span data-stu-id="cbc58-107">**To view the Auditing property page**</span></span>

-   <span data-ttu-id="cbc58-108">在 [ [基本安全性] 屬性頁](basic-security-property-page.md)上，按一下 [ **Advanced**]。</span><span class="sxs-lookup"><span data-stu-id="cbc58-108">On the [basic security property page](basic-security-property-page.md), click **Advanced**.</span></span> <span data-ttu-id="cbc58-109">[ **審核** ] 屬性頁位於 [ [advanced security] 屬性工作表](advanced-security-property-sheet.md)中。</span><span class="sxs-lookup"><span data-stu-id="cbc58-109">The **Auditing** property page is in the [advanced security property sheet](advanced-security-property-sheet.md).</span></span>

<span data-ttu-id="cbc58-110">若要包含 [**審核**] 屬性頁，請在 [**ISecurityInformation：： GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation)執行所傳回 [**的 si \_ 物件 \_ 資訊**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)結構中，設定 **si \_ ADVANCED** 和 **si \_ 編輯 \_ 審核** 旗標。</span><span class="sxs-lookup"><span data-stu-id="cbc58-110">To include the **Auditing** property page, set the **SI\_ADVANCED** and **SI\_EDIT\_AUDITS** flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
