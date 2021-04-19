---
description: 下列清單包含 C2 層級安全性的一些最重要需求，如美國所定義
ms.assetid: e81f31bb-6314-4493-844a-65032e3cf90b
title: C2 層級安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1653221b30d6556e4b0c6c1fd2eec194b46d7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974733"
---
# <a name="c2-level-security"></a><span data-ttu-id="e141b-103">C2 層級安全性</span><span class="sxs-lookup"><span data-stu-id="e141b-103">C2-level Security</span></span>

<span data-ttu-id="e141b-104">下列清單包含 C2 層級安全性的一些最重要需求，如美國國防部所定義：</span><span class="sxs-lookup"><span data-stu-id="e141b-104">The following list includes some of the most important requirements of C2-level security, as defined by the U.S. Department of Defense:</span></span>

-   <span data-ttu-id="e141b-105">您必須授與或拒絕個別使用者或命名使用者群組的存取權，才能控制資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="e141b-105">It must be possible to control access to a resource by granting or denying access to individual users or named groups of users.</span></span>
-   <span data-ttu-id="e141b-106">記憶體必須受到保護，如此一來，在 [*處理*](/windows/desktop/SecGloss/p-gly) 程式釋出之後，才能讀取其內容。</span><span class="sxs-lookup"><span data-stu-id="e141b-106">Memory must be protected so that its contents cannot be read after a [*process*](/windows/desktop/SecGloss/p-gly) frees it.</span></span> <span data-ttu-id="e141b-107">同樣地，安全檔案系統（例如 NTFS）必須防止讀取已刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="e141b-107">Similarly, a secure file system, such as NTFS, must protect deleted files from being read.</span></span>
-   <span data-ttu-id="e141b-108">使用者必須在登入時以獨特的方式（例如密碼）識別自己。</span><span class="sxs-lookup"><span data-stu-id="e141b-108">Users must identify themselves in a unique manner, such as by password, when they log on.</span></span> <span data-ttu-id="e141b-109">所有可審核的動作都必須識別執行動作的使用者。</span><span class="sxs-lookup"><span data-stu-id="e141b-109">All auditable actions must identify the user performing the action.</span></span>
-   <span data-ttu-id="e141b-110">系統管理員必須能夠審核安全性相關事件。</span><span class="sxs-lookup"><span data-stu-id="e141b-110">System administrators must be able to audit security-related events.</span></span> <span data-ttu-id="e141b-111">不過，對安全性相關事件的存取權必須限制為授權的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="e141b-111">However, access to the security-related events audit data must be limited to authorized administrators.</span></span>
-   <span data-ttu-id="e141b-112">系統必須受到保護，以防止外部干擾或篡改，例如修改執行中的系統或儲存在磁片上的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="e141b-112">The system must be protected from external interference or tampering, such as modification of the running system or of system files stored on disk.</span></span>

 

 
