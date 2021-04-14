---
description: 代表可分割 GPU。 每個 GPU 都可以分割成多個 GPU 磁碟分割，而這些分割區可指派給虛擬機器作為 vGPU。
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852379"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="371db-104">Msvm \_ PartitionableGpu 類別</span><span class="sxs-lookup"><span data-stu-id="371db-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="371db-105">代表可分割 GPU。</span><span class="sxs-lookup"><span data-stu-id="371db-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="371db-106">每個 GPU 都可以分割成多個 GPU 磁碟分割，而這些分割區可指派給虛擬機器作為 vGPU。</span><span class="sxs-lookup"><span data-stu-id="371db-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="371db-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="371db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="371db-108">語法</span><span class="sxs-lookup"><span data-stu-id="371db-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="371db-109">成員</span><span class="sxs-lookup"><span data-stu-id="371db-109">Members</span></span>

<span data-ttu-id="371db-110">**Msvm \_ PartitionableGpu** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="371db-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="371db-111">屬性</span><span class="sxs-lookup"><span data-stu-id="371db-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="371db-112">屬性</span><span class="sxs-lookup"><span data-stu-id="371db-112">Properties</span></span>

<span data-ttu-id="371db-113">**Msvm \_ PartitionableGpu** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="371db-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="371db-114">**AvailableCompute**</span><span class="sxs-lookup"><span data-stu-id="371db-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-115">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-117">將會出現在 GPU 磁碟分割中的可用計算引擎數量。</span><span class="sxs-lookup"><span data-stu-id="371db-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-118">**AvailableDecode**</span><span class="sxs-lookup"><span data-stu-id="371db-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-119">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-121">將會出現在 GPU 磁碟分割中的可用解碼引擎量。</span><span class="sxs-lookup"><span data-stu-id="371db-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-122">**AvailableEncode**</span><span class="sxs-lookup"><span data-stu-id="371db-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-123">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-125">將會出現在 GPU 磁碟分割中的可用編碼引擎數量。</span><span class="sxs-lookup"><span data-stu-id="371db-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-126">**AvailableVRAM**</span><span class="sxs-lookup"><span data-stu-id="371db-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-127">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-129">將會出現在 GPU 磁碟分割中的可用 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="371db-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-130">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="371db-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-131">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-133">要出現在 GPU 磁碟分割中的計算引擎數量上限。</span><span class="sxs-lookup"><span data-stu-id="371db-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-134">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="371db-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-137">要出現在 GPU 磁碟分割中的解碼引擎量上限。</span><span class="sxs-lookup"><span data-stu-id="371db-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-138">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="371db-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-139">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-141">在 GPU 磁碟分割中會出現的編碼引擎最大數量。</span><span class="sxs-lookup"><span data-stu-id="371db-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-142">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="371db-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-145">要出現在 GPU 分割區中的最大 VRAM 數量。</span><span class="sxs-lookup"><span data-stu-id="371db-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-146">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="371db-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-147">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-149">將會出現在 GPU 磁碟分割中的最小計算引擎量。</span><span class="sxs-lookup"><span data-stu-id="371db-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-150">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="371db-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-151">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-153">將會出現在 GPU 磁碟分割中的解碼引擎最小數量。</span><span class="sxs-lookup"><span data-stu-id="371db-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-154">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="371db-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-155">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-157">將會出現在 GPU 磁碟分割中的最小編碼引擎數量。</span><span class="sxs-lookup"><span data-stu-id="371db-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-158">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="371db-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-159">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-161">要出現在 GPU 磁碟分割中的最小 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="371db-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-162">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="371db-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-163">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-165">將會出現在 GPU 磁碟分割中的最佳計算引擎量。</span><span class="sxs-lookup"><span data-stu-id="371db-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-166">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="371db-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-167">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-169">將會出現在 GPU 磁碟分割中的最佳解碼引擎量。</span><span class="sxs-lookup"><span data-stu-id="371db-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-170">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="371db-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-171">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-173">將會出現在 GPU 磁碟分割中的最佳編碼引擎數量。</span><span class="sxs-lookup"><span data-stu-id="371db-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-174">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="371db-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-175">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-177">將會出現在 GPU 磁碟分割中的最佳 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="371db-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="371db-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="371db-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="371db-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="371db-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="371db-181">實體 GPU 分割成的 GPU 磁碟分割數量。</span><span class="sxs-lookup"><span data-stu-id="371db-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="371db-182">**TotalCompute**</span><span class="sxs-lookup"><span data-stu-id="371db-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-183">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-185">將會出現在 GPU 磁碟分割中的計算引擎總數量。</span><span class="sxs-lookup"><span data-stu-id="371db-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-186">**TotalDecode**</span><span class="sxs-lookup"><span data-stu-id="371db-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-187">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-189">將會出現在 GPU 磁碟分割中的解碼引擎總數量。</span><span class="sxs-lookup"><span data-stu-id="371db-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-190">**TotalEncode**</span><span class="sxs-lookup"><span data-stu-id="371db-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-191">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-193">將會出現在 GPU 磁碟分割中的編碼引擎總數量。</span><span class="sxs-lookup"><span data-stu-id="371db-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-194">**TotalVRAM**</span><span class="sxs-lookup"><span data-stu-id="371db-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-195">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="371db-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="371db-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="371db-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="371db-197">將出現在 GPU 磁碟分割中的總 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="371db-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="371db-198">**ValidPartitionCounts**</span><span class="sxs-lookup"><span data-stu-id="371db-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="371db-199">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="371db-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="371db-200">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="371db-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="371db-201">可將實體 GPU 分割成的有效 GPU 分割區選項陣列。</span><span class="sxs-lookup"><span data-stu-id="371db-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="371db-202">規格需求</span><span class="sxs-lookup"><span data-stu-id="371db-202">Requirements</span></span>



| <span data-ttu-id="371db-203">需求</span><span class="sxs-lookup"><span data-stu-id="371db-203">Requirement</span></span> | <span data-ttu-id="371db-204">值</span><span class="sxs-lookup"><span data-stu-id="371db-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="371db-205">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="371db-205">Minimum supported client</span></span><br/> | <span data-ttu-id="371db-206">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="371db-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="371db-207">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="371db-207">Minimum supported server</span></span><br/> | <span data-ttu-id="371db-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="371db-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="371db-209">命名空間</span><span class="sxs-lookup"><span data-stu-id="371db-209">Namespace</span></span><br/>                | <span data-ttu-id="371db-210">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="371db-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="371db-211">MOF</span><span class="sxs-lookup"><span data-stu-id="371db-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="371db-212"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="371db-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="371db-213">DLL</span><span class="sxs-lookup"><span data-stu-id="371db-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="371db-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="371db-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="371db-215">另請參閱</span><span class="sxs-lookup"><span data-stu-id="371db-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371db-216">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="371db-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




