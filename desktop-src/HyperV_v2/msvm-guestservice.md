---
description: Msvm \_ GuestService 是來賓中可從主機存取之服務的抽象基類。
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Msvm_GuestService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386110"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="18522-103">Msvm \_ GuestService 類別</span><span class="sxs-lookup"><span data-stu-id="18522-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="18522-104">**Msvm \_GuestService** 是來賓中可從主機存取之服務的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="18522-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="18522-105">此類別衍生自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service) 類別。</span><span class="sxs-lookup"><span data-stu-id="18522-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="18522-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18522-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18522-107">語法</span><span class="sxs-lookup"><span data-stu-id="18522-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="18522-108">成員</span><span class="sxs-lookup"><span data-stu-id="18522-108">Members</span></span>

<span data-ttu-id="18522-109">**Msvm \_ GuestService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18522-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="18522-110">方法</span><span class="sxs-lookup"><span data-stu-id="18522-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="18522-111">屬性</span><span class="sxs-lookup"><span data-stu-id="18522-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18522-112">方法</span><span class="sxs-lookup"><span data-stu-id="18522-112">Methods</span></span>

<span data-ttu-id="18522-113">**Msvm \_ GuestService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="18522-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="18522-114">方法</span><span class="sxs-lookup"><span data-stu-id="18522-114">Method</span></span>                                                             | <span data-ttu-id="18522-115">描述</span><span class="sxs-lookup"><span data-stu-id="18522-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18522-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="18522-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="18522-117">要求來賓服務的狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="18522-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="18522-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="18522-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="18522-119">將來賓服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="18522-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="18522-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="18522-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="18522-121">停止來賓服務。</span><span class="sxs-lookup"><span data-stu-id="18522-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="18522-122">屬性</span><span class="sxs-lookup"><span data-stu-id="18522-122">Properties</span></span>

<span data-ttu-id="18522-123">**Msvm \_ GuestService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18522-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18522-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="18522-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-127">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="18522-127">Short textual description of the object.</span></span> <span data-ttu-id="18522-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18522-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18522-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18522-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-132">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="18522-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="18522-133">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="18522-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="18522-134">**說明**</span><span class="sxs-lookup"><span data-stu-id="18522-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-137">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="18522-137">Textual description of the object.</span></span> <span data-ttu-id="18522-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18522-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18522-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18522-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18522-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18522-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-142">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="18522-142">Date and time the object was installed.</span></span> <span data-ttu-id="18522-143">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="18522-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="18522-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18522-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18522-145">**名稱**</span><span class="sxs-lookup"><span data-stu-id="18522-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-148">服務的唯一識別碼，也會提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="18522-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="18522-149">如需功能的詳細資訊，請參閱物件的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="18522-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="18522-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18522-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18522-151">**已開始**</span><span class="sxs-lookup"><span data-stu-id="18522-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-152">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18522-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18522-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-154">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="18522-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="18522-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="18522-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-158">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="18522-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="18522-159">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="18522-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="18522-160">**自動**</span><span class="sxs-lookup"><span data-stu-id="18522-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="18522-161">**》**</span><span class="sxs-lookup"><span data-stu-id="18522-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18522-162">**狀態**</span><span class="sxs-lookup"><span data-stu-id="18522-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-165">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18522-165">Current status of the object.</span></span> <span data-ttu-id="18522-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18522-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="18522-167">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="18522-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="18522-168">**正常**</span><span class="sxs-lookup"><span data-stu-id="18522-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="18522-169">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="18522-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="18522-170">**降級**</span><span class="sxs-lookup"><span data-stu-id="18522-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="18522-171">**不明**</span><span class="sxs-lookup"><span data-stu-id="18522-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="18522-172">**「Pred 失敗」**</span><span class="sxs-lookup"><span data-stu-id="18522-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="18522-173">**入門**</span><span class="sxs-lookup"><span data-stu-id="18522-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="18522-174">**從而**</span><span class="sxs-lookup"><span data-stu-id="18522-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="18522-175">**維護**</span><span class="sxs-lookup"><span data-stu-id="18522-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="18522-176">**強調**</span><span class="sxs-lookup"><span data-stu-id="18522-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="18522-177">**"NonRecover"**</span><span class="sxs-lookup"><span data-stu-id="18522-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="18522-178">**「無連絡人」**</span><span class="sxs-lookup"><span data-stu-id="18522-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="18522-179">**「遺失通訊」**</span><span class="sxs-lookup"><span data-stu-id="18522-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18522-180">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18522-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-183">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="18522-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="18522-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18522-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18522-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18522-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18522-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18522-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18522-187">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="18522-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18522-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="18522-188">Requirements</span></span>



| <span data-ttu-id="18522-189">需求</span><span class="sxs-lookup"><span data-stu-id="18522-189">Requirement</span></span> | <span data-ttu-id="18522-190">值</span><span class="sxs-lookup"><span data-stu-id="18522-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18522-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18522-191">Minimum supported client</span></span><br/> | <span data-ttu-id="18522-192">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18522-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="18522-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18522-193">Minimum supported server</span></span><br/> | <span data-ttu-id="18522-194">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18522-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="18522-195">命名空間</span><span class="sxs-lookup"><span data-stu-id="18522-195">Namespace</span></span><br/>                | <span data-ttu-id="18522-196">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="18522-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18522-197">MOF</span><span class="sxs-lookup"><span data-stu-id="18522-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18522-198"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18522-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18522-199">DLL</span><span class="sxs-lookup"><span data-stu-id="18522-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18522-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18522-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18522-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18522-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18522-202">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="18522-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="18522-203">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="18522-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

