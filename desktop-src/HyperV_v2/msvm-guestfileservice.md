---
description: Msvm \_ GuestFileService 包含一個方法，可用來將檔案從 hyper-v 主機複製到虛擬機器。
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Msvm_GuestFileService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991809"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="653ef-103">Msvm \_ GuestFileService 類別</span><span class="sxs-lookup"><span data-stu-id="653ef-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="653ef-104">**Msvm \_GuestFileService** 包含可用於將檔案從 hyper-v 主機複製到虛擬機器的方法。</span><span class="sxs-lookup"><span data-stu-id="653ef-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="653ef-105">這個類別衍生自 [**Msvm \_ GuestService**](msvm-guestservice.md)。</span><span class="sxs-lookup"><span data-stu-id="653ef-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="653ef-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="653ef-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="653ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="653ef-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="653ef-108">成員</span><span class="sxs-lookup"><span data-stu-id="653ef-108">Members</span></span>

<span data-ttu-id="653ef-109">**Msvm \_ GuestFileService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="653ef-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="653ef-110">方法</span><span class="sxs-lookup"><span data-stu-id="653ef-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="653ef-111">屬性</span><span class="sxs-lookup"><span data-stu-id="653ef-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="653ef-112">方法</span><span class="sxs-lookup"><span data-stu-id="653ef-112">Methods</span></span>

<span data-ttu-id="653ef-113">**Msvm \_ GuestFileService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="653ef-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="653ef-114">方法</span><span class="sxs-lookup"><span data-stu-id="653ef-114">Method</span></span>                                                             | <span data-ttu-id="653ef-115">描述</span><span class="sxs-lookup"><span data-stu-id="653ef-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="653ef-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="653ef-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="653ef-117">將檔案從 Hyper-v 主機複製到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="653ef-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="653ef-118">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="653ef-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="653ef-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="653ef-119">**StartService**</span></span>                                                   | <span data-ttu-id="653ef-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="653ef-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="653ef-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="653ef-121">**StopService**</span></span>                                                    | <span data-ttu-id="653ef-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="653ef-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="653ef-123">屬性</span><span class="sxs-lookup"><span data-stu-id="653ef-123">Properties</span></span>

<span data-ttu-id="653ef-124">**Msvm \_ GuestFileService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="653ef-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="653ef-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="653ef-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-128">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="653ef-128">Short textual description of the object.</span></span> <span data-ttu-id="653ef-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="653ef-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="653ef-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="653ef-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-133">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="653ef-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="653ef-134">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="653ef-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="653ef-135">**說明**</span><span class="sxs-lookup"><span data-stu-id="653ef-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-138">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="653ef-138">Textual description of the object.</span></span> <span data-ttu-id="653ef-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="653ef-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="653ef-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="653ef-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-141">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="653ef-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-143">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="653ef-143">Date and time the object was installed.</span></span> <span data-ttu-id="653ef-144">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="653ef-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="653ef-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="653ef-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="653ef-146">**名稱**</span><span class="sxs-lookup"><span data-stu-id="653ef-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-149">服務的唯一識別碼，也會提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="653ef-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="653ef-150">如需功能的詳細資訊，請參閱物件的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="653ef-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="653ef-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="653ef-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="653ef-152">**已開始**</span><span class="sxs-lookup"><span data-stu-id="653ef-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-153">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="653ef-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-155">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="653ef-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="653ef-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="653ef-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-159">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="653ef-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="653ef-160">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="653ef-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="653ef-161">**自動**</span><span class="sxs-lookup"><span data-stu-id="653ef-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="653ef-162">**》**</span><span class="sxs-lookup"><span data-stu-id="653ef-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="653ef-163">**狀態**</span><span class="sxs-lookup"><span data-stu-id="653ef-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-166">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="653ef-166">Current status of the object.</span></span> <span data-ttu-id="653ef-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="653ef-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="653ef-168">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="653ef-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="653ef-169">**正常**</span><span class="sxs-lookup"><span data-stu-id="653ef-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="653ef-170">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="653ef-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="653ef-171">**降級**</span><span class="sxs-lookup"><span data-stu-id="653ef-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="653ef-172">**不明**</span><span class="sxs-lookup"><span data-stu-id="653ef-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="653ef-173">**「Pred 失敗」**</span><span class="sxs-lookup"><span data-stu-id="653ef-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="653ef-174">**入門**</span><span class="sxs-lookup"><span data-stu-id="653ef-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="653ef-175">**從而**</span><span class="sxs-lookup"><span data-stu-id="653ef-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="653ef-176">**維護**</span><span class="sxs-lookup"><span data-stu-id="653ef-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="653ef-177">**強調**</span><span class="sxs-lookup"><span data-stu-id="653ef-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="653ef-178">**"NonRecover"**</span><span class="sxs-lookup"><span data-stu-id="653ef-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="653ef-179">**「無連絡人」**</span><span class="sxs-lookup"><span data-stu-id="653ef-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="653ef-180">**「遺失通訊」**</span><span class="sxs-lookup"><span data-stu-id="653ef-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="653ef-181">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="653ef-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-184">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="653ef-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="653ef-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="653ef-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="653ef-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="653ef-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="653ef-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="653ef-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="653ef-188">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="653ef-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="653ef-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="653ef-189">Requirements</span></span>



| <span data-ttu-id="653ef-190">需求</span><span class="sxs-lookup"><span data-stu-id="653ef-190">Requirement</span></span> | <span data-ttu-id="653ef-191">值</span><span class="sxs-lookup"><span data-stu-id="653ef-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653ef-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="653ef-192">Minimum supported client</span></span><br/> | <span data-ttu-id="653ef-193">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="653ef-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="653ef-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="653ef-194">Minimum supported server</span></span><br/> | <span data-ttu-id="653ef-195">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="653ef-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="653ef-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="653ef-196">Namespace</span></span><br/>                | <span data-ttu-id="653ef-197">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="653ef-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="653ef-198">MOF</span><span class="sxs-lookup"><span data-stu-id="653ef-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="653ef-199"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="653ef-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="653ef-200">DLL</span><span class="sxs-lookup"><span data-stu-id="653ef-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="653ef-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="653ef-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="653ef-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="653ef-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653ef-203">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="653ef-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

