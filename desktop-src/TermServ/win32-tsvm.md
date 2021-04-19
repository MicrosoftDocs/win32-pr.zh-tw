---
title: Win32_TSVm 類別
description: 代表遠端桌面虛擬機器。
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Win32_TSVm 類別遠端桌面服務
- Win32_TSVm 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966288"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="88151-105">Win32 \_ TSVm 類別</span><span class="sxs-lookup"><span data-stu-id="88151-105">Win32\_TSVm class</span></span>

<span data-ttu-id="88151-106">代表遠端桌面虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="88151-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="88151-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="88151-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88151-108">語法</span><span class="sxs-lookup"><span data-stu-id="88151-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="88151-109">成員</span><span class="sxs-lookup"><span data-stu-id="88151-109">Members</span></span>

<span data-ttu-id="88151-110">**Win32 \_ TSVm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88151-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="88151-111">方法</span><span class="sxs-lookup"><span data-stu-id="88151-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="88151-112">屬性</span><span class="sxs-lookup"><span data-stu-id="88151-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88151-113">方法</span><span class="sxs-lookup"><span data-stu-id="88151-113">Methods</span></span>

<span data-ttu-id="88151-114">**Win32 \_ TSVm** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="88151-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="88151-115">方法</span><span class="sxs-lookup"><span data-stu-id="88151-115">Method</span></span>                                                                | <span data-ttu-id="88151-116">描述</span><span class="sxs-lookup"><span data-stu-id="88151-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="88151-117">**DumpVmInfo**</span><span class="sxs-lookup"><span data-stu-id="88151-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="88151-118">僅供測試之用。</span><span class="sxs-lookup"><span data-stu-id="88151-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="88151-119">**出口**</span><span class="sxs-lookup"><span data-stu-id="88151-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="88151-120">取得 VM 的會話監視資訊</span><span class="sxs-lookup"><span data-stu-id="88151-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="88151-121">**QueryOfflineInformation**</span><span class="sxs-lookup"><span data-stu-id="88151-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="88151-122">僅在離線時查詢屬性。</span><span class="sxs-lookup"><span data-stu-id="88151-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="88151-123">屬性</span><span class="sxs-lookup"><span data-stu-id="88151-123">Properties</span></span>

<span data-ttu-id="88151-124">**Win32 \_ TSVm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88151-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88151-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="88151-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88151-128">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="88151-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88151-129">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="88151-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="88151-130">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88151-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88151-131">**說明**</span><span class="sxs-lookup"><span data-stu-id="88151-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88151-134">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="88151-134">Description of the object.</span></span>

<span data-ttu-id="88151-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88151-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88151-136">**EnlightmentSettings**</span><span class="sxs-lookup"><span data-stu-id="88151-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="88151-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="88151-139">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88151-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88151-140">包含虛擬機器之啟蒙設定的 XML BLOB。</span><span class="sxs-lookup"><span data-stu-id="88151-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="88151-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88151-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-142">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88151-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88151-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88151-144">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="88151-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="88151-145">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="88151-145">The date the object was installed.</span></span> <span data-ttu-id="88151-146">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="88151-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88151-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88151-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88151-148">**名稱**</span><span class="sxs-lookup"><span data-stu-id="88151-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88151-151">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="88151-151">The name of the object.</span></span>

<span data-ttu-id="88151-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88151-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88151-153">**狀態**</span><span class="sxs-lookup"><span data-stu-id="88151-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88151-156">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="88151-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="88151-157">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="88151-157">Current status of the object.</span></span> <span data-ttu-id="88151-158">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="88151-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="88151-159">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="88151-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="88151-160">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="88151-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88151-161">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="88151-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88151-162">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="88151-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88151-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88151-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="88151-164"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="88151-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-165"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-166"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-167"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-168"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-169"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-170"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="88151-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="88151-171"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="88151-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88151-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="88151-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88151-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88151-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88151-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88151-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88151-175">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88151-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88151-176">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="88151-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88151-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="88151-177">Requirements</span></span>



| <span data-ttu-id="88151-178">需求</span><span class="sxs-lookup"><span data-stu-id="88151-178">Requirement</span></span> | <span data-ttu-id="88151-179">值</span><span class="sxs-lookup"><span data-stu-id="88151-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="88151-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88151-180">Minimum supported client</span></span><br/> | <span data-ttu-id="88151-181">都不支援</span><span class="sxs-lookup"><span data-stu-id="88151-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="88151-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88151-182">Minimum supported server</span></span><br/> | <span data-ttu-id="88151-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="88151-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="88151-184">命名空間</span><span class="sxs-lookup"><span data-stu-id="88151-184">Namespace</span></span><br/>                | <span data-ttu-id="88151-185">根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="88151-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="88151-186">MOF</span><span class="sxs-lookup"><span data-stu-id="88151-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88151-187"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="88151-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="88151-188">DLL</span><span class="sxs-lookup"><span data-stu-id="88151-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88151-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88151-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

