---
description: Win32 \_ COMApplication ABSTRACT WMI 類別代表 (COM) 應用程式的元件物件模型。 在此內容中，COM 應用程式是 COM 類別的邏輯群組。
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Win32_COMApplication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025978"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="8fd52-104">Win32 \_ COMApplication 類別</span><span class="sxs-lookup"><span data-stu-id="8fd52-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="8fd52-105">**Win32 \_ COMApplication** abstract [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 (COM) 應用程式的元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="8fd52-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="8fd52-106">在此內容中，COM 應用程式是 COM 類別的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="8fd52-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="8fd52-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd52-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8fd52-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8fd52-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd52-109">語法</span><span class="sxs-lookup"><span data-stu-id="8fd52-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8fd52-110">成員</span><span class="sxs-lookup"><span data-stu-id="8fd52-110">Members</span></span>

<span data-ttu-id="8fd52-111">**Win32 \_ COMApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8fd52-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="8fd52-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd52-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fd52-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8fd52-113">Properties</span></span>

<span data-ttu-id="8fd52-114">**Win32 \_ COMApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd52-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fd52-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="8fd52-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd52-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd52-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd52-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8fd52-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="8fd52-119">A short textual description of the object.</span></span>

<span data-ttu-id="8fd52-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd52-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="8fd52-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd52-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd52-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd52-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-124">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8fd52-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="8fd52-125">A textual description of the object.</span></span>

<span data-ttu-id="8fd52-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd52-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8fd52-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd52-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8fd52-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd52-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8fd52-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8fd52-131">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="8fd52-131">Indicates when the object was installed.</span></span> <span data-ttu-id="8fd52-132">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="8fd52-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8fd52-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd52-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8fd52-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd52-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd52-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd52-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-137">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8fd52-138">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="8fd52-138">Label by which the object is known.</span></span> <span data-ttu-id="8fd52-139">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="8fd52-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8fd52-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fd52-141">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8fd52-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fd52-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8fd52-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8fd52-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fd52-144">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8fd52-145">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="8fd52-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="8fd52-146">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="8fd52-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8fd52-147">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="8fd52-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8fd52-148">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="8fd52-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8fd52-149">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8fd52-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8fd52-150">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="8fd52-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8fd52-151">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8fd52-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8fd52-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8fd52-153">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8fd52-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8fd52-154">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8fd52-155">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8fd52-156">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8fd52-157">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8fd52-158">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8fd52-159">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8fd52-160">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8fd52-161">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8fd52-162">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8fd52-163">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8fd52-164">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8fd52-165">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="8fd52-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8fd52-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fd52-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8fd52-167">備註</span><span class="sxs-lookup"><span data-stu-id="8fd52-167">Remarks</span></span>

<span data-ttu-id="8fd52-168">**Win32 \_ COMApplication** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd52-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd52-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fd52-169">Requirements</span></span>



| <span data-ttu-id="8fd52-170">需求</span><span class="sxs-lookup"><span data-stu-id="8fd52-170">Requirement</span></span> | <span data-ttu-id="8fd52-171">值</span><span class="sxs-lookup"><span data-stu-id="8fd52-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd52-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fd52-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd52-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fd52-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fd52-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fd52-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd52-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fd52-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fd52-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fd52-176">Namespace</span></span><br/>                | <span data-ttu-id="8fd52-177">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8fd52-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8fd52-178">MOF</span><span class="sxs-lookup"><span data-stu-id="8fd52-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fd52-179"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fd52-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fd52-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8fd52-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fd52-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fd52-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd52-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fd52-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd52-183">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8fd52-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="8fd52-184">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8fd52-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

