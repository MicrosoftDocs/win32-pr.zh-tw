---
title: COM 的存取控制清單
description: COM 的存取控制清單
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672375"
---
# <a name="access-control-lists-for-com"></a><span data-ttu-id="341fd-103">COM 的存取控制清單</span><span class="sxs-lookup"><span data-stu-id="341fd-103">Access Control Lists for COM</span></span>

<span data-ttu-id="341fd-104">Windows Server XP Service Pack 2 (SP 2) 和 Windows Server 2003 Service Pack 1 (SP 1) 引進分散式元件物件模型 (DCOM) 的安全性增強功能。</span><span class="sxs-lookup"><span data-stu-id="341fd-104">Windows Server XP Service Pack 2 (SP 2) and Windows Server 2003 Service Pack 1 (SP 1) introduce security enhancements for the Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="341fd-105">這些增強功能的其中一項是更特定的存取權限，可在 (Acl) 的存取控制清單中使用。</span><span class="sxs-lookup"><span data-stu-id="341fd-105">One of these enhancements is more specific access rights for use in access control lists (ACLs).</span></span> <span data-ttu-id="341fd-106">存取權限為：</span><span class="sxs-lookup"><span data-stu-id="341fd-106">The access rights are:</span></span>

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

<span data-ttu-id="341fd-107">為了提供回溯相容性，ACL 可能會以 Windows XP SP 2 和 Windows Server 2003 SP 1 之前所使用的格式存在，它只會使用存取權限的許可權 \_ \_ 執行，或可能存在於 WINDOWS XP SP 2 和 windows SERVER 2003 SP 1 中使用的新格式，此格式 \_ 會 \_ 搭配 com 許可權執行 \_ \_ \_ 本機、com \_ rights \_ execute \_ remote、com \_ rights \_ activate \_ 本機和 com \_ 許可權 \_ 啟用 \_ 遠端。</span><span class="sxs-lookup"><span data-stu-id="341fd-107">To provide backward compatibility, an ACL may exist in the format used before Windows XP SP 2 and Windows Server 2003 SP 1, which uses only the access right COM\_RIGHTS\_EXECUTE, or it may exist in the new format used in Windows XP SP 2 and Windows Server 2003 SP 1, which uses COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

> [!Note]  
> <span data-ttu-id="341fd-108">\_ \_ 必須一律存在 COM 許可權，否則不存在此許可權會產生不正確安全描述項。</span><span class="sxs-lookup"><span data-stu-id="341fd-108">COM\_RIGHTS\_EXECUTE must always be present; the absence of this right generates an invalid security descriptor.</span></span>

 

<span data-ttu-id="341fd-109">您不得在單一 ACL 內混用舊格式和新格式; (Ace 的所有存取控制專案) 必須僅授與 COM \_ 許可權 \_ 執行存取權限，或全部都必須授與 com 許可權執行、com rights \_ \_ execute、 \_ \_ \_ com \_ rights \_ execute \_ remote、com \_ rights \_ activate \_ 本機和 com 許可權 \_ \_ 啟用 \_ 遠端的組合。</span><span class="sxs-lookup"><span data-stu-id="341fd-109">You must not mix the old format and the new format within a single ACL; either all access control entries (ACEs) must grant only the COM\_RIGHTS\_EXECUTE access right, or they all must grant COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

<span data-ttu-id="341fd-110">以下是格式不正確的 ACL 範例：</span><span class="sxs-lookup"><span data-stu-id="341fd-110">The following is an example of an incorrectly formatted ACL:</span></span>

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

<span data-ttu-id="341fd-111">請注意，第一個存取控制專案 (ACE) 只會授與 COM \_ rights \_ execute (0x1) ，而第二個 ACE 會授 \_ 與 com 許可權執行 \_ 、com \_ 許可權 \_ 執行 \_ 本機和 com 許可權，以啟用本機 (\_ \_ \_ 0xb) ，而第三個授 \_ 與 com 許可權 \_ 執行和 com \_ 許可權會 \_ 啟用 \_ 本機 (0x9) 。</span><span class="sxs-lookup"><span data-stu-id="341fd-111">Note that the first access control entry (ACE) grants COM\_RIGHTS\_EXECUTE (0x1) only, while the second ACE grants COM\_RIGHTS\_EXECUTE, COM\_RIGHTS\_EXECUTE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_LOCAL (0xb), and the third grants COM\_RIGHTS\_EXECUTE and COM\_RIGHTS\_ACTIVATE\_LOCAL (0x9).</span></span>

<span data-ttu-id="341fd-112">若要修正這個錯誤，應該將第一個 ACE 變更為 \_ \_ 與其他四個存取權限的其中一個結合執行 com 許可權，否則第二個和第三個 ace 應變更為僅授與 com \_ 許可權 \_ 執行。</span><span class="sxs-lookup"><span data-stu-id="341fd-112">To correct this, the first ACE should be changed to grant COM\_RIGHTS\_EXECUTE in combination with one of the other four access rights, or else the second and third ACEs should be changed to grant only COM\_RIGHTS\_EXECUTE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="341fd-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="341fd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="341fd-114">Windows XP Service Pack 2 和 Windows Server 2003 Service Pack 1 中的 DCOM 安全性增強功能</span><span class="sxs-lookup"><span data-stu-id="341fd-114">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[<span data-ttu-id="341fd-115">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="341fd-115">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




