---
title: Win32_RDMSVirtualDesktopCollection 類別
description: 建立及管理虛擬桌面集合。
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967532"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="cbcb6-105">Win32 \_ RDMSVirtualDesktopCollection 類別</span><span class="sxs-lookup"><span data-stu-id="cbcb6-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="cbcb6-106">建立及管理虛擬桌面集合。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="cbcb6-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcb6-108">語法</span><span class="sxs-lookup"><span data-stu-id="cbcb6-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="cbcb6-109">成員</span><span class="sxs-lookup"><span data-stu-id="cbcb6-109">Members</span></span>

<span data-ttu-id="cbcb6-110">**Win32 \_ RDMSVirtualDesktopCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cbcb6-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="cbcb6-111">方法</span><span class="sxs-lookup"><span data-stu-id="cbcb6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="cbcb6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cbcb6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cbcb6-113">方法</span><span class="sxs-lookup"><span data-stu-id="cbcb6-113">Methods</span></span>

<span data-ttu-id="cbcb6-114">**Win32 \_ RDMSVirtualDesktopCollection** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="cbcb6-115">方法</span><span class="sxs-lookup"><span data-stu-id="cbcb6-115">Method</span></span>                                                                                            | <span data-ttu-id="cbcb6-116">描述</span><span class="sxs-lookup"><span data-stu-id="cbcb6-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbcb6-117">**AddVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="cbcb6-118">將虛擬桌面新增至虛擬桌面集合。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="cbcb6-119">**CancelPatch**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="cbcb6-120">取消虛擬機器集合中虛擬機器的軟體更新布建作業。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="cbcb6-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="cbcb6-122">從虛擬桌面集合抓取整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="cbcb6-123">**GetPatchProperties**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="cbcb6-124">抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="cbcb6-125">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="cbcb6-126">從虛擬桌面集合抓取字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="cbcb6-127">**ProvisioningEnumerateJobs**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="cbcb6-128">列舉此服務的虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="cbcb6-129">**ProvisioningJobCancel**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="cbcb6-130">取消虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cbcb6-131">**ProvisioningJobExecute**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="cbcb6-132">執行虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="cbcb6-133">**ProvisioningJobGetReport**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="cbcb6-134">取得虛擬桌面布建作業狀態的相關報告。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="cbcb6-135">**ProvisioningPrepJob**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="cbcb6-136">建立虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cbcb6-137">**RemoveVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="cbcb6-138">從虛擬桌面集合移除虛擬桌面。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="cbcb6-139">**SchedulePatch**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="cbcb6-140">排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="cbcb6-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="cbcb6-142">更新虛擬桌面集合的整數屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="cbcb6-143">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="cbcb6-144">更新虛擬桌面集合的字串屬性值。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="cbcb6-145">屬性</span><span class="sxs-lookup"><span data-stu-id="cbcb6-145">Properties</span></span>

<span data-ttu-id="cbcb6-146">**Win32 \_ RDMSVirtualDesktopCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbcb6-147">**別名**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-150">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-151">取得或設定集合的別名。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-152">**CollectionDescription**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-155">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-156">取得或設定集合的描述。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-157">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-158">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="cbcb6-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-160">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-161">取得或設定值的陣列，這些值會指定集合的圖示。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-162">**IsHA**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-163">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-165">取得或設定值，這個值會指出集合是否包含高可用性 Vm。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="cbcb6-166">如果集合包含高可用性 Vm，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-170">取得或設定值，這個值會指出集合是否為 managed。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="cbcb6-171">如果集合是受管理的，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-172">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-173">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-175">取得或設定值，指出使用者是否為 VM 上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="cbcb6-176">如果使用者是 VM 上的系統管理員，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-177">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-180">取得或設定集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-181">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-182">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-184">取得或設定值，這個值會指出 VM 是否以 VM 快照集進行匯總。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="cbcb6-185">如果 VM 是以 VM 快照集進行匯總，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-189">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-190">取得或設定控制對集合之存取的 SSDL 格式化安全描述項。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-191">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-192">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-194">取得或設定值，指出集合是否顯示在終端機服務中 Web 存取 (TS Web 存取) 。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="cbcb6-195">**TRUE** 表示在 TS Web 存取中顯示集合;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-196">**型別**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-199">取得或設定值，這個值表示集合所裝載的虛擬機器會話類型。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="cbcb6-200">此屬性包含下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="cbcb6-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="cbcb6-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1) </span><span class="sxs-lookup"><span data-stu-id="cbcb6-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cbcb6-202">暫時的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="cbcb6-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2) </span><span class="sxs-lookup"><span data-stu-id="cbcb6-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cbcb6-204">手動建立的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="cbcb6-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3) </span><span class="sxs-lookup"><span data-stu-id="cbcb6-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cbcb6-206">自動產生的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cbcb6-207">**UserVHDSetting**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-209">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-210">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-211">取得或設定集合的使用者資料 VHD 設定。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="cbcb6-212">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcb6-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cbcb6-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cbcb6-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cbcb6-215">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cbcb6-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cbcb6-216">取得或設定集合中虛擬機器的桌面設定。</span><span class="sxs-lookup"><span data-stu-id="cbcb6-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbcb6-217">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbcb6-217">Requirements</span></span>



| <span data-ttu-id="cbcb6-218">需求</span><span class="sxs-lookup"><span data-stu-id="cbcb6-218">Requirement</span></span> | <span data-ttu-id="cbcb6-219">值</span><span class="sxs-lookup"><span data-stu-id="cbcb6-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcb6-220">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbcb6-220">Minimum supported client</span></span><br/> | <span data-ttu-id="cbcb6-221">都不支援</span><span class="sxs-lookup"><span data-stu-id="cbcb6-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cbcb6-222">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbcb6-222">Minimum supported server</span></span><br/> | <span data-ttu-id="cbcb6-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cbcb6-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cbcb6-224">命名空間</span><span class="sxs-lookup"><span data-stu-id="cbcb6-224">Namespace</span></span><br/>                | <span data-ttu-id="cbcb6-225">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="cbcb6-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cbcb6-226">MOF</span><span class="sxs-lookup"><span data-stu-id="cbcb6-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbcb6-227"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbcb6-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbcb6-228">DLL</span><span class="sxs-lookup"><span data-stu-id="cbcb6-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbcb6-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbcb6-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cbcb6-230">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbcb6-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcb6-231">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="cbcb6-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

