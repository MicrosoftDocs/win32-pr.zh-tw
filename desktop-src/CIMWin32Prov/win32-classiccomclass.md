---
description: Win32 \_ CLASSICCOMCLASS WMI 類別代表 COM 元件的屬性。
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Win32_ClassicCOMClass 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972569"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="59556-103">Win32 \_ ClassicCOMClass 類別</span><span class="sxs-lookup"><span data-stu-id="59556-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="59556-104">**Win32 \_ ClassicCOMClass** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 COM 元件的屬性。</span><span class="sxs-lookup"><span data-stu-id="59556-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="59556-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="59556-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="59556-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="59556-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="59556-107">語法</span><span class="sxs-lookup"><span data-stu-id="59556-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="59556-108">成員</span><span class="sxs-lookup"><span data-stu-id="59556-108">Members</span></span>

<span data-ttu-id="59556-109">**Win32 \_ ClassicCOMClass** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="59556-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="59556-110">屬性</span><span class="sxs-lookup"><span data-stu-id="59556-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59556-111">屬性</span><span class="sxs-lookup"><span data-stu-id="59556-111">Properties</span></span>

<span data-ttu-id="59556-112">**Win32 \_ ClassicCOMClass** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="59556-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59556-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="59556-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59556-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59556-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="59556-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="59556-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="59556-117">A short textual description of the object.</span></span>

<span data-ttu-id="59556-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="59556-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59556-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="59556-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59556-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59556-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-122">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="59556-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="59556-123">這個 COM 類別 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="59556-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="59556-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="59556-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59556-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59556-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-127">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="59556-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="59556-128">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="59556-128">A textual description of the object.</span></span>

<span data-ttu-id="59556-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="59556-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59556-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="59556-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="59556-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59556-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-133">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="59556-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="59556-134">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="59556-134">Indicates when the object was installed.</span></span> <span data-ttu-id="59556-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="59556-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="59556-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="59556-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="59556-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="59556-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59556-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59556-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-140">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="59556-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="59556-141">Name 屬性包含 COM 類別的人類可讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="59556-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="59556-142">**狀態**</span><span class="sxs-lookup"><span data-stu-id="59556-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59556-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59556-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59556-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59556-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59556-145">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="59556-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="59556-146">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="59556-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="59556-147">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="59556-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="59556-148">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="59556-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="59556-149">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="59556-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="59556-150">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="59556-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="59556-151">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="59556-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="59556-152">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="59556-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="59556-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="59556-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="59556-154">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="59556-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="59556-155">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="59556-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="59556-156">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="59556-157">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="59556-158">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="59556-159">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="59556-160">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="59556-161">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="59556-162">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="59556-163">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="59556-164">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="59556-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="59556-165">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="59556-166">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="59556-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="59556-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="59556-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="59556-168">備註</span><span class="sxs-lookup"><span data-stu-id="59556-168">Remarks</span></span>

<span data-ttu-id="59556-169">**Win32 \_ ClassicCOMClass** 類別衍生自 [**win32 \_ comclass.zip**](win32-comclass.md)。</span><span class="sxs-lookup"><span data-stu-id="59556-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59556-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="59556-170">Requirements</span></span>



| <span data-ttu-id="59556-171">需求</span><span class="sxs-lookup"><span data-stu-id="59556-171">Requirement</span></span> | <span data-ttu-id="59556-172">值</span><span class="sxs-lookup"><span data-stu-id="59556-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59556-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59556-173">Minimum supported client</span></span><br/> | <span data-ttu-id="59556-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59556-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59556-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59556-175">Minimum supported server</span></span><br/> | <span data-ttu-id="59556-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59556-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59556-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="59556-177">Namespace</span></span><br/>                | <span data-ttu-id="59556-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="59556-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59556-179">MOF</span><span class="sxs-lookup"><span data-stu-id="59556-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59556-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="59556-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59556-181">DLL</span><span class="sxs-lookup"><span data-stu-id="59556-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59556-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59556-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59556-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59556-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59556-184">**Win32 \_ comclass.zip**</span><span class="sxs-lookup"><span data-stu-id="59556-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="59556-185">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59556-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

