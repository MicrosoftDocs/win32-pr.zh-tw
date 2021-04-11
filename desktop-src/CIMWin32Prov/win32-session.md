---
description: Win32 \_ 會話類別會定義使用者與資源（例如電腦系統或終端機會話）之間互動的相關狀態資訊。
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Win32_Session 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025842"
---
# <a name="win32_session-class"></a><span data-ttu-id="28f72-103">Win32 \_ 會話類別</span><span class="sxs-lookup"><span data-stu-id="28f72-103">Win32\_Session class</span></span>

<span data-ttu-id="28f72-104">**Win32 \_ 會話** 類別會定義使用者與資源（例如電腦系統或終端機會話）之間互動的相關狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="28f72-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="28f72-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="28f72-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="28f72-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="28f72-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f72-107">語法</span><span class="sxs-lookup"><span data-stu-id="28f72-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="28f72-108">成員</span><span class="sxs-lookup"><span data-stu-id="28f72-108">Members</span></span>

<span data-ttu-id="28f72-109">**Win32 \_ 會話** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="28f72-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="28f72-110">屬性</span><span class="sxs-lookup"><span data-stu-id="28f72-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28f72-111">屬性</span><span class="sxs-lookup"><span data-stu-id="28f72-111">Properties</span></span>

<span data-ttu-id="28f72-112">**Win32 \_ 會話** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="28f72-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28f72-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="28f72-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28f72-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28f72-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="28f72-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="28f72-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="28f72-117">A short textual description of the object.</span></span>

<span data-ttu-id="28f72-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28f72-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="28f72-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28f72-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28f72-122">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="28f72-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="28f72-123">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="28f72-123">A textual description of the object.</span></span>

<span data-ttu-id="28f72-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28f72-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="28f72-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="28f72-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28f72-128">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="28f72-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="28f72-129">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="28f72-129">Indicates when the object was installed.</span></span> <span data-ttu-id="28f72-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="28f72-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="28f72-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28f72-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="28f72-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28f72-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28f72-135">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="28f72-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="28f72-136">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="28f72-136">Label by which the object is known.</span></span> <span data-ttu-id="28f72-137">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="28f72-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="28f72-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="28f72-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="28f72-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="28f72-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28f72-142">會話開始的時間。</span><span class="sxs-lookup"><span data-stu-id="28f72-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="28f72-143">**狀態**</span><span class="sxs-lookup"><span data-stu-id="28f72-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28f72-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="28f72-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28f72-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="28f72-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28f72-146">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="28f72-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="28f72-147">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="28f72-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="28f72-148">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="28f72-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="28f72-149">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="28f72-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="28f72-150">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="28f72-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="28f72-151">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="28f72-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="28f72-152">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="28f72-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="28f72-153">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="28f72-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="28f72-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="28f72-155">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="28f72-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="28f72-156">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="28f72-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="28f72-157">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="28f72-158">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="28f72-159">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="28f72-160">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="28f72-161">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="28f72-162">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="28f72-163">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="28f72-164">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="28f72-165">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="28f72-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="28f72-166">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="28f72-167">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="28f72-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="28f72-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="28f72-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="28f72-169">備註</span><span class="sxs-lookup"><span data-stu-id="28f72-169">Remarks</span></span>

<span data-ttu-id="28f72-170">**Win32 \_ 會話** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="28f72-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28f72-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="28f72-171">Requirements</span></span>



| <span data-ttu-id="28f72-172">需求</span><span class="sxs-lookup"><span data-stu-id="28f72-172">Requirement</span></span> | <span data-ttu-id="28f72-173">值</span><span class="sxs-lookup"><span data-stu-id="28f72-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28f72-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28f72-174">Minimum supported client</span></span><br/> | <span data-ttu-id="28f72-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28f72-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28f72-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28f72-176">Minimum supported server</span></span><br/> | <span data-ttu-id="28f72-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28f72-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28f72-178">命名空間</span><span class="sxs-lookup"><span data-stu-id="28f72-178">Namespace</span></span><br/>                | <span data-ttu-id="28f72-179">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="28f72-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28f72-180">MOF</span><span class="sxs-lookup"><span data-stu-id="28f72-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28f72-181"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="28f72-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28f72-182">DLL</span><span class="sxs-lookup"><span data-stu-id="28f72-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28f72-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28f72-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f72-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28f72-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f72-185">**CIM \_ logicalElement**</span><span class="sxs-lookup"><span data-stu-id="28f72-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
