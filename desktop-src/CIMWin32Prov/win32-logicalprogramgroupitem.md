---
description: Win32 \_ LogicalProgramGroupItem&\# 8194;WMI 類別代表 Win32 LogicalProgramGroup 所包含的專案 \_ ，該專案也不是另一個 win32 \_ LogicalProgramGroup 實例。
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510730"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="71fa1-103">Win32 \_ LogicalProgramGroupItem 類別</span><span class="sxs-lookup"><span data-stu-id="71fa1-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="71fa1-104">**Win32 \_ LogicalProgramGroupItem** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 [**win32 \_ LogicalProgramGroup**](win32-logicalprogramgroup.md)所包含的元素，而該專案也不是另一個 **win32 \_ LogicalProgramGroup** 實例。</span><span class="sxs-lookup"><span data-stu-id="71fa1-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="71fa1-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="71fa1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71fa1-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="71fa1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71fa1-107">語法</span><span class="sxs-lookup"><span data-stu-id="71fa1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="71fa1-108">成員</span><span class="sxs-lookup"><span data-stu-id="71fa1-108">Members</span></span>

<span data-ttu-id="71fa1-109">**Win32 \_ LogicalProgramGroupItem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="71fa1-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="71fa1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="71fa1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71fa1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="71fa1-111">Properties</span></span>

<span data-ttu-id="71fa1-112">**Win32 \_ LogicalProgramGroupItem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="71fa1-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71fa1-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="71fa1-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fa1-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71fa1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71fa1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71fa1-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="71fa1-117">A short textual description of the object.</span></span>

<span data-ttu-id="71fa1-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fa1-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="71fa1-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fa1-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71fa1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71fa1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-122">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71fa1-123">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="71fa1-123">A textual description of the object.</span></span>

<span data-ttu-id="71fa1-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fa1-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71fa1-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fa1-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="71fa1-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71fa1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="71fa1-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71fa1-129">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="71fa1-129">Indicates when the object was installed.</span></span> <span data-ttu-id="71fa1-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="71fa1-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="71fa1-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71fa1-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="71fa1-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fa1-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71fa1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71fa1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-135">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| CWbemProviderGlue 類別方法 \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)" ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="71fa1-136">電腦系統內的實例。</span><span class="sxs-lookup"><span data-stu-id="71fa1-136">Instance within a computer system.</span></span> <span data-ttu-id="71fa1-137">程式群組會實作為 Win32 中的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="71fa1-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="71fa1-138">應提供完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="71fa1-138">Full path names should be provided.</span></span>

<span data-ttu-id="71fa1-139">範例： "C： \\ Users \\  \\ AppData \\ 漫遊 \\ Microsoft \\ Windows \\ 開始功能表 \\ 程式 \\ 配件 \\ NotePad"</span><span class="sxs-lookup"><span data-stu-id="71fa1-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="71fa1-140">**狀態**</span><span class="sxs-lookup"><span data-stu-id="71fa1-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71fa1-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71fa1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71fa1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71fa1-143">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71fa1-144">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="71fa1-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="71fa1-145">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="71fa1-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="71fa1-146">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="71fa1-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="71fa1-147">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="71fa1-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="71fa1-148">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="71fa1-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71fa1-149">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="71fa1-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71fa1-150">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="71fa1-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71fa1-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71fa1-152">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="71fa1-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71fa1-153">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71fa1-154">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71fa1-155">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71fa1-156">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71fa1-157">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71fa1-158">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71fa1-159">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71fa1-160">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71fa1-161">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71fa1-162">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71fa1-163">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71fa1-164">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="71fa1-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="71fa1-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="71fa1-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="71fa1-166">備註</span><span class="sxs-lookup"><span data-stu-id="71fa1-166">Remarks</span></span>

<span data-ttu-id="71fa1-167">**Win32 \_ LogicalProgramGroupItem** 類別衍生自 [**win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="71fa1-168">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="71fa1-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="71fa1-169">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="71fa1-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="71fa1-170">如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="71fa1-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="71fa1-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="71fa1-171">Requirements</span></span>



| <span data-ttu-id="71fa1-172">需求</span><span class="sxs-lookup"><span data-stu-id="71fa1-172">Requirement</span></span> | <span data-ttu-id="71fa1-173">值</span><span class="sxs-lookup"><span data-stu-id="71fa1-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71fa1-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71fa1-174">Minimum supported client</span></span><br/> | <span data-ttu-id="71fa1-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71fa1-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71fa1-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71fa1-176">Minimum supported server</span></span><br/> | <span data-ttu-id="71fa1-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71fa1-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71fa1-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="71fa1-178">Namespace</span></span><br/>                | <span data-ttu-id="71fa1-179">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="71fa1-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71fa1-180">MOF</span><span class="sxs-lookup"><span data-stu-id="71fa1-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71fa1-181"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="71fa1-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71fa1-182">DLL</span><span class="sxs-lookup"><span data-stu-id="71fa1-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71fa1-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71fa1-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71fa1-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71fa1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71fa1-185">**Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="71fa1-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="71fa1-186">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71fa1-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

