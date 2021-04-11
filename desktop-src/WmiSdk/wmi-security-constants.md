---
description: WMI 會檢查應用程式和腳本的存取權限。
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: WMI 安全性常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194909"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="9c5b6-103">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="9c5b6-103">WMI Security Constants</span></span>

<span data-ttu-id="9c5b6-104">WMI 會檢查應用程式和腳本對於 WMI 命名空間、印表機、服務、DCOM 應用程式、檔案、共用和其他安全物件等物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="9c5b6-105">這些安全物件的存取權是由 (ACE) 的存取控制專案所控制。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="9c5b6-106">每個 ACE 都包含指定哪些群組或使用者具有存取權的清單。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="9c5b6-107">如需有關安全性和存取控制清單 (Acl、Dacl 或 Sacl) 的詳細資訊，請參閱 [ (acl 的存取控制清單) ](/windows/desktop/SecAuthZ/access-control-lists) 和 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="9c5b6-108">WMI 中許多會影響安全物件的提供者方法，都需要系統管理員啟用某些特殊許可權。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="9c5b6-109">您使用的許可權版本取決於程式設計語言，如 [**許可權常數**](privilege-constants.md)中所示。</span><span class="sxs-lookup"><span data-stu-id="9c5b6-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="9c5b6-110">安全性常數定義于下列主題中：</span><span class="sxs-lookup"><span data-stu-id="9c5b6-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="9c5b6-111">**事件安全性常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="9c5b6-112">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="9c5b6-113">**命名空間存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="9c5b6-114">**命名空間 ACE 旗標常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="9c5b6-115">**命名空間 ACE 類型常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="9c5b6-116">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="9c5b6-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
