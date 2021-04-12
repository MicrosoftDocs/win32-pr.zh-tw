---
description: 提供現有虛擬硬碟映射的狀態資訊。
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468764"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="ecb99-103">Msvm \_ VirtualHardDiskState 類別</span><span class="sxs-lookup"><span data-stu-id="ecb99-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="ecb99-104">提供現有虛擬硬碟映射的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ecb99-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="ecb99-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb99-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb99-106">語法</span><span class="sxs-lookup"><span data-stu-id="ecb99-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="ecb99-107">成員</span><span class="sxs-lookup"><span data-stu-id="ecb99-107">Members</span></span>

<span data-ttu-id="ecb99-108">**Msvm \_ VirtualHardDiskState** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ecb99-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="ecb99-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ecb99-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecb99-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ecb99-110">Properties</span></span>

<span data-ttu-id="ecb99-111">**Msvm \_ VirtualHardDiskState** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ecb99-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ecb99-112">**對齊**</span><span class="sxs-lookup"><span data-stu-id="ecb99-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ecb99-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-115">指定虛擬硬碟的對齊類型。</span><span class="sxs-lookup"><span data-stu-id="ecb99-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="ecb99-116">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ecb99-116">This will be one of the following values.</span></span>



| <span data-ttu-id="ecb99-117">值</span><span class="sxs-lookup"><span data-stu-id="ecb99-117">Value</span></span>                                                                        | <span data-ttu-id="ecb99-118">意義</span><span class="sxs-lookup"><span data-stu-id="ecb99-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="ecb99-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ecb99-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ecb99-120">512位元組對齊。</span><span class="sxs-lookup"><span data-stu-id="ecb99-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="ecb99-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ecb99-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ecb99-122">4 KB 對齊。</span><span class="sxs-lookup"><span data-stu-id="ecb99-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ecb99-123">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ecb99-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ecb99-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-126">虛擬硬碟檔案的大小 (檔案) 所耗用的實際儲存體量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ecb99-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ecb99-127">**FragmentationPercentage**</span><span class="sxs-lookup"><span data-stu-id="ecb99-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ecb99-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-130">虛擬硬碟檔案中分散的虛擬磁片區塊百分比近似值。</span><span class="sxs-lookup"><span data-stu-id="ecb99-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="ecb99-131">**InUse**</span><span class="sxs-lookup"><span data-stu-id="ecb99-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ecb99-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-134">這個屬性保留給未來的版本使用。</span><span class="sxs-lookup"><span data-stu-id="ecb99-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ecb99-135">**MinInternalSize**</span><span class="sxs-lookup"><span data-stu-id="ecb99-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ecb99-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-138">可以壓縮虛擬硬碟的大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ecb99-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="ecb99-139">此大小會進位到磁區大小的下一個最大倍數。</span><span class="sxs-lookup"><span data-stu-id="ecb99-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="ecb99-140">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="ecb99-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ecb99-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-143">基礎實體磁片所使用的實體磁區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ecb99-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ecb99-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="ecb99-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecb99-145">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="ecb99-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="ecb99-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ecb99-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ecb99-147">虛擬硬碟的時間戳記</span><span class="sxs-lookup"><span data-stu-id="ecb99-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="ecb99-148">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="ecb99-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecb99-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecb99-149">Requirements</span></span>



| <span data-ttu-id="ecb99-150">需求</span><span class="sxs-lookup"><span data-stu-id="ecb99-150">Requirement</span></span> | <span data-ttu-id="ecb99-151">值</span><span class="sxs-lookup"><span data-stu-id="ecb99-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb99-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecb99-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb99-153">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecb99-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ecb99-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecb99-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb99-155">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecb99-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ecb99-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="ecb99-156">Namespace</span></span><br/>                | <span data-ttu-id="ecb99-157">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ecb99-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ecb99-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ecb99-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecb99-159"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ecb99-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecb99-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb99-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecb99-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ecb99-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ecb99-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecb99-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb99-163">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="ecb99-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




