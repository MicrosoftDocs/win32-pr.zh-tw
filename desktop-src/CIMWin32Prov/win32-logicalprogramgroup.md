---
description: Win32 \_ LogicalProgramGroup&\# 8194;WMI 類別代表執行 Windows 的電腦系統中的程式群組。 例如，「配件」或「啟動」。
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847482"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="ac771-104">Win32 \_ LogicalProgramGroup 類別</span><span class="sxs-lookup"><span data-stu-id="ac771-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="ac771-105">**Win32 \_ LogicalProgramGroup** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在執行 Windows 的電腦系統中的程式群組。</span><span class="sxs-lookup"><span data-stu-id="ac771-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="ac771-106">例如，「配件」或「啟動」。</span><span class="sxs-lookup"><span data-stu-id="ac771-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="ac771-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ac771-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ac771-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="ac771-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac771-109">語法</span><span class="sxs-lookup"><span data-stu-id="ac771-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="ac771-110">成員</span><span class="sxs-lookup"><span data-stu-id="ac771-110">Members</span></span>

<span data-ttu-id="ac771-111">**Win32 \_ LogicalProgramGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac771-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="ac771-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ac771-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac771-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ac771-113">Properties</span></span>

<span data-ttu-id="ac771-114">**Win32 \_ LogicalProgramGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ac771-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac771-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="ac771-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="ac771-119">A short textual description of the object.</span></span>

<span data-ttu-id="ac771-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ac771-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac771-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="ac771-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-124">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ac771-125">A textual description of the object.</span></span>

<span data-ttu-id="ac771-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ac771-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac771-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="ac771-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| CWbemProviderGlue Class 方法 \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-131">Windows 程式群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac771-131">Name of the Windows program group.</span></span> <span data-ttu-id="ac771-132">程式群組會實作為 Win32 中的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="ac771-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="ac771-133">範例：「配件 \\ 系統工具」</span><span class="sxs-lookup"><span data-stu-id="ac771-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="ac771-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ac771-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ac771-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-137">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="ac771-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-138">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="ac771-138">Indicates when the object was installed.</span></span> <span data-ttu-id="ac771-139">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="ac771-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ac771-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ac771-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac771-141">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ac771-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-144">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| CWbemProviderGlue Class 方法 \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-145">使用者指派的名稱，後面加上組名。</span><span class="sxs-lookup"><span data-stu-id="ac771-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="ac771-146">程式群組會實作為 Win32 中的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="ac771-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="ac771-147">範例：「所有使用者：配件 \\ 系統工具」</span><span class="sxs-lookup"><span data-stu-id="ac771-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="ac771-148">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ac771-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-152">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ac771-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="ac771-153">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="ac771-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ac771-154">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="ac771-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ac771-155">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="ac771-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ac771-156">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="ac771-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ac771-157">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="ac771-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ac771-158">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="ac771-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ac771-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="ac771-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ac771-160">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="ac771-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ac771-161">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="ac771-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ac771-162">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ac771-163">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac771-164">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ac771-165">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ac771-166">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ac771-167">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ac771-168">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ac771-169">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ac771-170">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ac771-171">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ac771-172">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="ac771-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac771-173">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="ac771-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac771-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac771-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac771-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac771-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac771-176">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| CWbemProviderGlue Class 方法 \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)" ) </span><span class="sxs-lookup"><span data-stu-id="ac771-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="ac771-177">可以存取 Windows 程式群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="ac771-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="ac771-178">程式群組會實作為 Win32 中的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="ac771-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="ac771-179">範例：「所有使用者」</span><span class="sxs-lookup"><span data-stu-id="ac771-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac771-180">備註</span><span class="sxs-lookup"><span data-stu-id="ac771-180">Remarks</span></span>

<span data-ttu-id="ac771-181">**Win32 \_ LogicalProgramGroup** 類別衍生自 [**win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)。</span><span class="sxs-lookup"><span data-stu-id="ac771-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="ac771-182">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="ac771-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="ac771-183">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="ac771-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="ac771-184">如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="ac771-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac771-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac771-185">Requirements</span></span>



| <span data-ttu-id="ac771-186">需求</span><span class="sxs-lookup"><span data-stu-id="ac771-186">Requirement</span></span> | <span data-ttu-id="ac771-187">值</span><span class="sxs-lookup"><span data-stu-id="ac771-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac771-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac771-188">Minimum supported client</span></span><br/> | <span data-ttu-id="ac771-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac771-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac771-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac771-190">Minimum supported server</span></span><br/> | <span data-ttu-id="ac771-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac771-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac771-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac771-192">Namespace</span></span><br/>                | <span data-ttu-id="ac771-193">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ac771-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ac771-194">MOF</span><span class="sxs-lookup"><span data-stu-id="ac771-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac771-195"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac771-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac771-196">DLL</span><span class="sxs-lookup"><span data-stu-id="ac771-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac771-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac771-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac771-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac771-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac771-199">**Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="ac771-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="ac771-200">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ac771-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

