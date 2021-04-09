---
description: Win32 \_ NETWORKCLIENT WMI 類別代表 Windows 系統上的網路用戶端。 網路上具有與系統之間的用戶端關係的任何電腦系統，都是此類別 (或成員) 的子系。
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Win32_NetworkClient 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936452"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="50ab4-104">Win32 \_ NetworkClient 類別</span><span class="sxs-lookup"><span data-stu-id="50ab4-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="50ab4-105">**Win32 \_ NetworkClient** [WMI 類別](../wmisdk/retrieving-a-class.md)代表 Windows 系統上的網路用戶端。</span><span class="sxs-lookup"><span data-stu-id="50ab4-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="50ab4-106">網路上具有與系統之間的用戶端關係的任何電腦系統，都是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="50ab4-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="50ab4-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="50ab4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="50ab4-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="50ab4-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="50ab4-109">語法</span><span class="sxs-lookup"><span data-stu-id="50ab4-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="50ab4-110">成員</span><span class="sxs-lookup"><span data-stu-id="50ab4-110">Members</span></span>

<span data-ttu-id="50ab4-111">**Win32 \_ NetworkClient** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="50ab4-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="50ab4-112">屬性</span><span class="sxs-lookup"><span data-stu-id="50ab4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50ab4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="50ab4-113">Properties</span></span>

<span data-ttu-id="50ab4-114">**Win32 \_ NetworkClient** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="50ab4-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50ab4-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="50ab4-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50ab4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-118">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-119">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="50ab4-119">A short textual description of the object.</span></span>

<span data-ttu-id="50ab4-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="50ab4-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50ab4-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="50ab4-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50ab4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-124">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-125">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="50ab4-125">A textual description of the object.</span></span>

<span data-ttu-id="50ab4-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="50ab4-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50ab4-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="50ab4-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="50ab4-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-130">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="50ab4-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-131">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="50ab4-131">Indicates when the object was installed.</span></span> <span data-ttu-id="50ab4-132">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="50ab4-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="50ab4-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="50ab4-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="50ab4-134">**製造商**</span><span class="sxs-lookup"><span data-stu-id="50ab4-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50ab4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-137">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| 製造業" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-138">執行 Windows 的電腦系統上執行之網路用戶端的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="50ab4-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="50ab4-139">範例： "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="50ab4-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="50ab4-140">**名稱**</span><span class="sxs-lookup"><span data-stu-id="50ab4-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50ab4-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-143">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| Name" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-144">在執行 Windows 的電腦系統上執行之網路用戶端的網路名稱。</span><span class="sxs-lookup"><span data-stu-id="50ab4-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="50ab4-145">範例：「Microsoft Windows 網路」</span><span class="sxs-lookup"><span data-stu-id="50ab4-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="50ab4-146">**狀態**</span><span class="sxs-lookup"><span data-stu-id="50ab4-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50ab4-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="50ab4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="50ab4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50ab4-149">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="50ab4-150">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="50ab4-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="50ab4-151">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="50ab4-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="50ab4-152">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="50ab4-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="50ab4-153">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="50ab4-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="50ab4-154">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="50ab4-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="50ab4-155">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="50ab4-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="50ab4-156">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="50ab4-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="50ab4-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="50ab4-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="50ab4-158">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="50ab4-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="50ab4-159">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="50ab4-160">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="50ab4-161">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="50ab4-162">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="50ab4-163">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="50ab4-164">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="50ab4-165">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="50ab4-166">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="50ab4-167">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="50ab4-168">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="50ab4-169">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="50ab4-170">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="50ab4-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="50ab4-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="50ab4-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="50ab4-172">備註</span><span class="sxs-lookup"><span data-stu-id="50ab4-172">Remarks</span></span>

<span data-ttu-id="50ab4-173">**Win32 \_ NetworkClient** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="50ab4-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50ab4-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="50ab4-174">Requirements</span></span>



| <span data-ttu-id="50ab4-175">需求</span><span class="sxs-lookup"><span data-stu-id="50ab4-175">Requirement</span></span> | <span data-ttu-id="50ab4-176">值</span><span class="sxs-lookup"><span data-stu-id="50ab4-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50ab4-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50ab4-177">Minimum supported client</span></span><br/> | <span data-ttu-id="50ab4-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50ab4-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50ab4-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50ab4-179">Minimum supported server</span></span><br/> | <span data-ttu-id="50ab4-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50ab4-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50ab4-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="50ab4-181">Namespace</span></span><br/>                | <span data-ttu-id="50ab4-182">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="50ab4-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="50ab4-183">MOF</span><span class="sxs-lookup"><span data-stu-id="50ab4-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50ab4-184"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="50ab4-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="50ab4-185">DLL</span><span class="sxs-lookup"><span data-stu-id="50ab4-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50ab4-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50ab4-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50ab4-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50ab4-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ab4-188">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="50ab4-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="50ab4-189">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="50ab4-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
