---
description: 代表 GPU 磁碟分割裝置的設定狀態。
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943536"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="e771e-103">Msvm \_ GpuPartitionSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="e771e-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="e771e-104">代表 GPU 磁碟分割裝置的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="e771e-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="e771e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e771e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e771e-106">語法</span><span class="sxs-lookup"><span data-stu-id="e771e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="e771e-107">成員</span><span class="sxs-lookup"><span data-stu-id="e771e-107">Members</span></span>

<span data-ttu-id="e771e-108">**Msvm \_ GpuPartitionSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e771e-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e771e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e771e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e771e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e771e-110">Properties</span></span>

<span data-ttu-id="e771e-111">**Msvm \_ GpuPartitionSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e771e-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e771e-112">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e771e-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-115">要出現在 GPU 磁碟分割中的計算引擎數量上限。</span><span class="sxs-lookup"><span data-stu-id="e771e-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-116">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e771e-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-117">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-119">要出現在 GPU 磁碟分割中的解碼引擎量上限。</span><span class="sxs-lookup"><span data-stu-id="e771e-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-120">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e771e-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-121">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-123">在 GPU 磁碟分割中會出現的編碼引擎最大數量。</span><span class="sxs-lookup"><span data-stu-id="e771e-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-124">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e771e-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-125">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-127">要出現在 GPU 分割區中的最大 VRAM 數量。</span><span class="sxs-lookup"><span data-stu-id="e771e-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-128">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e771e-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-129">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-131">將會出現在 GPU 磁碟分割中的最小計算引擎量。</span><span class="sxs-lookup"><span data-stu-id="e771e-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-132">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e771e-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-135">將會出現在 GPU 磁碟分割中的解碼引擎最小數量。</span><span class="sxs-lookup"><span data-stu-id="e771e-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-136">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e771e-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-137">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-139">將會出現在 GPU 磁碟分割中的編碼引擎最小數量。</span><span class="sxs-lookup"><span data-stu-id="e771e-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-140">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e771e-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-143">要出現在 GPU 磁碟分割中的最小 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="e771e-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-144">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e771e-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-145">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-147">將會出現在 GPU 磁碟分割中的最佳計算引擎量。</span><span class="sxs-lookup"><span data-stu-id="e771e-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-148">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e771e-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-149">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-151">將會出現在 GPU 磁碟分割中的最佳解碼引擎量。</span><span class="sxs-lookup"><span data-stu-id="e771e-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-152">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e771e-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-153">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-155">將會出現在 GPU 磁碟分割中的最佳編碼引擎數量。</span><span class="sxs-lookup"><span data-stu-id="e771e-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e771e-156">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e771e-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e771e-157">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e771e-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e771e-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e771e-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e771e-159">將會出現在 GPU 磁碟分割中的最佳 VRAM 量。</span><span class="sxs-lookup"><span data-stu-id="e771e-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e771e-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="e771e-160">Requirements</span></span>



| <span data-ttu-id="e771e-161">需求</span><span class="sxs-lookup"><span data-stu-id="e771e-161">Requirement</span></span> | <span data-ttu-id="e771e-162">值</span><span class="sxs-lookup"><span data-stu-id="e771e-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e771e-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e771e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e771e-164">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e771e-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e771e-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e771e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e771e-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e771e-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e771e-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="e771e-167">Namespace</span></span><br/>                | <span data-ttu-id="e771e-168">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="e771e-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e771e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="e771e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e771e-170"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e771e-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e771e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="e771e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e771e-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e771e-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e771e-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e771e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e771e-174">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="e771e-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




