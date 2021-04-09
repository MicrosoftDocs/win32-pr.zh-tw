---
description: 提供虛擬硬碟的設定資料。
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112293"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="e74ca-103">Msvm \_ VirtualHardDiskSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="e74ca-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="e74ca-104">提供虛擬硬碟的設定資料。</span><span class="sxs-lookup"><span data-stu-id="e74ca-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="e74ca-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e74ca-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e74ca-106">語法</span><span class="sxs-lookup"><span data-stu-id="e74ca-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="e74ca-107">成員</span><span class="sxs-lookup"><span data-stu-id="e74ca-107">Members</span></span>

<span data-ttu-id="e74ca-108">**Msvm \_ VirtualHardDiskSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e74ca-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e74ca-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e74ca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e74ca-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e74ca-110">Properties</span></span>

<span data-ttu-id="e74ca-111">**Msvm \_ VirtualHardDiskSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e74ca-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e74ca-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e74ca-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e74ca-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-115">虛擬硬碟使用的區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e74ca-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="e74ca-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e74ca-119">A short description of the object.</span></span> <span data-ttu-id="e74ca-120">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「虛擬硬碟設定資料」。</span><span class="sxs-lookup"><span data-stu-id="e74ca-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-121">**DataAlignment**</span><span class="sxs-lookup"><span data-stu-id="e74ca-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-122">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e74ca-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-123">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-124">針對虛擬磁片的資料裝載，指定所需的對齊（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="e74ca-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="e74ca-125">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e74ca-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="e74ca-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-129">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e74ca-129">A description of the object.</span></span> <span data-ttu-id="e74ca-130">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「設定虛擬硬碟的資料」。</span><span class="sxs-lookup"><span data-stu-id="e74ca-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e74ca-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-134">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e74ca-134">A display name for the object.</span></span> <span data-ttu-id="e74ca-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="e74ca-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-136">**格式**</span><span class="sxs-lookup"><span data-stu-id="e74ca-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e74ca-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-139">虛擬硬碟的格式。</span><span class="sxs-lookup"><span data-stu-id="e74ca-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="e74ca-140">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e74ca-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="e74ca-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2) </span><span class="sxs-lookup"><span data-stu-id="e74ca-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="e74ca-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3) </span><span class="sxs-lookup"><span data-stu-id="e74ca-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="e74ca-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4) </span><span class="sxs-lookup"><span data-stu-id="e74ca-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="e74ca-144">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e74ca-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e74ca-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-148">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="e74ca-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-149">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="e74ca-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e74ca-150">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e74ca-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-151">**IsPmemCompatible**</span><span class="sxs-lookup"><span data-stu-id="e74ca-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-152">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e74ca-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-154">指定是否可使用虛擬磁片做為持續性記憶體裝置的備份存放區。</span><span class="sxs-lookup"><span data-stu-id="e74ca-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="e74ca-155">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="e74ca-156">**LogicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="e74ca-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e74ca-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-159">虛擬硬碟使用的邏輯磁區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e74ca-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="e74ca-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-161">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e74ca-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-163">虛擬機器可看見的虛擬硬碟大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e74ca-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="e74ca-164">此大小將會四捨五入到磁區大小的下一個最大倍數。</span><span class="sxs-lookup"><span data-stu-id="e74ca-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-165">**ParentIdentifier**</span><span class="sxs-lookup"><span data-stu-id="e74ca-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-168">用來唯一識別虛擬硬碟父系的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e74ca-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="e74ca-169">如果虛擬硬碟沒有父系，則此欄位為空白。</span><span class="sxs-lookup"><span data-stu-id="e74ca-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="e74ca-170">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e74ca-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="e74ca-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-174">虛擬硬碟的父系。</span><span class="sxs-lookup"><span data-stu-id="e74ca-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="e74ca-175">如果虛擬硬碟沒有父系，則這個屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="e74ca-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-176">**ParentTimestamp**</span><span class="sxs-lookup"><span data-stu-id="e74ca-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-177">資料類型： **DATETIME**</span><span class="sxs-lookup"><span data-stu-id="e74ca-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e74ca-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-179">虛擬硬碟父系的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e74ca-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="e74ca-180">如果虛擬硬碟沒有父系，則此欄位為空白。</span><span class="sxs-lookup"><span data-stu-id="e74ca-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="e74ca-181">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="e74ca-182">**路徑**</span><span class="sxs-lookup"><span data-stu-id="e74ca-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-185">虛擬硬碟的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e74ca-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-186">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="e74ca-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e74ca-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-189">虛擬硬碟使用的實體磁區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e74ca-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e74ca-190">**PmemAddressAbstractionType**</span><span class="sxs-lookup"><span data-stu-id="e74ca-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e74ca-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-193">要搭配此虛擬磁片使用的持續性記憶體位址抽象方法。</span><span class="sxs-lookup"><span data-stu-id="e74ca-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="e74ca-194">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="e74ca-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e74ca-195">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="e74ca-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="e74ca-196">**.Btt** (1) </span><span class="sxs-lookup"><span data-stu-id="e74ca-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e74ca-197">**未知** 的 (65535) </span><span class="sxs-lookup"><span data-stu-id="e74ca-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e74ca-198">**型別**</span><span class="sxs-lookup"><span data-stu-id="e74ca-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e74ca-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-200">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-201">虛擬硬碟的類型。</span><span class="sxs-lookup"><span data-stu-id="e74ca-201">The type of virtual hard disk.</span></span> <span data-ttu-id="e74ca-202">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e74ca-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="e74ca-203">已 **修正** (2) </span><span class="sxs-lookup"><span data-stu-id="e74ca-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="e74ca-204">**Dynamic** (3) </span><span class="sxs-lookup"><span data-stu-id="e74ca-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="e74ca-205">**差異** (4) </span><span class="sxs-lookup"><span data-stu-id="e74ca-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e74ca-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="e74ca-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e74ca-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e74ca-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e74ca-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e74ca-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e74ca-209">用來唯一識別虛擬磁片的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e74ca-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="e74ca-210">當 [**Msvm \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) 方法傳回 **Msvm \_ VirtualHardDiskSettingData** 的實例時，用戶端可以使用此屬性來取得 VHD 的唯一磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="e74ca-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="e74ca-211">在衝突偵測或其他情況下，用戶端可以將 **VirtualDiskId** 值設定為新的 GUID，並將此 **Msvm \_ VirtualHardDiskSettingData** 實例傳遞至 [**Msvm \_ ImageManagementService. SETVIRTUALHARDDISKSETTINGDATA**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) 方法來變更 VHD 的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="e74ca-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="e74ca-212">如果 VHD 不是 VHDX VHD，或 VHD 已附加，則作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="e74ca-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="e74ca-213">如果傳遞的值格式不正確，也就是不是 GUID 或全部都是0，則作業也會失敗。</span><span class="sxs-lookup"><span data-stu-id="e74ca-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="e74ca-214">如果傳遞的值與目前的磁片識別碼相同，則作業會以無訊息模式成功。</span><span class="sxs-lookup"><span data-stu-id="e74ca-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="e74ca-215">[**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation)函式所產生的錯誤會透過這個屬性向上反升。</span><span class="sxs-lookup"><span data-stu-id="e74ca-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="e74ca-216">用戶端也可以使用相同的機制，透過相同命名空間中的 [**Msvm \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md)方法，在建立 VHD 時提供 **VirtualDiskId** 值。</span><span class="sxs-lookup"><span data-stu-id="e74ca-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="e74ca-217">這可以用來建立 VHD1 或 VHD2 Vhd。</span><span class="sxs-lookup"><span data-stu-id="e74ca-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="e74ca-218">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="e74ca-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e74ca-219">規格需求</span><span class="sxs-lookup"><span data-stu-id="e74ca-219">Requirements</span></span>



| <span data-ttu-id="e74ca-220">需求</span><span class="sxs-lookup"><span data-stu-id="e74ca-220">Requirement</span></span> | <span data-ttu-id="e74ca-221">值</span><span class="sxs-lookup"><span data-stu-id="e74ca-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e74ca-222">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e74ca-222">Minimum supported client</span></span><br/> | <span data-ttu-id="e74ca-223">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e74ca-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e74ca-224">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e74ca-224">Minimum supported server</span></span><br/> | <span data-ttu-id="e74ca-225">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e74ca-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e74ca-226">命名空間</span><span class="sxs-lookup"><span data-stu-id="e74ca-226">Namespace</span></span><br/>                | <span data-ttu-id="e74ca-227">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e74ca-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e74ca-228">MOF</span><span class="sxs-lookup"><span data-stu-id="e74ca-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e74ca-229"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e74ca-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e74ca-230">DLL</span><span class="sxs-lookup"><span data-stu-id="e74ca-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e74ca-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e74ca-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e74ca-232">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e74ca-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74ca-233">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="e74ca-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="e74ca-234">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="e74ca-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

