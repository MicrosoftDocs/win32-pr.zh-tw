---
description: Win32 \_ COMPONENTCATEGORY WMI 類別代表元件類別。
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Win32_ComponentCategory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936422"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="60feb-103">Win32 \_ ComponentCategory 類別</span><span class="sxs-lookup"><span data-stu-id="60feb-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="60feb-104">**Win32 \_ ComponentCategory** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表元件類別。</span><span class="sxs-lookup"><span data-stu-id="60feb-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="60feb-105">元件類別是元件物件模型的群組， (COM) 類別，並在兩者之間共用已定義的功能集。</span><span class="sxs-lookup"><span data-stu-id="60feb-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="60feb-106">使用這些介面的用戶端會查詢登錄中的分類標題和唯一識別碼 **，稱為 [類別目錄**]，這是從全域唯一識別碼 (GUID) 所建立。</span><span class="sxs-lookup"><span data-stu-id="60feb-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="60feb-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="60feb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="60feb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="60feb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60feb-109">語法</span><span class="sxs-lookup"><span data-stu-id="60feb-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="60feb-110">成員</span><span class="sxs-lookup"><span data-stu-id="60feb-110">Members</span></span>

<span data-ttu-id="60feb-111">**Win32 \_ ComponentCategory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="60feb-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="60feb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="60feb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60feb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="60feb-113">Properties</span></span>

<span data-ttu-id="60feb-114">**Win32 \_ ComponentCategory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="60feb-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60feb-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="60feb-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="60feb-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="60feb-119">A short textual description of the object.</span></span>

<span data-ttu-id="60feb-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="60feb-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60feb-121">**CategoryId**</span><span class="sxs-lookup"><span data-stu-id="60feb-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="60feb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-124">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 元件類別 \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| catid" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-125">此元件類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="60feb-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="60feb-126">**說明**</span><span class="sxs-lookup"><span data-stu-id="60feb-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="60feb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-129">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-130">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="60feb-130">A textual description of the object.</span></span>

<span data-ttu-id="60feb-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="60feb-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60feb-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60feb-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="60feb-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-135">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="60feb-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-136">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="60feb-136">Indicates when the object was installed.</span></span> <span data-ttu-id="60feb-137">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="60feb-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="60feb-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="60feb-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60feb-139">**名稱**</span><span class="sxs-lookup"><span data-stu-id="60feb-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="60feb-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-142">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| 元件類別 \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| szDescription" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-143">Name 屬性工作表示這個元件類別的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="60feb-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="60feb-144">**狀態**</span><span class="sxs-lookup"><span data-stu-id="60feb-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60feb-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="60feb-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60feb-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="60feb-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60feb-147">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="60feb-148">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="60feb-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="60feb-149">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="60feb-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="60feb-150">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="60feb-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="60feb-151">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="60feb-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="60feb-152">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="60feb-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="60feb-153">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="60feb-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="60feb-154">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="60feb-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="60feb-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="60feb-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="60feb-156">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="60feb-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="60feb-157">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="60feb-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="60feb-158">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="60feb-159">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60feb-160">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="60feb-161">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="60feb-162">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="60feb-163">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="60feb-164">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="60feb-165">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="60feb-166">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="60feb-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="60feb-167">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="60feb-168">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="60feb-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="60feb-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="60feb-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="60feb-170">備註</span><span class="sxs-lookup"><span data-stu-id="60feb-170">Remarks</span></span>

<span data-ttu-id="60feb-171">**Win32 \_ ComponentCategory** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="60feb-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60feb-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="60feb-172">Requirements</span></span>



| <span data-ttu-id="60feb-173">需求</span><span class="sxs-lookup"><span data-stu-id="60feb-173">Requirement</span></span> | <span data-ttu-id="60feb-174">值</span><span class="sxs-lookup"><span data-stu-id="60feb-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60feb-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60feb-175">Minimum supported client</span></span><br/> | <span data-ttu-id="60feb-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60feb-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60feb-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60feb-177">Minimum supported server</span></span><br/> | <span data-ttu-id="60feb-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60feb-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60feb-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="60feb-179">Namespace</span></span><br/>                | <span data-ttu-id="60feb-180">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60feb-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60feb-181">MOF</span><span class="sxs-lookup"><span data-stu-id="60feb-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60feb-182"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="60feb-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60feb-183">DLL</span><span class="sxs-lookup"><span data-stu-id="60feb-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60feb-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60feb-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60feb-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60feb-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60feb-186">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="60feb-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="60feb-187">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60feb-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

