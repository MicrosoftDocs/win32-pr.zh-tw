---
title: 使用 TB
description: 提交至 TBS 的每個命令都會與特定實體相關聯。 這是藉由建立實體的一或多個內容來完成，然後再與該實體提交的每個後續命令相關聯。
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TPM 基礎服務 TB、範例
- TPM 基礎服務 TB，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932263"
---
# <a name="using-tbs"></a><span data-ttu-id="5e3fd-106">使用 TB</span><span class="sxs-lookup"><span data-stu-id="5e3fd-106">Using TBS</span></span>

<span data-ttu-id="5e3fd-107">TPM 基本服務功能分為四個功能區域：</span><span class="sxs-lookup"><span data-stu-id="5e3fd-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="5e3fd-108">資源虛擬化</span><span class="sxs-lookup"><span data-stu-id="5e3fd-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="5e3fd-109">命令排程</span><span class="sxs-lookup"><span data-stu-id="5e3fd-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="5e3fd-110">電源管理</span><span class="sxs-lookup"><span data-stu-id="5e3fd-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="5e3fd-111">命令封鎖</span><span class="sxs-lookup"><span data-stu-id="5e3fd-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="5e3fd-112">為了確保不同的實體無法存取彼此的資源，提交至 TBS 的每個命令都會與特定實體相關聯。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="5e3fd-113">這是藉由建立實體的一或多個內容來完成，然後再與該實體提交的每個後續命令相關聯。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="5e3fd-114">每個命令都包含一個內容物件，可讓您在適當的內容底下執行最 TB 的 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="5e3fd-115">當內容關閉時，命令所建立的所有物件都會從 TPM 進行清除。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="5e3fd-116">實體會先建立內容，然後才會先存取 TB 並維護內容，直到完成執行 TBS 存取為止。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="5e3fd-117">例如，在 TSS 的案例中，TSS 的 TCG core services (TCS) 功能會在啟動時建立 TB 內容，而且會將該內容保持在作用中狀態，直到它關閉為止。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="5e3fd-118">若為 Windows Server 2008 和 Windows Vista，此 TB 會限制對系統管理員、NT 授權單位 \\ LocalService 和 NT 授權單位 NetworkService 帳戶的存取 TB API \\ 。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="5e3fd-119">根據預設，這些帳戶是唯一可連接到 TBS 和建立內容的帳戶。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="5e3fd-120">藉由使用字串 (**REG \_ SZ**) 登錄值名稱來建立登錄機碼 **存取** 權，即可修改存取限制 **SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5e3fd-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="5e3fd-121">資料類型</span><span class="sxs-lookup"><span data-stu-id="5e3fd-121">Data type</span></span>
</dt> <dd><span data-ttu-id="5e3fd-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="5e3fd-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="5e3fd-123">範例：</span><span class="sxs-lookup"><span data-stu-id="5e3fd-123">Example:</span></span>

<span data-ttu-id="5e3fd-124">**O:BAG：不正確： (A;; 0x00000001;;;BA)  (A;; 0x00000001;;;NS)  (A;; 0x00000001;;;LS)**</span><span class="sxs-lookup"><span data-stu-id="5e3fd-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="5e3fd-125">根據預設，最大值支援的內容數目是25。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="5e3fd-126">您可以藉由建立或修改 **HKEY \_ LOCAL \_ MACHINE**   \\ **Software** \\ **Microsoft** \\ **Tpm** 下名為 MaxCoNtexts 的 DWORD 登錄值來改變這個數位。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="5e3fd-127">您可以使用效能監視器工具追蹤 TBS 內容的數目，來觀察即時的 TB 內容使用狀況。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="5e3fd-128">針對 Windows 8、Windows Server 2012 和更新版本，此 TB 允許存取標準使用者和系統管理員。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="5e3fd-129">**SecurityDescriptor** 和 **MaxCoNtexts** 登錄機碼已淘汰。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="5e3fd-130">針對 Windows 8、Windows Server 2012 和更新版本，此 TB 會使用命令封鎖來限制對特定命令的存取。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="5e3fd-131">針對 Windows 10 1607 版，此 TB 允許從 AppContainer 應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="5e3fd-132">針對每個 TPM 版本，分別新增了 **BlockedAppContainerCommands** 和 **AllowedW8AppContainerCommands** 金鑰與已封鎖和允許的 TPM 命令相符的清單。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="5e3fd-133">針對 Windows 10 1803 版，將不再支援 **AllowedW8AppContainerCommands** 下的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5e3fd-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




