---
description: 限制由 WMI 用戶端所起始的作業所使用的內部資源。
ms.assetid: e877899d-2f5e-4468-8c47-055fd4d16f56
ms.tgt_platform: multiple
title: __ArbitratorConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ArbitratorConfiguration
- Root.__ArbitratorConfiguration.OutstandingTasksTotal
- Root.__ArbitratorConfiguration.OutstandingTasksPerUser
- Root.__ArbitratorConfiguration.TaskThreadsTotal
- Root.__ArbitratorConfiguration.TaskThreadsPerUser
- Root.__ArbitratorConfiguration.QuotaRetryCount
- Root.__ArbitratorConfiguration.QuotaRetryWaitInterval
- Root.__ArbitratorConfiguration.TotalUsers
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerTask
- Root.__ArbitratorConfiguration.TotalCacheMemoryPerUser
- Root.__ArbitratorConfiguration.TotalCacheMemory
- Root.__ArbitratorConfiguration.TotalCacheDiskPerTask
- Root.__ArbitratorConfiguration.TotalCacheDiskPerUser
- Root.__ArbitratorConfiguration.TotalCacheDisk
- Root.__ArbitratorConfiguration.TemporarySubscriptionsPerUser
- Root.__ArbitratorConfiguration.PermanentSubscriptionsPerUser
- Root.__ArbitratorConfiguration.PollingInstructionsPerUser
- Root.__ArbitratorConfiguration.PollingMemoryPerUser
- Root.__ArbitratorConfiguration.TemporarySubscriptionsTotal
- Root.__ArbitratorConfiguration.PermanentSubscriptionsTotal
- Root.__ArbitratorConfiguration.PollingInstructionsTotal
- Root.__ArbitratorConfiguration.PollingMemoryTotal
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 906164d6d715ed70bccecf61fba767ada622c74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193452"
---
# <a name="__arbitratorconfiguration-class"></a><span data-ttu-id="82bf1-103">\_\_ArbitratorConfiguration 類別</span><span class="sxs-lookup"><span data-stu-id="82bf1-103">\_\_ArbitratorConfiguration class</span></span>

<span data-ttu-id="82bf1-104">**\_ \_ ArbitratorConfiguration** 類別是一種設定類別，可限制由 WMI 用戶端所起始的作業所使用的內部資源。</span><span class="sxs-lookup"><span data-stu-id="82bf1-104">The **\_\_ArbitratorConfiguration** class is a configuration class that limits the internal resources that are used by operations initiated by WMI clients.</span></span> <span data-ttu-id="82bf1-105">這是位在根命名空間中的單一類別 \\ 。</span><span class="sxs-lookup"><span data-stu-id="82bf1-105">This is a singleton class that resides in the \\root namespace.</span></span> <span data-ttu-id="82bf1-106">類別會在內部產生，因此沒有任何 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="82bf1-106">The class is internally generated so there is no MOF file for it.</span></span>

<span data-ttu-id="82bf1-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="82bf1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="82bf1-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="82bf1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82bf1-109">語法</span><span class="sxs-lookup"><span data-stu-id="82bf1-109">Syntax</span></span>

``` syntax
[singleton]
class __ArbitratorConfiguration : __SystemClass
{
  uint32 OutstandingTasksTotal;
  uint32 OutstandingTasksPerUser;
  uint32 TaskThreadsTotal;
  uint32 TaskThreadsPerUser;
  uint32 QuotaRetryCount;
  uint32 QuotaRetryWaitInterval;
  uint32 TotalUsers;
  uint32 TotalCacheMemoryPerTask;
  uint32 TotalCacheMemoryPerUser;
  uint32 TotalCacheMemory;
  uint32 TotalCacheDiskPerTask;
  uint32 TotalCacheDiskPerUser;
  uint32 TotalCacheDisk;
  uint32 TemporarySubscriptionsPerUser;
  uint32 PermanentSubscriptionsPerUser;
  uint32 PollingInstructionsPerUser;
  uint32 PollingMemoryPerUser;
  uint32 TemporarySubscriptionsTotal;
  uint32 PermanentSubscriptionsTotal;
  uint32 PollingInstructionsTotal;
  uint32 PollingMemoryTotal;
};
```

## <a name="members"></a><span data-ttu-id="82bf1-110">成員</span><span class="sxs-lookup"><span data-stu-id="82bf1-110">Members</span></span>

<span data-ttu-id="82bf1-111">**\_ \_ ArbitratorConfiguration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="82bf1-111">The **\_\_ArbitratorConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="82bf1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="82bf1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82bf1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="82bf1-113">Properties</span></span>

<span data-ttu-id="82bf1-114">**\_ \_ ArbitratorConfiguration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="82bf1-114">The **\_\_ArbitratorConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82bf1-115">**OutstandingTasksPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-115">**OutstandingTasksPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-118">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-118">Unused.</span></span> <span data-ttu-id="82bf1-119">任何一次的未處理使用者起始工作數目。</span><span class="sxs-lookup"><span data-stu-id="82bf1-119">Number of outstanding user initiated tasks at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-120">**OutstandingTasksTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-120">**OutstandingTasksTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-121">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-123">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-123">Unused.</span></span> <span data-ttu-id="82bf1-124">所有未完成的工作總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-124">Total number of outstanding tasks at any time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-125">**PermanentSubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-125">**PermanentSubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-128">特定使用者一次允許的永久訂閱數目。</span><span class="sxs-lookup"><span data-stu-id="82bf1-128">Number of permanent subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-129">**PermanentSubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-129">**PermanentSubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-132">所有使用者在任何時間都允許的永久訂閱總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-132">Total number of permanent subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-133">**PollingInstructionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-133">**PollingInstructionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-136">特定使用者一次允許的輪詢事件查詢數目。</span><span class="sxs-lookup"><span data-stu-id="82bf1-136">Number of polling event queries allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-137">**PollingInstructionsTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-137">**PollingInstructionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-140">所有使用者在任何時間都允許的輪詢指令總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-140">Total number of polling instructions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-141">**PollingMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-141">**PollingMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-142">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-144">由特定使用者發出的記憶體輪詢事件查詢數量，可以在任何時間使用。</span><span class="sxs-lookup"><span data-stu-id="82bf1-144">Amount of memory polling event queries, issued by a particular user, can consume at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-145">**PollingMemoryTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-145">**PollingMemoryTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-148">針對所有合併的使用者，輪詢事件查詢的總記憶體量，可以在任何時間使用。</span><span class="sxs-lookup"><span data-stu-id="82bf1-148">Total amount of memory that polling event queries, for all users combined, can consumer at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-149">**QuotaRetryCount**</span><span class="sxs-lookup"><span data-stu-id="82bf1-149">**QuotaRetryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-152">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-152">Unused.</span></span> <span data-ttu-id="82bf1-153">取消工作之前允許的配額違規數目。</span><span class="sxs-lookup"><span data-stu-id="82bf1-153">Number of quota violations permitted before a task is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-154">**QuotaRetryWaitInterval**</span><span class="sxs-lookup"><span data-stu-id="82bf1-154">**QuotaRetryWaitInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-157">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-157">Unused.</span></span> <span data-ttu-id="82bf1-158">針對每個配額違規引進工作執行的延遲。</span><span class="sxs-lookup"><span data-stu-id="82bf1-158">Delay introduced into the task execution on each quota violation.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-159">**TaskThreadsPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-159">**TaskThreadsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-162">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-162">Unused.</span></span> <span data-ttu-id="82bf1-163">與特定使用者相關聯的工作執行緒數目上限。</span><span class="sxs-lookup"><span data-stu-id="82bf1-163">Maximum number of task threads associated with a particular user t any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-164">**TaskThreadsTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-164">**TaskThreadsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-167">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-167">Unused.</span></span> <span data-ttu-id="82bf1-168">工作執行緒數目上限。</span><span class="sxs-lookup"><span data-stu-id="82bf1-168">Maximum number of task threads.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-169">**TemporarySubscriptionsPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-169">**TemporarySubscriptionsPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-172">特定使用者一次允許的臨時訂閱數目。</span><span class="sxs-lookup"><span data-stu-id="82bf1-172">Number of temporary subscriptions allowed for a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-173">**TemporarySubscriptionsTotal**</span><span class="sxs-lookup"><span data-stu-id="82bf1-173">**TemporarySubscriptionsTotal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-176">所有使用者在任何時間都允許的臨時訂閱總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-176">Total number of temporary subscriptions allowed for all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-177">**TotalCacheDisk**</span><span class="sxs-lookup"><span data-stu-id="82bf1-177">**TotalCacheDisk**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-178">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-180">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-180">Unused.</span></span> <span data-ttu-id="82bf1-181">任何一次與所有使用者相關聯的磁碟快取總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-181">Total disk cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-182">**TotalCacheDiskPerTask**</span><span class="sxs-lookup"><span data-stu-id="82bf1-182">**TotalCacheDiskPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-185">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-185">Unused.</span></span> <span data-ttu-id="82bf1-186">一次與特定工作相關聯的磁碟快取總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-186">Total disk cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-187">**TotalCacheDiskPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-187">**TotalCacheDiskPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-188">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-190">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-190">Unused.</span></span> <span data-ttu-id="82bf1-191">與特定使用者一次相關聯的磁碟快取總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-191">Total disk cache associated with a particular user at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-192">**TotalCacheMemory**</span><span class="sxs-lookup"><span data-stu-id="82bf1-192">**TotalCacheMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-195">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-195">Unused.</span></span> <span data-ttu-id="82bf1-196">任何一次與所有使用者相關聯的總記憶體快取。</span><span class="sxs-lookup"><span data-stu-id="82bf1-196">Total memory cache associated with all users at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-197">**TotalCacheMemoryPerTask**</span><span class="sxs-lookup"><span data-stu-id="82bf1-197">**TotalCacheMemoryPerTask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-200">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-200">Unused.</span></span> <span data-ttu-id="82bf1-201">一次與特定工作相關聯的記憶體快取總計。</span><span class="sxs-lookup"><span data-stu-id="82bf1-201">Total memory cache associated with a particular task at any one time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-202">**TotalCacheMemoryPerUser**</span><span class="sxs-lookup"><span data-stu-id="82bf1-202">**TotalCacheMemoryPerUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-205">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-205">Unused.</span></span> <span data-ttu-id="82bf1-206">與特定使用者在任何時候相關聯的記憶體快取總數。</span><span class="sxs-lookup"><span data-stu-id="82bf1-206">Total memory cache associated with a particular user at anyone time.</span></span>

</dd> <dt>

<span data-ttu-id="82bf1-207">**TotalUsers**</span><span class="sxs-lookup"><span data-stu-id="82bf1-207">**TotalUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82bf1-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="82bf1-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82bf1-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="82bf1-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82bf1-210">未使用的。</span><span class="sxs-lookup"><span data-stu-id="82bf1-210">Unused.</span></span> <span data-ttu-id="82bf1-211">已連線的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="82bf1-211">Maximum number of connected users.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82bf1-212">備註</span><span class="sxs-lookup"><span data-stu-id="82bf1-212">Remarks</span></span>

<span data-ttu-id="82bf1-213">**\_ \_ ArbitratorConfiguration** 繼承自 [**\_ \_ SystemClass**](--systemclass.md)。</span><span class="sxs-lookup"><span data-stu-id="82bf1-213">**\_\_ArbitratorConfiguration** is inherited from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82bf1-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="82bf1-214">Requirements</span></span>



| <span data-ttu-id="82bf1-215">需求</span><span class="sxs-lookup"><span data-stu-id="82bf1-215">Requirement</span></span> | <span data-ttu-id="82bf1-216">值</span><span class="sxs-lookup"><span data-stu-id="82bf1-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="82bf1-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82bf1-217">Minimum supported client</span></span><br/> | <span data-ttu-id="82bf1-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82bf1-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="82bf1-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82bf1-219">Minimum supported server</span></span><br/> | <span data-ttu-id="82bf1-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82bf1-220">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="82bf1-221">命名空間</span><span class="sxs-lookup"><span data-stu-id="82bf1-221">Namespace</span></span><br/>                | <span data-ttu-id="82bf1-222">Root</span><span class="sxs-lookup"><span data-stu-id="82bf1-222">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="82bf1-223">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82bf1-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82bf1-224">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="82bf1-224">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="82bf1-225">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="82bf1-225">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

