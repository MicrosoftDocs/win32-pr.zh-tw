---
description: 允許在主機進程使用系統資源時設定限制。
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: __ProviderHostQuotaConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193067"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="93336-103">\_\_ProviderHostQuotaConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="93336-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="93336-104">**\_ \_ ProviderHostQuotaConfiguration** 系統類別是主機提供者進程的設定類別。</span><span class="sxs-lookup"><span data-stu-id="93336-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="93336-105">此類別位於根命名空間中，並允許在主機進程使用系統資源時設定限制。</span><span class="sxs-lookup"><span data-stu-id="93336-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="93336-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="93336-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="93336-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="93336-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93336-108">語法</span><span class="sxs-lookup"><span data-stu-id="93336-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="93336-109">成員</span><span class="sxs-lookup"><span data-stu-id="93336-109">Members</span></span>

<span data-ttu-id="93336-110">**\_ \_ ProviderHostQuotaConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93336-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="93336-111">屬性</span><span class="sxs-lookup"><span data-stu-id="93336-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93336-112">屬性</span><span class="sxs-lookup"><span data-stu-id="93336-112">Properties</span></span>

<span data-ttu-id="93336-113">**\_ \_ ProviderHostQuotaConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93336-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93336-114">**HandlesPerHost**</span><span class="sxs-lookup"><span data-stu-id="93336-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93336-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93336-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93336-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93336-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93336-117">每個主機可以有的核心物件控制碼數目。</span><span class="sxs-lookup"><span data-stu-id="93336-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="93336-118">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="93336-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93336-119">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="93336-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93336-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93336-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93336-121">所有主機可以保留的私用記憶體（以位元組為單位）組合。</span><span class="sxs-lookup"><span data-stu-id="93336-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="93336-122">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="93336-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="93336-123">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="93336-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93336-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="93336-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93336-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93336-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93336-126">每部主機可以保留的私用記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="93336-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="93336-127">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="93336-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="93336-128">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="93336-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93336-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93336-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93336-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93336-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93336-131">可以同時執行的主控制項進程總數。</span><span class="sxs-lookup"><span data-stu-id="93336-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="93336-132">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="93336-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93336-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93336-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93336-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93336-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93336-135">任何一部主機擁有的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="93336-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93336-136">備註</span><span class="sxs-lookup"><span data-stu-id="93336-136">Remarks</span></span>

<span data-ttu-id="93336-137">代表限制的屬性可以變更，但因為此類別是單一類別，所以所有提供者主機都會共用相同的限制。</span><span class="sxs-lookup"><span data-stu-id="93336-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="93336-138">設定主機工作物件的工作物件限制時，會使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="93336-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="93336-139">**MemoryAllHosts**</span><span class="sxs-lookup"><span data-stu-id="93336-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="93336-140">**MemoryPerHost**</span><span class="sxs-lookup"><span data-stu-id="93336-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="93336-141">**ProcessLimitAllHosts**</span><span class="sxs-lookup"><span data-stu-id="93336-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="93336-142">**ThreadsPerHost**</span><span class="sxs-lookup"><span data-stu-id="93336-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="93336-143">如果違反 **HandlesPerHost** 配額，主機進程會輪詢處理常式的使用，並結束進程。</span><span class="sxs-lookup"><span data-stu-id="93336-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="93336-144">這些值的變更會在電腦重新開機之後生效。</span><span class="sxs-lookup"><span data-stu-id="93336-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="93336-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="93336-145">Requirements</span></span>



| <span data-ttu-id="93336-146">需求</span><span class="sxs-lookup"><span data-stu-id="93336-146">Requirement</span></span> | <span data-ttu-id="93336-147">值</span><span class="sxs-lookup"><span data-stu-id="93336-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="93336-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93336-148">Minimum supported client</span></span><br/> | <span data-ttu-id="93336-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93336-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="93336-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93336-150">Minimum supported server</span></span><br/> | <span data-ttu-id="93336-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93336-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="93336-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="93336-152">Namespace</span></span><br/>                | <span data-ttu-id="93336-153">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="93336-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="93336-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93336-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93336-155">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="93336-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="93336-156">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="93336-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

