---
description: Win32 \_ LOADORDERGROUP WMI 類別代表一組定義執行相依性的系統服務。
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Win32_LoadOrderGroup 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111368"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="878a4-103">Win32 \_ LoadOrderGroup 類別</span><span class="sxs-lookup"><span data-stu-id="878a4-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="878a4-104">**Win32 \_ LoadOrderGroup** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表一組定義執行相依性的系統服務。</span><span class="sxs-lookup"><span data-stu-id="878a4-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="878a4-105">服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。</span><span class="sxs-lookup"><span data-stu-id="878a4-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="878a4-106">這些相依服務需要有前面的服務才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="878a4-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="878a4-107">此類別中的資料是由提供者從登錄機碼衍生： **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**。</span><span class="sxs-lookup"><span data-stu-id="878a4-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="878a4-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="878a4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="878a4-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="878a4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="878a4-110">語法</span><span class="sxs-lookup"><span data-stu-id="878a4-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="878a4-111">成員</span><span class="sxs-lookup"><span data-stu-id="878a4-111">Members</span></span>

<span data-ttu-id="878a4-112">**Win32 \_ LoadOrderGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="878a4-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="878a4-113">屬性</span><span class="sxs-lookup"><span data-stu-id="878a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="878a4-114">屬性</span><span class="sxs-lookup"><span data-stu-id="878a4-114">Properties</span></span>

<span data-ttu-id="878a4-115">**Win32 \_ LoadOrderGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="878a4-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="878a4-116">**標題**</span><span class="sxs-lookup"><span data-stu-id="878a4-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="878a4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-119">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-120">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="878a4-120">A short textual description of the object.</span></span>

<span data-ttu-id="878a4-121">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="878a4-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="878a4-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="878a4-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="878a4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-125">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-126">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="878a4-126">A textual description of the object.</span></span>

<span data-ttu-id="878a4-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="878a4-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="878a4-128">**DriverEnabled**</span><span class="sxs-lookup"><span data-stu-id="878a4-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="878a4-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-131">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-132">指出此載入順序群組是否可包含驅動程式和系統服務。</span><span class="sxs-lookup"><span data-stu-id="878a4-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="878a4-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="878a4-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="878a4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-137">將此服務群組載入作業系統上的順序。</span><span class="sxs-lookup"><span data-stu-id="878a4-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="878a4-138">範例：2</span><span class="sxs-lookup"><span data-stu-id="878a4-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="878a4-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="878a4-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="878a4-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-142">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="878a4-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-143">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="878a4-143">Indicates when the object was installed.</span></span> <span data-ttu-id="878a4-144">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="878a4-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="878a4-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="878a4-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="878a4-146">**名稱**</span><span class="sxs-lookup"><span data-stu-id="878a4-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="878a4-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-149">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-150">載入順序群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="878a4-150">Name of the load order group.</span></span>

<span data-ttu-id="878a4-151">範例：「主要磁片」</span><span class="sxs-lookup"><span data-stu-id="878a4-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="878a4-152">**狀態**</span><span class="sxs-lookup"><span data-stu-id="878a4-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="878a4-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="878a4-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="878a4-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="878a4-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="878a4-155">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="878a4-156">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="878a4-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="878a4-157">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="878a4-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="878a4-158">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="878a4-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="878a4-159">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="878a4-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="878a4-160">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="878a4-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="878a4-161">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="878a4-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="878a4-162">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="878a4-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="878a4-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="878a4-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="878a4-164">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="878a4-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="878a4-165">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="878a4-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="878a4-166">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="878a4-167">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="878a4-168">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="878a4-169">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="878a4-170">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="878a4-171">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="878a4-172">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="878a4-173">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="878a4-174">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="878a4-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="878a4-175">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="878a4-176">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="878a4-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="878a4-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="878a4-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="878a4-178">備註</span><span class="sxs-lookup"><span data-stu-id="878a4-178">Remarks</span></span>

<span data-ttu-id="878a4-179">**Win32 \_ LoadOrderGroup** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="878a4-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="878a4-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="878a4-180">Requirements</span></span>



| <span data-ttu-id="878a4-181">需求</span><span class="sxs-lookup"><span data-stu-id="878a4-181">Requirement</span></span> | <span data-ttu-id="878a4-182">值</span><span class="sxs-lookup"><span data-stu-id="878a4-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="878a4-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="878a4-183">Minimum supported client</span></span><br/> | <span data-ttu-id="878a4-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="878a4-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="878a4-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="878a4-185">Minimum supported server</span></span><br/> | <span data-ttu-id="878a4-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="878a4-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="878a4-187">命名空間</span><span class="sxs-lookup"><span data-stu-id="878a4-187">Namespace</span></span><br/>                | <span data-ttu-id="878a4-188">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="878a4-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="878a4-189">MOF</span><span class="sxs-lookup"><span data-stu-id="878a4-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="878a4-190"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="878a4-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="878a4-191">DLL</span><span class="sxs-lookup"><span data-stu-id="878a4-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="878a4-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="878a4-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="878a4-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="878a4-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878a4-194">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="878a4-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="878a4-195">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="878a4-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

