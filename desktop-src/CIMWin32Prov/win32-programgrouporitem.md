---
description: Win32 \_ ProgramGroupOrItem ABSTRACT WMI 類別代表使用者的 [啟動程式] 功能表上程式的邏輯群組 \\ 。 它包含程式群組和程式群組專案。
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Win32_ProgramGroupOrItem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110225"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="2a343-104">Win32 \_ ProgramGroupOrItem 類別</span><span class="sxs-lookup"><span data-stu-id="2a343-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="2a343-105">**Win32 \_ ProgramGroupOrItem** abstract [WMI 類別](../wmisdk/retrieving-a-class.md)代表使用者的 [**啟動 \\ 程式**] 功能表上程式的邏輯群組。</span><span class="sxs-lookup"><span data-stu-id="2a343-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="2a343-106">它包含程式群組和程式群組專案。</span><span class="sxs-lookup"><span data-stu-id="2a343-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="2a343-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2a343-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2a343-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="2a343-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a343-109">語法</span><span class="sxs-lookup"><span data-stu-id="2a343-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="2a343-110">成員</span><span class="sxs-lookup"><span data-stu-id="2a343-110">Members</span></span>

<span data-ttu-id="2a343-111">**Win32 \_ ProgramGroupOrItem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2a343-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="2a343-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2a343-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a343-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2a343-113">Properties</span></span>

<span data-ttu-id="2a343-114">**Win32 \_ ProgramGroupOrItem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2a343-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a343-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="2a343-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a343-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a343-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a343-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2a343-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a343-118">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="2a343-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2a343-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2a343-119">A short textual description of the object.</span></span>

<span data-ttu-id="2a343-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a343-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="2a343-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a343-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a343-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a343-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2a343-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a343-124">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="2a343-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2a343-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2a343-125">A textual description of the object.</span></span>

<span data-ttu-id="2a343-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a343-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2a343-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a343-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2a343-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a343-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2a343-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a343-130">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="2a343-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2a343-131">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="2a343-131">Indicates when the object was installed.</span></span> <span data-ttu-id="2a343-132">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="2a343-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2a343-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a343-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2a343-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a343-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a343-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a343-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2a343-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a343-137">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2a343-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2a343-138">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2a343-138">Label by which the object is known.</span></span> <span data-ttu-id="2a343-139">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2a343-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2a343-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a343-141">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2a343-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a343-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2a343-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a343-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2a343-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a343-144">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="2a343-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2a343-145">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="2a343-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="2a343-146">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="2a343-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2a343-147">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="2a343-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2a343-148">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="2a343-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2a343-149">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="2a343-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2a343-150">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="2a343-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2a343-151">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="2a343-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2a343-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2a343-153">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="2a343-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2a343-154">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="2a343-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2a343-155">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2a343-156">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a343-157">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2a343-158">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2a343-159">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2a343-160">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2a343-161">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2a343-162">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2a343-163">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="2a343-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2a343-164">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2a343-165">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="2a343-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2a343-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2a343-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2a343-167">備註</span><span class="sxs-lookup"><span data-stu-id="2a343-167">Remarks</span></span>

<span data-ttu-id="2a343-168">**Win32 \_ ProgramGroupOrItem** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2a343-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a343-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a343-169">Requirements</span></span>



| <span data-ttu-id="2a343-170">需求</span><span class="sxs-lookup"><span data-stu-id="2a343-170">Requirement</span></span> | <span data-ttu-id="2a343-171">值</span><span class="sxs-lookup"><span data-stu-id="2a343-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a343-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a343-172">Minimum supported client</span></span><br/> | <span data-ttu-id="2a343-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a343-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a343-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a343-174">Minimum supported server</span></span><br/> | <span data-ttu-id="2a343-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a343-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a343-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a343-176">Namespace</span></span><br/>                | <span data-ttu-id="2a343-177">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2a343-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a343-178">MOF</span><span class="sxs-lookup"><span data-stu-id="2a343-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a343-179"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a343-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a343-180">DLL</span><span class="sxs-lookup"><span data-stu-id="2a343-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a343-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a343-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a343-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a343-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a343-183">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="2a343-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="2a343-184">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="2a343-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
