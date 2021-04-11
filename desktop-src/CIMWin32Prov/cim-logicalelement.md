---
description: CIM \_ LogicalElement 類別是代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: 'CIM_LogicalElement 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847114"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="a8709-103">CIM_LogicalElement 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="a8709-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a8709-104">**CIM \_ LogicalElement** 類別是代表抽象系統元件的所有系統元件的基類，例如設定檔、進程或系統功能（以邏輯裝置的形式）。</span><span class="sxs-lookup"><span data-stu-id="a8709-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8709-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a8709-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8709-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a8709-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8709-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8709-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a8709-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a8709-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8709-109">語法</span><span class="sxs-lookup"><span data-stu-id="a8709-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a8709-110">成員</span><span class="sxs-lookup"><span data-stu-id="a8709-110">Members</span></span>

<span data-ttu-id="a8709-111">**CIM \_ LogicalElement** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8709-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a8709-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a8709-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8709-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a8709-113">Properties</span></span>

<span data-ttu-id="a8709-114">**CIM \_ LogicalElement** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8709-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8709-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="a8709-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8709-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8709-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8709-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8709-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8709-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a8709-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a8709-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="a8709-119">A short textual description of the object.</span></span>

<span data-ttu-id="a8709-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8709-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="a8709-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8709-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8709-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8709-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8709-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8709-124">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a8709-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a8709-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a8709-125">A textual description of the object.</span></span>

<span data-ttu-id="a8709-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8709-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a8709-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8709-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a8709-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8709-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8709-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8709-130">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a8709-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a8709-131">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="a8709-131">Indicates when the object was installed.</span></span> <span data-ttu-id="a8709-132">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="a8709-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a8709-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8709-134">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a8709-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8709-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8709-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8709-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8709-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8709-137">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="a8709-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a8709-138">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a8709-138">Label by which the object is known.</span></span> <span data-ttu-id="a8709-139">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="a8709-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a8709-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8709-141">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a8709-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8709-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a8709-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8709-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a8709-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8709-144">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a8709-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a8709-145">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="a8709-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="a8709-146">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="a8709-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a8709-147">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="a8709-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a8709-148">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="a8709-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a8709-149">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a8709-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a8709-150">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="a8709-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a8709-151">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a8709-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a8709-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a8709-153">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a8709-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a8709-154">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a8709-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a8709-155">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a8709-156">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a8709-157">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a8709-158">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a8709-159">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a8709-160">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a8709-161">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a8709-162">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a8709-163">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a8709-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a8709-164">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a8709-165">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a8709-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a8709-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a8709-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a8709-167">備註</span><span class="sxs-lookup"><span data-stu-id="a8709-167">Remarks</span></span>

<span data-ttu-id="a8709-168">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a8709-168">WMI does not implement this class.</span></span> <span data-ttu-id="a8709-169">針對衍生自 **CIM \_ LogicalElement** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a8709-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a8709-170">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a8709-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8709-171">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a8709-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8709-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8709-172">Requirements</span></span>



| <span data-ttu-id="a8709-173">需求</span><span class="sxs-lookup"><span data-stu-id="a8709-173">Requirement</span></span> | <span data-ttu-id="a8709-174">值</span><span class="sxs-lookup"><span data-stu-id="a8709-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8709-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8709-175">Minimum supported client</span></span><br/> | <span data-ttu-id="a8709-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8709-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8709-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8709-177">Minimum supported server</span></span><br/> | <span data-ttu-id="a8709-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8709-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8709-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8709-179">Namespace</span></span><br/>                | <span data-ttu-id="a8709-180">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8709-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8709-181">MOF</span><span class="sxs-lookup"><span data-stu-id="a8709-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8709-182"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8709-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8709-183">DLL</span><span class="sxs-lookup"><span data-stu-id="a8709-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8709-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8709-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8709-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8709-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8709-186">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="a8709-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

