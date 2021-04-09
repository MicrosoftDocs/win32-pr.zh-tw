---
description: Win32 登錄 \_&\# 8194;WMI 類別代表執行 Windows 的電腦系統上的系統登錄。
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Win32_Registry 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936131"
---
# <a name="win32_registry-class"></a><span data-ttu-id="a8273-103">Win32 登錄 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="a8273-103">Win32\_Registry class</span></span>

<span data-ttu-id="a8273-104">**\_ Win32** 登錄  [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的系統登錄。</span><span class="sxs-lookup"><span data-stu-id="a8273-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="a8273-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8273-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a8273-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="a8273-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8273-107">語法</span><span class="sxs-lookup"><span data-stu-id="a8273-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="a8273-108">成員</span><span class="sxs-lookup"><span data-stu-id="a8273-108">Members</span></span>

<span data-ttu-id="a8273-109">**Win32 登錄 \_** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8273-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="a8273-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a8273-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8273-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a8273-111">Properties</span></span>

<span data-ttu-id="a8273-112">**Win32 登錄 \_** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8273-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8273-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="a8273-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8273-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="a8273-117">A short textual description of the object.</span></span>

<span data-ttu-id="a8273-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8273-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8273-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="a8273-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a8273-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-122">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-123">Windows 登錄的目前實體大小。</span><span class="sxs-lookup"><span data-stu-id="a8273-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="a8273-124">範例：10</span><span class="sxs-lookup"><span data-stu-id="a8273-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="a8273-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="a8273-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8273-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-128">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-129">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a8273-129">A textual description of the object.</span></span>

<span data-ttu-id="a8273-130">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8273-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8273-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a8273-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-132">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a8273-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-134">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a8273-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-135">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="a8273-135">Indicates when the object was installed.</span></span> <span data-ttu-id="a8273-136">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="a8273-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a8273-137">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8273-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8273-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="a8273-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a8273-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-141">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-142">Windows 登錄的大小上限。</span><span class="sxs-lookup"><span data-stu-id="a8273-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="a8273-143">如果系統成功使用 **ProposedSize** 屬性， **MaximumSize** 應該包含相同的值。</span><span class="sxs-lookup"><span data-stu-id="a8273-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="a8273-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a8273-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8273-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-147">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-148">Windows 登錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8273-148">Name of the Windows registry.</span></span> <span data-ttu-id="a8273-149">最大長度是 256 個字元。</span><span class="sxs-lookup"><span data-stu-id="a8273-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="a8273-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="a8273-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a8273-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a8273-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8273-153">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-154">建議的 Windows 登錄大小。</span><span class="sxs-lookup"><span data-stu-id="a8273-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="a8273-155">這是唯一可以修改的登錄設定，並且會在系統下次開機時嘗試其提案。</span><span class="sxs-lookup"><span data-stu-id="a8273-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="a8273-156">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a8273-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8273-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8273-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8273-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8273-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8273-159">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a8273-160">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="a8273-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="a8273-161">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="a8273-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a8273-162">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="a8273-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a8273-163">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="a8273-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a8273-164">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a8273-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a8273-165">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="a8273-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a8273-166">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a8273-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a8273-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8273-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a8273-168">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a8273-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a8273-169">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a8273-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a8273-170">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a8273-171">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a8273-172">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a8273-173">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a8273-174">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a8273-175">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a8273-176">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a8273-177">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a8273-178">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a8273-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a8273-179">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a8273-180">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a8273-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a8273-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a8273-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a8273-182">備註</span><span class="sxs-lookup"><span data-stu-id="a8273-182">Remarks</span></span>

<span data-ttu-id="a8273-183">**Win32 登錄 \_** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8273-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8273-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8273-184">Requirements</span></span>



| <span data-ttu-id="a8273-185">需求</span><span class="sxs-lookup"><span data-stu-id="a8273-185">Requirement</span></span> | <span data-ttu-id="a8273-186">值</span><span class="sxs-lookup"><span data-stu-id="a8273-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8273-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8273-187">Minimum supported client</span></span><br/> | <span data-ttu-id="a8273-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8273-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8273-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8273-189">Minimum supported server</span></span><br/> | <span data-ttu-id="a8273-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8273-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8273-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8273-191">Namespace</span></span><br/>                | <span data-ttu-id="a8273-192">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8273-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8273-193">MOF</span><span class="sxs-lookup"><span data-stu-id="a8273-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8273-194"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8273-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8273-195">DLL</span><span class="sxs-lookup"><span data-stu-id="a8273-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8273-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8273-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8273-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8273-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8273-198">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a8273-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="a8273-199">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="a8273-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
