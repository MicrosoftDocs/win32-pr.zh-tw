---
description: Win32 \_ comclass.zip 抽象 WMI 類別代表元件物件模型 (COM) 元件的屬性。
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Win32_COMClass 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936423"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="07712-103">Win32 \_ comclass.zip 類別</span><span class="sxs-lookup"><span data-stu-id="07712-103">Win32\_COMClass class</span></span>

<span data-ttu-id="07712-104">**Win32 \_ Comclass.zip** 抽象 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表元件物件模型 (COM) 元件的屬性。</span><span class="sxs-lookup"><span data-stu-id="07712-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="07712-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="07712-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="07712-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="07712-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07712-107">語法</span><span class="sxs-lookup"><span data-stu-id="07712-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="07712-108">成員</span><span class="sxs-lookup"><span data-stu-id="07712-108">Members</span></span>

<span data-ttu-id="07712-109">**Win32 \_ comclass.zip** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="07712-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="07712-110">屬性</span><span class="sxs-lookup"><span data-stu-id="07712-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07712-111">屬性</span><span class="sxs-lookup"><span data-stu-id="07712-111">Properties</span></span>

<span data-ttu-id="07712-112">**Win32 \_ comclass.zip** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="07712-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07712-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="07712-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07712-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07712-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07712-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07712-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07712-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="07712-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07712-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="07712-117">A short textual description of the object.</span></span>

<span data-ttu-id="07712-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07712-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="07712-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07712-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07712-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07712-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07712-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07712-122">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="07712-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07712-123">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="07712-123">A textual description of the object.</span></span>

<span data-ttu-id="07712-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07712-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07712-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07712-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="07712-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07712-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07712-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07712-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="07712-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07712-129">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="07712-129">Indicates when the object was installed.</span></span> <span data-ttu-id="07712-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="07712-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="07712-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07712-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="07712-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07712-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07712-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07712-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07712-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07712-135">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="07712-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="07712-136">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="07712-136">Label by which the object is known.</span></span> <span data-ttu-id="07712-137">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="07712-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="07712-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07712-139">**狀態**</span><span class="sxs-lookup"><span data-stu-id="07712-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07712-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="07712-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07712-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="07712-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07712-142">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="07712-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07712-143">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="07712-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="07712-144">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="07712-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="07712-145">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="07712-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="07712-146">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="07712-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="07712-147">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="07712-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07712-148">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="07712-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07712-149">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="07712-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07712-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07712-151">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="07712-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07712-152">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="07712-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07712-153">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07712-154">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07712-155">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07712-156">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07712-157">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07712-158">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07712-159">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07712-160">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07712-161">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="07712-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07712-162">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07712-163">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="07712-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="07712-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="07712-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="07712-165">備註</span><span class="sxs-lookup"><span data-stu-id="07712-165">Remarks</span></span>

<span data-ttu-id="07712-166">**Win32 \_ comclass.zip** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="07712-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07712-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="07712-167">Requirements</span></span>



| <span data-ttu-id="07712-168">需求</span><span class="sxs-lookup"><span data-stu-id="07712-168">Requirement</span></span> | <span data-ttu-id="07712-169">值</span><span class="sxs-lookup"><span data-stu-id="07712-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07712-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07712-170">Minimum supported client</span></span><br/> | <span data-ttu-id="07712-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07712-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07712-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07712-172">Minimum supported server</span></span><br/> | <span data-ttu-id="07712-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07712-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07712-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="07712-174">Namespace</span></span><br/>                | <span data-ttu-id="07712-175">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07712-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07712-176">MOF</span><span class="sxs-lookup"><span data-stu-id="07712-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07712-177"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="07712-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07712-178">DLL</span><span class="sxs-lookup"><span data-stu-id="07712-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07712-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07712-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07712-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07712-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07712-181">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="07712-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="07712-182">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07712-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

