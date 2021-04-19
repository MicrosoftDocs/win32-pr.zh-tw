---
description: Windows 安全性模型可讓您控制服務控制管理員 (SCM) 和服務物件的存取權。
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: 服務安全性與存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978139"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="52844-103">服務安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-103">Service Security and Access Rights</span></span>

<span data-ttu-id="52844-104">Windows 安全性模型可讓您控制服務控制管理員 (SCM) 和服務物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="52844-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="52844-105">下列各節提供詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="52844-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="52844-106">服務控制管理員的存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="52844-107">服務的存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="52844-108">服務控制管理員的存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="52844-109">以下是 SCM 的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="52844-110">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-110">Access right</span></span>                                   | <span data-ttu-id="52844-111">Description</span><span class="sxs-lookup"><span data-stu-id="52844-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52844-112">**SC \_管理員 \_ 所有 \_ 存取** (0xF003F) </span><span class="sxs-lookup"><span data-stu-id="52844-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="52844-113">除了此資料表中的所有存取權限之外，還包含 **\_ \_ 所需的標準許可權**。</span><span class="sxs-lookup"><span data-stu-id="52844-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="52844-114">**SC \_MANAGER \_ 建立 \_ 服務** (0x0002) </span><span class="sxs-lookup"><span data-stu-id="52844-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="52844-115">需要呼叫 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式來建立服務物件，並將它加入至資料庫。</span><span class="sxs-lookup"><span data-stu-id="52844-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="52844-116">**SC \_MANAGER \_ CONNECT** (0x0001) </span><span class="sxs-lookup"><span data-stu-id="52844-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="52844-117">連接至服務控制管理員所需。</span><span class="sxs-lookup"><span data-stu-id="52844-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="52844-118">**SC \_管理員 \_ 列舉 \_ 服務** (0x0004) </span><span class="sxs-lookup"><span data-stu-id="52844-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="52844-119">需要呼叫 [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) 或 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) 函式，以列出資料庫中的服務。</span><span class="sxs-lookup"><span data-stu-id="52844-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="52844-120">在建立或刪除任何服務時，呼叫 [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) 函式以接收通知的必要項。</span><span class="sxs-lookup"><span data-stu-id="52844-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="52844-121">**SC \_管理員 \_ 鎖定** (0x0008) </span><span class="sxs-lookup"><span data-stu-id="52844-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="52844-122">需要呼叫 [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) 函數，才能取得資料庫的鎖定。</span><span class="sxs-lookup"><span data-stu-id="52844-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="52844-123">**SC \_MANAGER \_ 修改 \_ 開機 \_** 設定 (0x0020) </span><span class="sxs-lookup"><span data-stu-id="52844-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="52844-124">需要呼叫 [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) 函數。</span><span class="sxs-lookup"><span data-stu-id="52844-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="52844-125">**SC \_管理員 \_ 查詢 \_ 鎖定 \_ 狀態** (0x0010) </span><span class="sxs-lookup"><span data-stu-id="52844-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="52844-126">需要呼叫 [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) 函數，才能取得資料庫的鎖定狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="52844-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="52844-127">以下是 SCM 的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="52844-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52844-128">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-128">Access right</span></span></th>
<th><span data-ttu-id="52844-129">Description</span><span class="sxs-lookup"><span data-stu-id="52844-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52844-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="52844-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="52844-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="52844-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="52844-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52844-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="52844-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="52844-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="52844-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="52844-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52844-144">具有正確存取權限的進程可以開啟可在 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)、 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)和 [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) 函式中使用之 SCM 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="52844-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="52844-145">只有具備系統管理員許可權的進程才能開啟 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 和 [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) 函式可使用的 SCM 控制碼。</span><span class="sxs-lookup"><span data-stu-id="52844-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="52844-146">系統會建立 SCM 的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="52844-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="52844-147">若要取得或設定 SCM 的安全描述項，請使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 和 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數搭配 SCManager 物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="52844-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="52844-148">**Windows Server 2003 和 WINDOWS XP：** 與大部分其他安全物件不同的是，無法修改 SCM 的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="52844-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="52844-149">此行為已從 Windows Server 2003 Service Pack 1 (SP1) 變更。</span><span class="sxs-lookup"><span data-stu-id="52844-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="52844-150">系統會授與下列存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52844-151">帳戶</span><span class="sxs-lookup"><span data-stu-id="52844-151">Account</span></span></th>
<th><span data-ttu-id="52844-152">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52844-153">遠端驗證的使用者</span><span class="sxs-lookup"><span data-stu-id="52844-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="52844-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="52844-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-155">本機驗證的使用者 (包括 LocalService 和 NetworkService) </span><span class="sxs-lookup"><span data-stu-id="52844-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="52844-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="52844-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="52844-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="52844-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="52844-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52844-160">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="52844-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="52844-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="52844-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="52844-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="52844-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="52844-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="52844-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-166">系統管理員</span><span class="sxs-lookup"><span data-stu-id="52844-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="52844-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52844-168">請注意，透過網路驗證的遠端使用者（而不是以互動方式登入）可以連接到 SCM，但無法執行需要其他存取權限的作業。</span><span class="sxs-lookup"><span data-stu-id="52844-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="52844-169">若要執行這些作業，使用者必須以互動方式登入，或服務必須使用其中一個服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="52844-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="52844-170">**Windows Server 2003 和 WINDOWS XP：** 遠端驗證的使用者會被授與 **sc \_ manager \_ CONNECT**、 **sc \_ manager \_ 列舉 \_ 服務**、 **sc \_ manager \_ 查詢 \_ 鎖定 \_ 狀態**，以及 **標準 \_ 許可權 \_ 讀取** 存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="52844-171">從 Windows Server 2003 （含 SP1）開始，這些存取權限受限於上表所述</span><span class="sxs-lookup"><span data-stu-id="52844-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="52844-172">當進程使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來開啟已安裝服務之資料庫的控制碼時，它可以要求存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="52844-173">在授與所要求的存取權限之前，系統會針對 SCM 的安全描述項執行安全性檢查。</span><span class="sxs-lookup"><span data-stu-id="52844-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="52844-174">服務的存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-174">Access Rights for a Service</span></span>

<span data-ttu-id="52844-175">以下是服務的特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="52844-176">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-176">Access right</span></span>                                | <span data-ttu-id="52844-177">Description</span><span class="sxs-lookup"><span data-stu-id="52844-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52844-178">**服務 \_所有 \_ 存取** (0xF01FF) </span><span class="sxs-lookup"><span data-stu-id="52844-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="52844-179">除了此資料表中的所有存取權限之外，還包含 **\_ \_ 所需的標準許可權** 。</span><span class="sxs-lookup"><span data-stu-id="52844-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="52844-180">**服務 \_變更 \_ CONFIG** (0x0002) </span><span class="sxs-lookup"><span data-stu-id="52844-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="52844-181">需要呼叫 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 或 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函式來變更服務設定。</span><span class="sxs-lookup"><span data-stu-id="52844-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="52844-182">因為這會授與呼叫者變更系統所執行之可執行檔的許可權，所以只能授與系統管理員。</span><span class="sxs-lookup"><span data-stu-id="52844-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="52844-183">**服務 \_列舉相依 \_ 項** (0x0008) </span><span class="sxs-lookup"><span data-stu-id="52844-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="52844-184">需要呼叫 [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) 函式，以列舉相依于服務的所有服務。</span><span class="sxs-lookup"><span data-stu-id="52844-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="52844-185">**服務 \_查閱 (0x0080**) </span><span class="sxs-lookup"><span data-stu-id="52844-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="52844-186">需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式，才能要求服務立即報告其狀態。</span><span class="sxs-lookup"><span data-stu-id="52844-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="52844-187">**服務 \_暫停 \_ 繼續** (0x0040) </span><span class="sxs-lookup"><span data-stu-id="52844-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="52844-188">需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來暫停或繼續服務。</span><span class="sxs-lookup"><span data-stu-id="52844-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="52844-189">**服務 \_查詢 \_** 設定 (0x0001) </span><span class="sxs-lookup"><span data-stu-id="52844-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="52844-190">需要呼叫 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 和 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) 函數才能查詢服務設定。</span><span class="sxs-lookup"><span data-stu-id="52844-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="52844-191">**服務 \_查詢 \_ 狀態** (0x0004) </span><span class="sxs-lookup"><span data-stu-id="52844-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="52844-192">需要呼叫 [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) 或 [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) 函式，才能向服務控制管理員要求服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="52844-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="52844-193">當服務變更狀態時，需要呼叫 [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) 函式來接收通知。</span><span class="sxs-lookup"><span data-stu-id="52844-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="52844-194">**服務 \_開始** (0x0010) </span><span class="sxs-lookup"><span data-stu-id="52844-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="52844-195">呼叫 [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) 函式來啟動服務時所需。</span><span class="sxs-lookup"><span data-stu-id="52844-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="52844-196">**服務 \_停止** (0x0020) </span><span class="sxs-lookup"><span data-stu-id="52844-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="52844-197">需要呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來停止服務。</span><span class="sxs-lookup"><span data-stu-id="52844-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="52844-198">**服務 \_使用者 \_ 定義 \_ 控制項** (0x0100) </span><span class="sxs-lookup"><span data-stu-id="52844-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="52844-199">呼叫 [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) 函式來指定使用者定義的控制項程式碼時，需要用到。</span><span class="sxs-lookup"><span data-stu-id="52844-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="52844-200">以下是服務的 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="52844-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="52844-201">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-201">Access right</span></span>                 | <span data-ttu-id="52844-202">Description</span><span class="sxs-lookup"><span data-stu-id="52844-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52844-203">**存取 \_ 系統 \_ 安全性**</span><span class="sxs-lookup"><span data-stu-id="52844-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="52844-204">呼叫 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 或 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式以存取 SACL 的必要參數。</span><span class="sxs-lookup"><span data-stu-id="52844-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="52844-205">取得此存取權的正確方式是在呼叫端的目前存取權杖中啟用「 **SE \_ 安全性 \_ 名稱**」[**許可權**](/windows/desktop/SecAuthZ/privileges)、開啟 **存取 \_ 系統 \_ 安全性** 存取的控制碼，然後停用該許可權。</span><span class="sxs-lookup"><span data-stu-id="52844-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="52844-206">**刪除**   (0x10000) </span><span class="sxs-lookup"><span data-stu-id="52844-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="52844-207">呼叫 [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) 函數來刪除服務的必要參數。</span><span class="sxs-lookup"><span data-stu-id="52844-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="52844-208">**讀取 \_控制**  (0x20000) </span><span class="sxs-lookup"><span data-stu-id="52844-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="52844-209">呼叫 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 函數來查詢服務物件的安全描述項時，需要此項。</span><span class="sxs-lookup"><span data-stu-id="52844-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="52844-210">**寫入 \_DAC**  (0x40000) </span><span class="sxs-lookup"><span data-stu-id="52844-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="52844-211">需要呼叫 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式，才能修改服務物件安全描述項的 **Dacl** 成員。</span><span class="sxs-lookup"><span data-stu-id="52844-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="52844-212">**寫入 \_擁有** 者 (0x80000) </span><span class="sxs-lookup"><span data-stu-id="52844-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="52844-213">需要呼叫 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函式，才能修改服務物件安全描述項的 **擁有** 者和 **群組** 成員。</span><span class="sxs-lookup"><span data-stu-id="52844-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="52844-214">以下是服務的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="52844-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52844-215">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-215">Access right</span></span></th>
<th><span data-ttu-id="52844-216">Description</span><span class="sxs-lookup"><span data-stu-id="52844-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52844-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="52844-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="52844-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="52844-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="52844-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="52844-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="52844-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52844-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="52844-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="52844-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="52844-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="52844-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="52844-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="52844-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="52844-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52844-232">當 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數安裝服務時，SCM 會建立服務物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="52844-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="52844-233">服務物件的預設安全描述項會授與下列存取權。</span><span class="sxs-lookup"><span data-stu-id="52844-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="52844-234">帳戶</span><span class="sxs-lookup"><span data-stu-id="52844-234">Account</span></span></th>
<th><span data-ttu-id="52844-235">存取權限</span><span class="sxs-lookup"><span data-stu-id="52844-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="52844-236">遠端驗證的使用者</span><span class="sxs-lookup"><span data-stu-id="52844-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="52844-237">預設不會授與。<strong>Windows Server 2003 SP1： SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="52844-238"><strong>Windows Server 2003 和 WINDOWS XP：</strong> 遠端驗證使用者的存取權限與本機驗證使用者的存取權限相同。</span><span class="sxs-lookup"><span data-stu-id="52844-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-239">本機驗證的使用者 (包括 LocalService 和 NetworkService) </span><span class="sxs-lookup"><span data-stu-id="52844-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="52844-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="52844-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="52844-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="52844-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="52844-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="52844-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="52844-246">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="52844-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="52844-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="52844-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="52844-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="52844-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="52844-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="52844-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="52844-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="52844-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="52844-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="52844-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="52844-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="52844-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="52844-256">系統管理員</span><span class="sxs-lookup"><span data-stu-id="52844-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="52844-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="52844-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="52844-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="52844-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="52844-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="52844-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="52844-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="52844-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="52844-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="52844-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="52844-262">若要執行任何作業，使用者必須以互動方式登入，或服務必須使用其中一個服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="52844-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="52844-263">若要取得或設定服務物件的安全描述項，請使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 和 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數。</span><span class="sxs-lookup"><span data-stu-id="52844-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="52844-264">如需詳細資訊，請參閱 [修改服務的 DACL](modifying-the-dacl-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="52844-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="52844-265">當進程使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 函式時，系統會根據服務物件的安全描述項來檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="52844-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="52844-266">授與不受信任使用者的特定存取權限 (例如 **服務 \_ 變更 \_** 設定或 **服務 \_ 停止**) 可讓他們干擾您的服務執行，而且可能會允許他們在 LocalSystem 帳戶下執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="52844-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="52844-267">呼叫 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) 函式時，如果呼叫端沒有服務的 **服務 \_ 查詢 \_ 狀態** 存取權，則會從傳回給用戶端的服務清單中，以無訊息方式省略服務。</span><span class="sxs-lookup"><span data-stu-id="52844-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

