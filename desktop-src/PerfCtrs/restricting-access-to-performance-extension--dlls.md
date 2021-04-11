---
description: 從 Windows Server 2003 開始，效能監視器 Users 群組和 Performance Log Users 群組可供效能 Dll 的開發人員和使用者使用，以及效能資料協助程式 (PDH) API 功能。
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: 限制對效能延伸模組 Dll 的存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849278"
---
# <a name="restricting-access-to-performance-extension-dlls"></a><span data-ttu-id="93e7d-103">限制對效能延伸模組 Dll 的存取</span><span class="sxs-lookup"><span data-stu-id="93e7d-103">Restricting Access to Performance Extension DLLs</span></span>

<span data-ttu-id="93e7d-104">從 Windows Server 2003 開始，效能監視器 Users 群組和 Performance Log Users 群組可供效能 Dll 的開發人員和使用者使用，以及效能資料協助程式 (PDH) API 功能。</span><span class="sxs-lookup"><span data-stu-id="93e7d-104">Beginning with Windows Server 2003, the Performance Monitor Users group and the Performance Log Users group were made available to developers and users of performance DLLs and the Performance Data Helper (PDH) API functions.</span></span> <span data-ttu-id="93e7d-105">這些效能安全性群組可供系統管理員使用，以限制對特定使用者清單的效能 Dll 所公開的資訊存取。</span><span class="sxs-lookup"><span data-stu-id="93e7d-105">These performance security groups are intended for use by system administrators in restricting access to the information exposed by performance DLLs to a specific list of users.</span></span>

<span data-ttu-id="93e7d-106">效能監視器 Users 群組旨在包含可查看計數器資料的使用者，而不使用效能記錄檔及警示服務記錄計數器資料。</span><span class="sxs-lookup"><span data-stu-id="93e7d-106">The Performance Monitor Users group is intended to include users that view counter data and do not log counter data using the Performance Logs and Alerts service.</span></span> <span data-ttu-id="93e7d-107">Performance Log Users 群組應該包含有權使用效能記錄檔和警示服務的使用者，以便在本機或遠端伺服器上記錄計數器。</span><span class="sxs-lookup"><span data-stu-id="93e7d-107">The Performance Log Users group should include users that have permission to use the Performance Logs and Alert service to log counters on the local or remote server.</span></span> <span data-ttu-id="93e7d-108">此群組的許可權也包括在本機或遠端系統上建立記錄檔、使用警示服務，以及在服務中執行程式。</span><span class="sxs-lookup"><span data-stu-id="93e7d-108">Privileges of this group also include creating log files on local or remote systems, using the alerts service, and running programs as part of the service.</span></span>

<span data-ttu-id="93e7d-109">請注意，這些效能安全性群組本身並不是存取限制機制。</span><span class="sxs-lookup"><span data-stu-id="93e7d-109">Note that these performance security groups are not by themselves an access restriction mechanism.</span></span> <span data-ttu-id="93e7d-110">您必須使用這些群組搭配 Windows 物件存取控制模型來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="93e7d-110">You must use these groups with the Windows object access-control model to do this.</span></span>

<span data-ttu-id="93e7d-111">大部分的應用程式會透過 IPC 機制（通常是共用記憶體）與效能 DLL 通訊。</span><span class="sxs-lookup"><span data-stu-id="93e7d-111">Most applications communicate with the performance DLL through an IPC mechanism, typically shared memory.</span></span> <span data-ttu-id="93e7d-112">因此，您可以將效能安全性群組的成員新增至共用記憶體物件的安全描述項，以將 DLL 的存取限制為安全性群組的成員。</span><span class="sxs-lookup"><span data-stu-id="93e7d-112">Therefore, you can add the members of a performance security group to the security descriptor of the shared memory object to restrict access to the DLL to those members of the security group.</span></span> <span data-ttu-id="93e7d-113">執行這項操作時，您也必須將群組成員加入至效能 DLL 所存取之系統物件的安全描述項，以便提供計數器資料，例如記錄檔和資料夾。</span><span class="sxs-lookup"><span data-stu-id="93e7d-113">When doing this, you must also add the group members to the security descriptor of the system objects that the performance DLL accesses in order to provide counter data, for example, log files and folders.</span></span> <span data-ttu-id="93e7d-114">如需將 Acl 新增至物件安全描述項的詳細資訊，請參閱 [修改物件的 acl](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="93e7d-114">For more detailed information on adding ACLs to object security descriptors, refer to [Modifying an Object's ACL](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).</span></span>

<span data-ttu-id="93e7d-115">您可以用來修改 IPC 系統物件安全描述項之 ACL 資訊的另一種方法，就是指定具有安全描述項定義語言 (SDDL) 的「效能安全性群組」清單成員，然後呼叫 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 來建立安全描述項。</span><span class="sxs-lookup"><span data-stu-id="93e7d-115">Another method you can use to modify the ACL information of an IPC system object's security descriptor is to specify the members of the performance security group list with Security Descriptor Definition Language (SDDL) and call [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) to create the security descriptor.</span></span> <span data-ttu-id="93e7d-116">接著會將此安全描述項附加至 IPC 系統物件。</span><span class="sxs-lookup"><span data-stu-id="93e7d-116">This security descriptor is then attached to the IPC system object.</span></span> <span data-ttu-id="93e7d-117">以下顯示的 SDDL 字串包含效能監視器 Users 群組、MU 和 Performance Log Users 群組（LU）。</span><span class="sxs-lookup"><span data-stu-id="93e7d-117">The following shows an SDDL string that includes the Performance Monitor Users group, MU, and the Performance Log Users group, LU.</span></span>

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
