---
description: 由於檔案是安全的物件，因此對它們的存取會受到控制 Windows 中所有其他安全物件存取權的存取控制模型所管制。
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: 檔案安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971721"
---
# <a name="file-security-and-access-rights"></a><span data-ttu-id="d70e9-103">檔案安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="d70e9-103">File Security and Access Rights</span></span>

<span data-ttu-id="d70e9-104">由於檔案是 [安全的物件](/windows/desktop/SecAuthZ/securable-objects)，因此對它們的存取會受到控制 Windows 中所有其他安全物件存取權的存取控制模型所管制。</span><span class="sxs-lookup"><span data-stu-id="d70e9-104">Because files are [securable objects](/windows/desktop/SecAuthZ/securable-objects), access to them is regulated by the access-control model that governs access to all other securable objects in Windows.</span></span> <span data-ttu-id="d70e9-105">如需此模型的詳細說明，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="d70e9-105">For a detailed explanation of this model, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="d70e9-106">當您呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)、 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)或 [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)函數時，可以指定檔案或目錄的 [安全描述項](/windows/desktop/api/winnt/ns-winnt-security_descriptor)。</span><span class="sxs-lookup"><span data-stu-id="d70e9-106">You can specify a [security descriptor](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for a file or directory when you call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), or [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) function.</span></span> <span data-ttu-id="d70e9-107">如果您對 *lpSecurityAttributes* 參數指定 **Null** ，則檔案或目錄會取得預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d70e9-107">If you specify **NULL** for the *lpSecurityAttributes* parameter, the file or directory gets a default security descriptor.</span></span> <span data-ttu-id="d70e9-108">存取控制會在檔案或目錄的預設安全描述項中， (ACL) 清單繼承自其父目錄。</span><span class="sxs-lookup"><span data-stu-id="d70e9-108">The access control lists (ACL) in the default security descriptor for a file or directory are inherited from its parent directory.</span></span> <span data-ttu-id="d70e9-109">請注意，只有在新建立檔案或目錄時，才會指派預設安全描述項，而不會在重新命名或移動時指派。</span><span class="sxs-lookup"><span data-stu-id="d70e9-109">Note that a default security descriptor is assigned only when a file or directory is newly created, and not when it is renamed or moved.</span></span>

<span data-ttu-id="d70e9-110">若要取得檔案或目錄物件的安全描述項，請呼叫 [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="d70e9-110">To retrieve the security descriptor of a file or directory object, call the [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) or [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="d70e9-111">若要變更檔案或目錄物件的安全描述項，請呼叫 [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) 或 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="d70e9-111">To change the security descriptor of a file or directory object, call the [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) or [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="d70e9-112">檔案和目錄的有效存取權限包括 **刪除**、**讀取 \_ 控制**、**寫入 \_ DAC**、**寫入 \_ 擁有** 者，以及 **同步處理**[標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="d70e9-112">The valid access rights for files and directories include the **DELETE**, **READ\_CONTROL**, **WRITE\_DAC**, **WRITE\_OWNER**, and **SYNCHRONIZE** [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="d70e9-113">檔案 [**存取權限常數**](file-access-rights-constants.md) 中的表格會列出檔案和目錄的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="d70e9-113">The table in [**File Access Rights Constants**](file-access-rights-constants.md) lists the access rights that are specific to files and directories.</span></span>

<span data-ttu-id="d70e9-114">雖然 **同步** 存取許可權是在 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) 清單中定義為在其中一個等候函式中指定檔案控制代碼的許可權，但在使用非同步檔案 i/o 作業時，您應該等候已 [**正確設定之**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 重迭結構中所包含的事件控制碼，而不是使用檔案控制代碼與同步處理的 **同步** 存取許可權。</span><span class="sxs-lookup"><span data-stu-id="d70e9-114">Although the **SYNCHRONIZE** access right is defined within the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) list as the right to specify a file handle in one of the wait functions, when using asynchronous file I/O operations you should wait on the event handle contained in a properly configured [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure rather than using the file handle with the **SYNCHRONIZE** access right for synchronization.</span></span>

<span data-ttu-id="d70e9-115">以下是檔案和目錄的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="d70e9-115">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for files and directories.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d70e9-116">存取權限</span><span class="sxs-lookup"><span data-stu-id="d70e9-116">Access right</span></span></th>
<th><span data-ttu-id="d70e9-117">Description</span><span class="sxs-lookup"><span data-stu-id="d70e9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d70e9-118"><strong>FILE_GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-118"><strong>FILE_GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="d70e9-119"><strong>FILE_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-119"><strong>FILE_EXECUTE</strong></span></span><br /><span data-ttu-id="d70e9-120">
<strong>FILE_READ_ATTRIBUTES</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-120">
<strong>FILE_READ_ATTRIBUTES</strong></span></span><br /><span data-ttu-id="d70e9-121">
<strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-121">
<strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="d70e9-122">
<strong>同步</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-122">
<strong>SYNCHRONIZE</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d70e9-123"><strong>FILE_GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-123"><strong>FILE_GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="d70e9-124"><strong>FILE_READ_ATTRIBUTES</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-124"><strong>FILE_READ_ATTRIBUTES</strong></span></span><br /><span data-ttu-id="d70e9-125">
<strong>FILE_READ_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-125">
<strong>FILE_READ_DATA</strong></span></span><br /><span data-ttu-id="d70e9-126">
<strong>FILE_READ_EA</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-126">
<strong>FILE_READ_EA</strong></span></span><br /><span data-ttu-id="d70e9-127">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-127">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="d70e9-128">
<strong>同步</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-128">
<strong>SYNCHRONIZE</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d70e9-129"><strong>FILE_GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-129"><strong>FILE_GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="d70e9-130"><strong>FILE_APPEND_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-130"><strong>FILE_APPEND_DATA</strong></span></span><br /><span data-ttu-id="d70e9-131">
<strong>FILE_WRITE_ATTRIBUTES</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-131">
<strong>FILE_WRITE_ATTRIBUTES</strong></span></span><br /><span data-ttu-id="d70e9-132">
<strong>FILE_WRITE_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-132">
<strong>FILE_WRITE_DATA</strong></span></span><br /><span data-ttu-id="d70e9-133">
<strong>FILE_WRITE_EA</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-133">
<strong>FILE_WRITE_EA</strong></span></span><br /><span data-ttu-id="d70e9-134">
<strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-134">
<strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="d70e9-135">
<strong>同步</strong></span><span class="sxs-lookup"><span data-stu-id="d70e9-135">
<strong>SYNCHRONIZE</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d70e9-136">Windows 會將要求的存取權限和執行緒存取權杖中的資訊，與檔案或目錄物件的安全描述項中的資訊進行比較。</span><span class="sxs-lookup"><span data-stu-id="d70e9-136">Windows compares the requested access rights and the information in the thread's access token with the information in the file or directory object's security descriptor.</span></span> <span data-ttu-id="d70e9-137">如果比較不禁止授與所有要求的存取權限，則會將物件的控制碼傳回給執行緒，並授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="d70e9-137">If the comparison does not prohibit all of the requested access rights from being granted, a handle to the object is returned to the thread and the access rights are granted.</span></span> <span data-ttu-id="d70e9-138">如需此程式的詳細資訊，請參閱 [執行緒和安全物件之間的互動](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="d70e9-138">For more information about this process, see [Interaction between Threads and Securable Objects](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).</span></span>

<span data-ttu-id="d70e9-139">依預設，存取檔案或目錄的授權是由與該檔案或目錄相關聯之安全描述項中的 Acl 所控制。</span><span class="sxs-lookup"><span data-stu-id="d70e9-139">By default, authorization for access to a file or directory is controlled strictly by the ACLs in the security descriptor associated with that file or directory.</span></span> <span data-ttu-id="d70e9-140">尤其是，父目錄的安全描述項不會用來控制對任何子檔案或目錄的存取。</span><span class="sxs-lookup"><span data-stu-id="d70e9-140">In particular, the security descriptor of a parent directory is not used to control access to any child file or directory.</span></span> <span data-ttu-id="d70e9-141">您可以藉由移除使用者的 **略過 \_ 遍歷 \_ 檢查**[許可權](/windows/desktop/SecAuthZ/privileges)，來強制執行檔案 **\_ 遍歷**[訪問](/windows/desktop/SecAuthZ/access-rights-and-access-masks)許可權。</span><span class="sxs-lookup"><span data-stu-id="d70e9-141">The **FILE\_TRAVERSE** [access right](/windows/desktop/SecAuthZ/access-rights-and-access-masks) can be enforced by removing the **BYPASS\_TRAVERSE\_CHECKING** [privilege](/windows/desktop/SecAuthZ/privileges) from users.</span></span> <span data-ttu-id="d70e9-142">在一般情況下，並不建議這麼做，因為許多程式都不會正確處理目錄遍歷錯誤。</span><span class="sxs-lookup"><span data-stu-id="d70e9-142">This is not recommended in the general case, as many programs do not correctly handle directory traversal errors.</span></span> <span data-ttu-id="d70e9-143">檔案的主要用途是在目錄上 **進行存取權限 \_** 的主要用途，是在需要與 Unix 系統之間的互通性時，能夠符合某些 IEEE 和 ISO POSIX 標準。</span><span class="sxs-lookup"><span data-stu-id="d70e9-143">The primary use for the **FILE\_TRAVERSE** access right on directories is to enable conformance to certain IEEE and ISO POSIX standards when interoperability with Unix systems is a requirement.</span></span>

<span data-ttu-id="d70e9-144">Windows 安全性模型提供一種方式，讓子目錄繼承或防止繼承父目錄的安全描述項中的一或多個 Ace。</span><span class="sxs-lookup"><span data-stu-id="d70e9-144">The Windows security model provides a way for a child directory to inherit, or to be prevented from inheriting, one or more of the ACEs in the parent directory's security descriptor.</span></span> <span data-ttu-id="d70e9-145">每個 ACE 都包含決定如何繼承的資訊，以及它是否會影響繼承目錄物件。</span><span class="sxs-lookup"><span data-stu-id="d70e9-145">Each ACE contains information that determines how it can be inherited, and whether it will have an effect on the inheriting directory object.</span></span> <span data-ttu-id="d70e9-146">例如，某些繼承的 Ace 會控制繼承的目錄物件的存取，而這些 Ace 稱為 *有效的 ace*。</span><span class="sxs-lookup"><span data-stu-id="d70e9-146">For example, some inherited ACEs control access to the inherited directory object, and these are called *effective ACEs*.</span></span> <span data-ttu-id="d70e9-147">所有其他 Ace 都稱為 *僅限繼承 ace*。</span><span class="sxs-lookup"><span data-stu-id="d70e9-147">All other ACEs are called *inherit-only ACEs*.</span></span>

<span data-ttu-id="d70e9-148">Windows 安全性模型也會根據 [ace 繼承規則](/windows/desktop/SecAuthZ/ace-inheritance-rules)，強制將 ace 自動繼承到子物件。</span><span class="sxs-lookup"><span data-stu-id="d70e9-148">The Windows security model also enforces the automatic inheritance of ACEs to child objects according to the [ACE inheritance rules](/windows/desktop/SecAuthZ/ace-inheritance-rules).</span></span> <span data-ttu-id="d70e9-149">此自動繼承以及每個 ACE 中的繼承資訊，會決定如何將安全性限制傳遞到目錄階層。</span><span class="sxs-lookup"><span data-stu-id="d70e9-149">This automatic inheritance, along with the inheritance information in each ACE, determines how security restrictions are passed down the directory hierarchy.</span></span>

<span data-ttu-id="d70e9-150">請注意，您不能使用拒絕存取的 ACE 來拒絕檔案的 **一般 \_ 讀取** 或僅 **一般 \_ 寫入** 存取權。</span><span class="sxs-lookup"><span data-stu-id="d70e9-150">Note that you cannot use an access-denied ACE to deny only **GENERIC\_READ** or only **GENERIC\_WRITE** access to a file.</span></span> <span data-ttu-id="d70e9-151">這是因為對於檔案物件而言， **泛型 \_ 讀取** 或 **一般 \_ 寫入** 的泛型對應會包含 **同步** 存取許可權。</span><span class="sxs-lookup"><span data-stu-id="d70e9-151">This is because for file objects, the generic mappings for both **GENERIC\_READ** or **GENERIC\_WRITE** include the **SYNCHRONIZE** access right.</span></span> <span data-ttu-id="d70e9-152">如果 ACE 拒絕對信任者的 **一般 \_ 寫入** 存取，而信任者要求 **一般 \_ 讀取** 許可權，則要求將會失敗，因為要求會隱含地包含 ACE 隱含拒絕的 **同步** 存取，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="d70e9-152">If an ACE denies **GENERIC\_WRITE** access to a trustee, and the trustee requests **GENERIC\_READ** access, the request will fail because the request implicitly includes **SYNCHRONIZE** access which is implicitly denied by the ACE, and vice versa.</span></span> <span data-ttu-id="d70e9-153">請使用允許存取的 Ace 明確地允許允許的存取權限，而不是使用拒絕存取的 Ace。</span><span class="sxs-lookup"><span data-stu-id="d70e9-153">Instead of using access-denied ACEs, use access-allowed ACEs to explicitly allow the permitted access rights.</span></span>

<span data-ttu-id="d70e9-154">管理儲存體物件存取的另一種方式是加密。</span><span class="sxs-lookup"><span data-stu-id="d70e9-154">Another means of managing access to storage objects is encryption.</span></span> <span data-ttu-id="d70e9-155">在 Windows 中執行檔案系統加密是加密檔案系統（EFS）。</span><span class="sxs-lookup"><span data-stu-id="d70e9-155">The implementation of file system encryption in Windows is the Encrypted File System, or EFS.</span></span> <span data-ttu-id="d70e9-156">EFS 只會加密檔案而非目錄。</span><span class="sxs-lookup"><span data-stu-id="d70e9-156">EFS encrypts only files and not directories.</span></span> <span data-ttu-id="d70e9-157">加密的優點是，它可為套用在媒體上的檔案提供額外的保護，而不是透過檔案系統和標準的 Windows 存取控制架構。</span><span class="sxs-lookup"><span data-stu-id="d70e9-157">The advantage of encryption is that it provides additional protection to files that is applied on the media and not through the file system and the standard Windows access control architecture.</span></span> <span data-ttu-id="d70e9-158">如需檔案加密的詳細資訊，請參閱檔案 [加密](file-encryption.md)。</span><span class="sxs-lookup"><span data-stu-id="d70e9-158">For more information on file encryption, see [File Encryption](file-encryption.md).</span></span>

<span data-ttu-id="d70e9-159">在大部分的情況下，讀取和寫入檔案或目錄物件之安全性設定的功能，會限制為核心模式進程。</span><span class="sxs-lookup"><span data-stu-id="d70e9-159">In most cases, the ability to read and write the security settings of a file or directory object is restricted to kernel-mode processes.</span></span> <span data-ttu-id="d70e9-160">很明顯地，您不希望任何使用者進程都能變更私人檔案或目錄的擁有權或存取限制。</span><span class="sxs-lookup"><span data-stu-id="d70e9-160">Clearly, you would not want any user process to be able to change the ownership or access restriction on your private file or directory.</span></span> <span data-ttu-id="d70e9-161">但是，如果您在檔案或目錄上放置的存取限制不允許應用程式的使用者模式進程讀取，則備份應用程式無法完成其備份檔案的作業。</span><span class="sxs-lookup"><span data-stu-id="d70e9-161">However, a backup application would not be able to complete its job of backing up your file if the access restrictions you have placed on your file or directory does not allow the application's user-mode process to read it.</span></span> <span data-ttu-id="d70e9-162">備份應用程式必須能夠覆寫檔案和目錄物件的安全性設定，以確保完整備份。</span><span class="sxs-lookup"><span data-stu-id="d70e9-162">Backup applications must be able to override the security settings of file and directory objects to ensure a complete backup.</span></span> <span data-ttu-id="d70e9-163">同樣地，如果備份應用程式嘗試透過磁片常駐複本來寫入檔案的備份副本，而您明確拒絕備份應用程式處理常式的寫入權限，則還原作業無法完成。</span><span class="sxs-lookup"><span data-stu-id="d70e9-163">Similarly, if a backup application attempts to write a backup copy of your file over the disk-resident copy, and you explicitly deny write privileges to the backup application process, the restore operation cannot complete.</span></span> <span data-ttu-id="d70e9-164">在此情況下，備份應用程式也必須能夠覆寫檔案的存取控制設定。</span><span class="sxs-lookup"><span data-stu-id="d70e9-164">In this case also, the backup application must be able to override the access control settings of your file.</span></span>

<span data-ttu-id="d70e9-165">「 **Se \_ 備份 \_ 名稱** 」和「 **se \_ 還原 \_ 名稱** 」存取權限是特別建立來提供備份應用程式的能力。</span><span class="sxs-lookup"><span data-stu-id="d70e9-165">The **SE\_BACKUP\_NAME** and **SE\_RESTORE\_NAME** access privileges were specifically created to provide this ability to backup applications.</span></span> <span data-ttu-id="d70e9-166">如果已在備份應用程式處理常式的存取權杖中授與並啟用這些許可權，則可以呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 開啟您的檔案或目錄進行備份，並將標準的 **讀取 \_ 控制** 存取權指定為 *dwDesiredAccess* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="d70e9-166">If these privileges have been granted and enabled in the access token of the backup application process, it can then call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open your file or directory for backup, specifying the standard **READ\_CONTROL** access right as the value of the *dwDesiredAccess* parameter.</span></span> <span data-ttu-id="d70e9-167">不過，若要將呼叫進程識別為備份程式，呼叫 **CreateFile** 必須在 *dwFlagsAndAttributes* 參數中包含檔案 **旗標 \_ \_ 備份 \_ 語義** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d70e9-167">However, to identify the calling process as a backup process, the call to **CreateFile** must include the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag in the *dwFlagsAndAttributes* parameter.</span></span> <span data-ttu-id="d70e9-168">函式呼叫的完整語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="d70e9-168">The full syntax of the function call is the following:</span></span>


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



<span data-ttu-id="d70e9-169">這可讓備份應用程式進程開啟您的檔案，並覆寫標準安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="d70e9-169">This will allow the backup application process to open your file and override the standard security checking.</span></span> <span data-ttu-id="d70e9-170">若要還原您的檔案，在開啟要寫入的檔案時，備份應用程式會使用下列 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 呼叫語法。</span><span class="sxs-lookup"><span data-stu-id="d70e9-170">To restore your file, the backup application would use the following [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) call syntax when opening your file to be written.</span></span>


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



<span data-ttu-id="d70e9-171">在某些情況下，備份應用程式必須能夠變更檔案或目錄的存取控制設定。</span><span class="sxs-lookup"><span data-stu-id="d70e9-171">There are situations when a backup application must be able to change the access control settings of a file or directory.</span></span> <span data-ttu-id="d70e9-172">例如，當檔案或目錄之磁片常駐複本的存取控制設定與備份複本不同時。</span><span class="sxs-lookup"><span data-stu-id="d70e9-172">An example is when the access control settings of the disk-resident copy of a file or directory is different from the backup copy.</span></span> <span data-ttu-id="d70e9-173">如果在備份檔案案或目錄之後變更這些設定，或已損毀，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d70e9-173">This would happen if these settings were changed after the file or directory was backed up, or if it was corrupted.</span></span>

<span data-ttu-id="d70e9-174">對 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的呼叫中指定的檔案 **\_ 旗標 \_ 備份 \_ 語義** 旗標，會提供備份應用程式處理許可權，以讀取檔案或目錄的存取控制設定。</span><span class="sxs-lookup"><span data-stu-id="d70e9-174">The **FILE\_FLAG\_BACKUP\_SEMANTICS** flag specified in the call to [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) gives the backup application process permission to read the access-control settings of the file or directory.</span></span> <span data-ttu-id="d70e9-175">有了這個許可權之後，備份應用程式進程就可以呼叫 [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) 和 [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) ，以讀取和重設存取控制設定。</span><span class="sxs-lookup"><span data-stu-id="d70e9-175">With this permission, the backup application process can then call [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) and [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) to read and than reset the access-control settings.</span></span>

<span data-ttu-id="d70e9-176">如果備份應用程式必須具有系統層級 [存取控制設定](/windows/desktop/SecAuthZ/access-control-lists)的存取權，則必須在傳遞至 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)的 *dwDesiredAccess* 參數值中指定「**存取 \_ 系統」 \_ 安全性** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d70e9-176">If a backup application must have access to the system-level [access control settings](/windows/desktop/SecAuthZ/access-control-lists), the **ACCESS\_SYSTEM\_SECURITY** flag must be specified in the *dwDesiredAccess* parameter value passed to [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>

<span data-ttu-id="d70e9-177">備份應用程式會呼叫 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ，以讀取為還原作業指定的檔案和目錄，並 [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) 寫入這些檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="d70e9-177">Backup applications call [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) to read the files and directories specified for the restore operation, and [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) to write them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d70e9-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="d70e9-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d70e9-179">標準存取權限</span><span class="sxs-lookup"><span data-stu-id="d70e9-179">standard access rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
