---
description: Win32 \_ DCOMAPPLICATION WMI 類別代表 DCOM 應用程式的屬性。
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Win32_DCOMApplication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991654"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="0b17d-103">Win32 \_ DCOMApplication 類別</span><span class="sxs-lookup"><span data-stu-id="0b17d-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="0b17d-104">**Win32 \_ DCOMApplication** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 DCOM 應用程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b17d-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="0b17d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b17d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0b17d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0b17d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b17d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0b17d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="0b17d-108">成員</span><span class="sxs-lookup"><span data-stu-id="0b17d-108">Members</span></span>

<span data-ttu-id="0b17d-109">**Win32 \_ DCOMApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0b17d-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="0b17d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0b17d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b17d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0b17d-111">Properties</span></span>

<span data-ttu-id="0b17d-112">**Win32 \_ DCOMApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0b17d-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b17d-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="0b17d-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b17d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-116">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] " ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-117">DCOM 應用程式的全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="0b17d-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="0b17d-118">**標題**</span><span class="sxs-lookup"><span data-stu-id="0b17d-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b17d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-121">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-122">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0b17d-122">A short textual description of the object.</span></span>

<span data-ttu-id="0b17d-123">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b17d-124">**說明**</span><span class="sxs-lookup"><span data-stu-id="0b17d-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b17d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-127">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-128">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0b17d-128">A textual description of the object.</span></span>

<span data-ttu-id="0b17d-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b17d-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b17d-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0b17d-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-133">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0b17d-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-134">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0b17d-134">Indicates when the object was installed.</span></span> <span data-ttu-id="0b17d-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0b17d-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0b17d-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b17d-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0b17d-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b17d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-140">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-141">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0b17d-141">Label by which the object is known.</span></span> <span data-ttu-id="0b17d-142">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0b17d-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0b17d-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b17d-144">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0b17d-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b17d-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0b17d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0b17d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b17d-147">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0b17d-148">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0b17d-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="0b17d-149">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0b17d-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0b17d-150">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0b17d-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0b17d-151">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0b17d-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0b17d-152">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0b17d-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0b17d-153">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0b17d-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0b17d-154">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0b17d-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0b17d-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b17d-156">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0b17d-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b17d-157">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0b17d-158">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b17d-159">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b17d-160">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0b17d-161">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0b17d-162">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0b17d-163">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0b17d-164">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0b17d-165">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0b17d-166">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0b17d-167">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0b17d-168">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0b17d-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="0b17d-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0b17d-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0b17d-170">備註</span><span class="sxs-lookup"><span data-stu-id="0b17d-170">Remarks</span></span>

<span data-ttu-id="0b17d-171">**Win32 \_ DCOMApplication** 類別衍生自 [**win32 \_ COMApplication**](win32-comapplication.md)。</span><span class="sxs-lookup"><span data-stu-id="0b17d-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b17d-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b17d-172">Requirements</span></span>



| <span data-ttu-id="0b17d-173">需求</span><span class="sxs-lookup"><span data-stu-id="0b17d-173">Requirement</span></span> | <span data-ttu-id="0b17d-174">值</span><span class="sxs-lookup"><span data-stu-id="0b17d-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b17d-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b17d-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0b17d-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b17d-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b17d-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b17d-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0b17d-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b17d-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b17d-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="0b17d-179">Namespace</span></span><br/>                | <span data-ttu-id="0b17d-180">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0b17d-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b17d-181">MOF</span><span class="sxs-lookup"><span data-stu-id="0b17d-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b17d-182"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b17d-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b17d-183">DLL</span><span class="sxs-lookup"><span data-stu-id="0b17d-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b17d-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b17d-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b17d-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b17d-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b17d-186">**Win32 \_ COMApplication**</span><span class="sxs-lookup"><span data-stu-id="0b17d-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="0b17d-187">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b17d-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

