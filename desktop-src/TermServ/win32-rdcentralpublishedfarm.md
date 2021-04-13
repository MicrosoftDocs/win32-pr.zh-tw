---
title: Win32_RDCentralPublishedFarm 類別
description: 已發佈桌面或應用程式的伺服器陣列清單。
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFarm 類別遠端桌面服務
- Win32_RDCentralPublishedFarm 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464972"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="295e9-105">Win32 \_ RDCentralPublishedFarm 類別</span><span class="sxs-lookup"><span data-stu-id="295e9-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="295e9-106">已發佈桌面或應用程式的伺服器陣列清單。</span><span class="sxs-lookup"><span data-stu-id="295e9-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="295e9-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="295e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="295e9-108">語法</span><span class="sxs-lookup"><span data-stu-id="295e9-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="295e9-109">成員</span><span class="sxs-lookup"><span data-stu-id="295e9-109">Members</span></span>

<span data-ttu-id="295e9-110">**Win32 \_ RDCentralPublishedFarm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="295e9-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="295e9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="295e9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="295e9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="295e9-112">Properties</span></span>

<span data-ttu-id="295e9-113">**Win32 \_ RDCentralPublishedFarm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="295e9-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="295e9-114">**別名**</span><span class="sxs-lookup"><span data-stu-id="295e9-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="295e9-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-118">已發佈桌面或應用程式之伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="295e9-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="295e9-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="295e9-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="295e9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="295e9-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="295e9-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-123">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="295e9-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="295e9-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="295e9-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="295e9-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="295e9-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="295e9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="295e9-128">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="295e9-128">Description of the object.</span></span>

<span data-ttu-id="295e9-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="295e9-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="295e9-130">**FarmType**</span><span class="sxs-lookup"><span data-stu-id="295e9-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="295e9-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-133">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="295e9-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-134">伺服器陣列的種類：</span><span class="sxs-lookup"><span data-stu-id="295e9-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="295e9-135">**RDSH** (0) </span><span class="sxs-lookup"><span data-stu-id="295e9-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="295e9-136">**TempVM** (1) </span><span class="sxs-lookup"><span data-stu-id="295e9-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="295e9-137">**ManualPersonalVM** (2) </span><span class="sxs-lookup"><span data-stu-id="295e9-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="295e9-138">**AutoPersonalVM** (3) </span><span class="sxs-lookup"><span data-stu-id="295e9-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="295e9-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="295e9-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="295e9-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="295e9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="295e9-142">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="295e9-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="295e9-143">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="295e9-143">The date the object was installed.</span></span> <span data-ttu-id="295e9-144">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="295e9-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="295e9-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="295e9-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="295e9-146">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="295e9-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="295e9-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-149">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="295e9-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-150">如果在連接時需要將使用者新增至本機系統管理員群組，**則為 true** 。否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="295e9-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="295e9-151">僅適用于 ManualPersonalVm 和 AutoPersonalVM 伺服器陣列類型。</span><span class="sxs-lookup"><span data-stu-id="295e9-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="295e9-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="295e9-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="295e9-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="295e9-155">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="295e9-155">The name of the object.</span></span>

<span data-ttu-id="295e9-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="295e9-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="295e9-157">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="295e9-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-158">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="295e9-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-160">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="295e9-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-161">**true** 表示在使用者登出後將 VM 自動回復至快照集;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="295e9-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="295e9-162">僅適用于 TempVm 伺服器陣列類型。</span><span class="sxs-lookup"><span data-stu-id="295e9-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="295e9-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="295e9-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-166">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="295e9-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-167">控制應用程式存取權之安全描述項的名稱（以 SDDL 格式）。</span><span class="sxs-lookup"><span data-stu-id="295e9-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="295e9-168">使用空字串表示允許所有的存取。</span><span class="sxs-lookup"><span data-stu-id="295e9-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="295e9-169">**狀態**</span><span class="sxs-lookup"><span data-stu-id="295e9-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="295e9-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="295e9-172">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="295e9-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-173">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="295e9-173">Current status of the object.</span></span> <span data-ttu-id="295e9-174">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="295e9-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="295e9-175">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="295e9-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="295e9-176">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="295e9-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="295e9-177">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="295e9-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="295e9-178">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="295e9-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="295e9-179">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="295e9-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="295e9-180"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="295e9-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-181"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-182"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-183"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-184"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-185"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-186"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="295e9-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="295e9-187"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="295e9-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="295e9-188">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="295e9-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="295e9-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="295e9-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="295e9-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="295e9-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="295e9-191">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="295e9-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="295e9-192">虛擬機器伺服器陣列設定。</span><span class="sxs-lookup"><span data-stu-id="295e9-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="295e9-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="295e9-193">Requirements</span></span>



| <span data-ttu-id="295e9-194">需求</span><span class="sxs-lookup"><span data-stu-id="295e9-194">Requirement</span></span> | <span data-ttu-id="295e9-195">值</span><span class="sxs-lookup"><span data-stu-id="295e9-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="295e9-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="295e9-196">Minimum supported client</span></span><br/> | <span data-ttu-id="295e9-197">都不支援</span><span class="sxs-lookup"><span data-stu-id="295e9-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="295e9-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="295e9-198">Minimum supported server</span></span><br/> | <span data-ttu-id="295e9-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="295e9-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="295e9-200">命名空間</span><span class="sxs-lookup"><span data-stu-id="295e9-200">Namespace</span></span><br/>                | <span data-ttu-id="295e9-201">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="295e9-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="295e9-202">MOF</span><span class="sxs-lookup"><span data-stu-id="295e9-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="295e9-203"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="295e9-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="295e9-204">DLL</span><span class="sxs-lookup"><span data-stu-id="295e9-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="295e9-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="295e9-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

