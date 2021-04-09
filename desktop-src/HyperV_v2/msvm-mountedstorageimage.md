---
description: 提供有關手動掛接之儲存體映射的詳細資訊。
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Msvm_MountedStorageImage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695075"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="011b3-103">Msvm \_ MountedStorageImage 類別</span><span class="sxs-lookup"><span data-stu-id="011b3-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="011b3-104">提供有關手動掛接之儲存體映射的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="011b3-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="011b3-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="011b3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="011b3-106">語法</span><span class="sxs-lookup"><span data-stu-id="011b3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="011b3-107">成員</span><span class="sxs-lookup"><span data-stu-id="011b3-107">Members</span></span>

<span data-ttu-id="011b3-108">**Msvm \_ MountedStorageImage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="011b3-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="011b3-109">方法</span><span class="sxs-lookup"><span data-stu-id="011b3-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="011b3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="011b3-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="011b3-111">方法</span><span class="sxs-lookup"><span data-stu-id="011b3-111">Methods</span></span>

<span data-ttu-id="011b3-112">**Msvm \_ MountedStorageImage** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="011b3-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="011b3-113">方法</span><span class="sxs-lookup"><span data-stu-id="011b3-113">Method</span></span>                                                                          | <span data-ttu-id="011b3-114">描述</span><span class="sxs-lookup"><span data-stu-id="011b3-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="011b3-115">**DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="011b3-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="011b3-116">卸離掛接的存放裝置映射。</span><span class="sxs-lookup"><span data-stu-id="011b3-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="011b3-117">屬性</span><span class="sxs-lookup"><span data-stu-id="011b3-117">Properties</span></span>

<span data-ttu-id="011b3-118">**Msvm \_ MountedStorageImage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="011b3-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="011b3-119">**存取**</span><span class="sxs-lookup"><span data-stu-id="011b3-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-120">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-122">用來裝載儲存體映射的存取權。</span><span class="sxs-lookup"><span data-stu-id="011b3-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="011b3-123">**唯讀** (1) </span><span class="sxs-lookup"><span data-stu-id="011b3-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="011b3-124">**讀取/寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="011b3-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="011b3-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="011b3-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-128">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="011b3-128">A short description of the object.</span></span> <span data-ttu-id="011b3-129">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律包含「掛接的儲存體映射」。</span><span class="sxs-lookup"><span data-stu-id="011b3-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="011b3-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="011b3-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-133">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="011b3-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="011b3-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-135">**說明**</span><span class="sxs-lookup"><span data-stu-id="011b3-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-138">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="011b3-138">A description of the object.</span></span> <span data-ttu-id="011b3-139">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會包含「掛接的儲存映射相關資訊」。</span><span class="sxs-lookup"><span data-stu-id="011b3-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="011b3-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="011b3-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-143">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="011b3-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="011b3-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="011b3-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-148">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="011b3-148">A display name for the object.</span></span> <span data-ttu-id="011b3-149">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律包含「掛接的儲存體映射」。</span><span class="sxs-lookup"><span data-stu-id="011b3-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="011b3-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="011b3-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-153">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="011b3-153">The current health of the element.</span></span> <span data-ttu-id="011b3-154">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="011b3-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="011b3-155">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="011b3-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="011b3-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="011b3-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="011b3-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-158">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="011b3-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-160">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="011b3-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="011b3-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="011b3-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="011b3-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="011b3-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="011b3-165">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="011b3-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="011b3-166">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="011b3-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="011b3-167">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，且一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-168">**倫**</span><span class="sxs-lookup"><span data-stu-id="011b3-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-169">資料類型： **UINT8**</span><span class="sxs-lookup"><span data-stu-id="011b3-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="011b3-171">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="011b3-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="011b3-172">SCSI 位址 LUN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="011b3-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-173">**名稱**</span><span class="sxs-lookup"><span data-stu-id="011b3-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-176">裝載之 VHD 的路徑。</span><span class="sxs-lookup"><span data-stu-id="011b3-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="011b3-177">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="011b3-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="011b3-178">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="011b3-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-181">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="011b3-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="011b3-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="011b3-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-184">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="011b3-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="011b3-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-186">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="011b3-186">The current status of the object.</span></span> <span data-ttu-id="011b3-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-188">**PathId**</span><span class="sxs-lookup"><span data-stu-id="011b3-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-189">資料類型： **UINT8**</span><span class="sxs-lookup"><span data-stu-id="011b3-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="011b3-191">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="011b3-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="011b3-192">SCSI 位址路徑識別碼。</span><span class="sxs-lookup"><span data-stu-id="011b3-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-193">**PnpDevicePath**</span><span class="sxs-lookup"><span data-stu-id="011b3-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-196">PNP 裝置路徑。</span><span class="sxs-lookup"><span data-stu-id="011b3-196">The PNP device path.</span></span>

<span data-ttu-id="011b3-197">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="011b3-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-198">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="011b3-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-199">資料類型： **UINT8**</span><span class="sxs-lookup"><span data-stu-id="011b3-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="011b3-201">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="011b3-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="011b3-202">SCSI 位址埠號碼。</span><span class="sxs-lookup"><span data-stu-id="011b3-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-203">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="011b3-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-204">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-206">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="011b3-206">Provides high level status information.</span></span> <span data-ttu-id="011b3-207">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="011b3-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="011b3-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="011b3-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-209">**狀態**</span><span class="sxs-lookup"><span data-stu-id="011b3-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="011b3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="011b3-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="011b3-213">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="011b3-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-214">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="011b3-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="011b3-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-216">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="011b3-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="011b3-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="011b3-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="011b3-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="011b3-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-219">資料類型： **UINT8**</span><span class="sxs-lookup"><span data-stu-id="011b3-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="011b3-221">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="011b3-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="011b3-222">SCSI 位址目標識別碼。</span><span class="sxs-lookup"><span data-stu-id="011b3-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="011b3-223">**型別**</span><span class="sxs-lookup"><span data-stu-id="011b3-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="011b3-224">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="011b3-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="011b3-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="011b3-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="011b3-226">裝載的儲存體映射類型。</span><span class="sxs-lookup"><span data-stu-id="011b3-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="011b3-227">**虛擬硬碟** (0) </span><span class="sxs-lookup"><span data-stu-id="011b3-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="011b3-228">**ISO 映像** (1) </span><span class="sxs-lookup"><span data-stu-id="011b3-228">**ISO Image** (1)</span></span>


<span data-ttu-id="011b3-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="011b3-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="011b3-230">備註</span><span class="sxs-lookup"><span data-stu-id="011b3-230">Remarks</span></span>

<span data-ttu-id="011b3-231">存取 **Msvm \_ MountedStorageImage** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="011b3-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="011b3-232">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="011b3-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="011b3-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="011b3-233">Requirements</span></span>



| <span data-ttu-id="011b3-234">需求</span><span class="sxs-lookup"><span data-stu-id="011b3-234">Requirement</span></span> | <span data-ttu-id="011b3-235">值</span><span class="sxs-lookup"><span data-stu-id="011b3-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="011b3-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="011b3-236">Minimum supported client</span></span><br/> | <span data-ttu-id="011b3-237">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="011b3-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="011b3-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="011b3-238">Minimum supported server</span></span><br/> | <span data-ttu-id="011b3-239">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="011b3-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="011b3-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="011b3-240">Namespace</span></span><br/>                | <span data-ttu-id="011b3-241">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="011b3-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="011b3-242">MOF</span><span class="sxs-lookup"><span data-stu-id="011b3-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="011b3-243"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="011b3-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="011b3-244">DLL</span><span class="sxs-lookup"><span data-stu-id="011b3-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="011b3-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="011b3-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="011b3-246">另請參閱</span><span class="sxs-lookup"><span data-stu-id="011b3-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011b3-247">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="011b3-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="011b3-248">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="011b3-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="011b3-249">儲存類別</span><span class="sxs-lookup"><span data-stu-id="011b3-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

