---
description: CIM \_ ManagedSystemElement 類別是 system 元素階層的基類。 任何可辨別的系統元件都是包含在這個類別中的候選。
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: 'CIM_ManagedSystemElement 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110828"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="7bab7-104">CIM_ManagedSystemElement 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="7bab7-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7bab7-105">**CIM \_ ManagedSystemElement** 類別是 system 元素階層的基類。</span><span class="sxs-lookup"><span data-stu-id="7bab7-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="7bab7-106">任何可辨別的系統元件都是包含在這個類別中的候選。</span><span class="sxs-lookup"><span data-stu-id="7bab7-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="7bab7-107">範例包括軟體元件，例如檔案;裝置，例如磁片磁碟機和控制器;以及實體元件，例如晶片和卡片。</span><span class="sxs-lookup"><span data-stu-id="7bab7-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bab7-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7bab7-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7bab7-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7bab7-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7bab7-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7bab7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7bab7-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7bab7-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bab7-112">語法</span><span class="sxs-lookup"><span data-stu-id="7bab7-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="7bab7-113">成員</span><span class="sxs-lookup"><span data-stu-id="7bab7-113">Members</span></span>

<span data-ttu-id="7bab7-114">**CIM \_ ManagedSystemElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7bab7-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="7bab7-115">屬性</span><span class="sxs-lookup"><span data-stu-id="7bab7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bab7-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7bab7-116">Properties</span></span>

<span data-ttu-id="7bab7-117">**CIM \_ ManagedSystemElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7bab7-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bab7-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="7bab7-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bab7-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bab7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bab7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7bab7-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="7bab7-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7bab7-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="7bab7-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bab7-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bab7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bab7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-126">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7bab7-127">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="7bab7-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7bab7-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7bab7-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bab7-129">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7bab7-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bab7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-131">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="7bab7-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7bab7-132">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="7bab7-132">Indicates when the object was installed.</span></span> <span data-ttu-id="7bab7-133">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="7bab7-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="7bab7-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="7bab7-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bab7-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bab7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bab7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-137">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7bab7-138">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="7bab7-138">Label by which the object is known.</span></span> <span data-ttu-id="7bab7-139">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7bab7-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="7bab7-140">**狀態**</span><span class="sxs-lookup"><span data-stu-id="7bab7-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bab7-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7bab7-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7bab7-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bab7-143">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7bab7-144">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="7bab7-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="7bab7-145">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="7bab7-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7bab7-146">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="7bab7-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7bab7-147">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="7bab7-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7bab7-148">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="7bab7-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7bab7-149">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="7bab7-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7bab7-150">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="7bab7-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7bab7-151">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="7bab7-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7bab7-152">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7bab7-153">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7bab7-154">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7bab7-155">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7bab7-156">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7bab7-157">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7bab7-158">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7bab7-159">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7bab7-160">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7bab7-161">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7bab7-162">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7bab7-163">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="7bab7-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7bab7-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7bab7-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7bab7-165">備註</span><span class="sxs-lookup"><span data-stu-id="7bab7-165">Remarks</span></span>

<span data-ttu-id="7bab7-166">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7bab7-166">WMI does not implement this class.</span></span> <span data-ttu-id="7bab7-167">針對衍生自這個類別的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="7bab7-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7bab7-168">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7bab7-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7bab7-169">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7bab7-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bab7-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bab7-170">Requirements</span></span>



| <span data-ttu-id="7bab7-171">需求</span><span class="sxs-lookup"><span data-stu-id="7bab7-171">Requirement</span></span> | <span data-ttu-id="7bab7-172">值</span><span class="sxs-lookup"><span data-stu-id="7bab7-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bab7-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bab7-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7bab7-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bab7-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bab7-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bab7-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7bab7-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bab7-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bab7-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="7bab7-177">Namespace</span></span><br/>                | <span data-ttu-id="7bab7-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7bab7-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bab7-179">MOF</span><span class="sxs-lookup"><span data-stu-id="7bab7-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bab7-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bab7-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bab7-181">DLL</span><span class="sxs-lookup"><span data-stu-id="7bab7-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bab7-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bab7-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

