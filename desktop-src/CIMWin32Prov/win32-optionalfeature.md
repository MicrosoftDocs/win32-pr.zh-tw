---
description: 代表存在於作業系統上之選用功能的狀態。
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Win32_OptionalFeature 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985591"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="15f54-103">Win32 \_ OptionalFeature 類別</span><span class="sxs-lookup"><span data-stu-id="15f54-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="15f54-104">代表存在於作業系統上之選用功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="15f54-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="15f54-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="15f54-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f54-106">語法</span><span class="sxs-lookup"><span data-stu-id="15f54-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="15f54-107">成員</span><span class="sxs-lookup"><span data-stu-id="15f54-107">Members</span></span>

<span data-ttu-id="15f54-108">**Win32 \_ OptionalFeature** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="15f54-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="15f54-109">屬性</span><span class="sxs-lookup"><span data-stu-id="15f54-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15f54-110">屬性</span><span class="sxs-lookup"><span data-stu-id="15f54-110">Properties</span></span>

<span data-ttu-id="15f54-111">**Win32 \_ OptionalFeature** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="15f54-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15f54-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="15f54-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15f54-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f54-115">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) (標題) 、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (260) </span><span class="sxs-lookup"><span data-stu-id="15f54-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="15f54-116">選用的功能顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="15f54-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="15f54-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="15f54-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15f54-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f54-120">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="15f54-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="15f54-121">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="15f54-121">A textual description of the object.</span></span>

<span data-ttu-id="15f54-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="15f54-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15f54-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="15f54-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-124">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="15f54-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f54-126">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="15f54-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="15f54-127">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="15f54-127">Indicates when the object was installed.</span></span> <span data-ttu-id="15f54-128">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="15f54-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="15f54-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="15f54-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15f54-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="15f54-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="15f54-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15f54-133">識別選用功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="15f54-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="15f54-134">可能的狀態如下：</span><span class="sxs-lookup"><span data-stu-id="15f54-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="15f54-135">**已啟用** (1) </span><span class="sxs-lookup"><span data-stu-id="15f54-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="15f54-136">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="15f54-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="15f54-137">不 **存在** (3) </span><span class="sxs-lookup"><span data-stu-id="15f54-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15f54-138">**未知** 的 (4) </span><span class="sxs-lookup"><span data-stu-id="15f54-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15f54-139">**名稱**</span><span class="sxs-lookup"><span data-stu-id="15f54-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15f54-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f54-142">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) (名稱) 、 [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (260) </span><span class="sxs-lookup"><span data-stu-id="15f54-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="15f54-143">代表選用功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="15f54-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="15f54-144">**狀態**</span><span class="sxs-lookup"><span data-stu-id="15f54-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15f54-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="15f54-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15f54-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="15f54-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15f54-147">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="15f54-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="15f54-148">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="15f54-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="15f54-149">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="15f54-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="15f54-150">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="15f54-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="15f54-151">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="15f54-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="15f54-152">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="15f54-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="15f54-153">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="15f54-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="15f54-154">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="15f54-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="15f54-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="15f54-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="15f54-156">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="15f54-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="15f54-157">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="15f54-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="15f54-158">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="15f54-159">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15f54-160">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="15f54-161">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="15f54-162">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="15f54-163">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="15f54-164">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="15f54-165">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="15f54-166">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="15f54-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="15f54-167">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="15f54-168">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="15f54-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="15f54-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="15f54-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="15f54-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="15f54-170">Requirements</span></span>



| <span data-ttu-id="15f54-171">需求</span><span class="sxs-lookup"><span data-stu-id="15f54-171">Requirement</span></span> | <span data-ttu-id="15f54-172">值</span><span class="sxs-lookup"><span data-stu-id="15f54-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15f54-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15f54-173">Minimum supported client</span></span><br/> | <span data-ttu-id="15f54-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15f54-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="15f54-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15f54-175">Minimum supported server</span></span><br/> | <span data-ttu-id="15f54-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="15f54-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="15f54-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="15f54-177">Namespace</span></span><br/>                | <span data-ttu-id="15f54-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15f54-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15f54-179">MOF</span><span class="sxs-lookup"><span data-stu-id="15f54-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15f54-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="15f54-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15f54-181">DLL</span><span class="sxs-lookup"><span data-stu-id="15f54-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15f54-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15f54-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f54-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15f54-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f54-184">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="15f54-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="15f54-185">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="15f54-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="15f54-186">查詢選用功能的狀態</span><span class="sxs-lookup"><span data-stu-id="15f54-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
