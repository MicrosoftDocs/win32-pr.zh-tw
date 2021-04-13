---
description: Win32 \_ PageFileUsage&\# 8194;WMI 類別代表用來處理在 Win32 系統上交換虛擬記憶體檔案的檔案。 從這個類別所具現化的物件內所包含的資訊會指定分頁檔的執行時間狀態。
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Win32_PageFileUsage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510685"
---
# <a name="win32_pagefileusage-class"></a><span data-ttu-id="0096d-104">Win32 \_ PageFileUsage 類別</span><span class="sxs-lookup"><span data-stu-id="0096d-104">Win32\_PageFileUsage class</span></span>

<span data-ttu-id="0096d-105">**Win32 \_ PageFileUsage** [WMI 類別](../wmisdk/retrieving-a-class.md)代表用來處理在 Win32 系統上交換虛擬記憶體檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="0096d-105">The **Win32\_PageFileUsage** [WMI class](../wmisdk/retrieving-a-class.md) represents the file used for handling virtual memory file swapping on a Win32 system.</span></span> <span data-ttu-id="0096d-106">從這個類別所具現化的物件內所包含的資訊會指定分頁檔的執行時間狀態。</span><span class="sxs-lookup"><span data-stu-id="0096d-106">Information contained within objects instantiated from this class specify the run-time state of the page file.</span></span>

<span data-ttu-id="0096d-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0096d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0096d-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="0096d-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0096d-109">語法</span><span class="sxs-lookup"><span data-stu-id="0096d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a><span data-ttu-id="0096d-110">成員</span><span class="sxs-lookup"><span data-stu-id="0096d-110">Members</span></span>

<span data-ttu-id="0096d-111">**Win32 \_ PageFileUsage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0096d-111">The **Win32\_PageFileUsage** class has these types of members:</span></span>

-   [<span data-ttu-id="0096d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0096d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0096d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0096d-113">Properties</span></span>

<span data-ttu-id="0096d-114">**Win32 \_ PageFileUsage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0096d-114">The **Win32\_PageFileUsage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0096d-115">**AllocatedBaseSize**</span><span class="sxs-lookup"><span data-stu-id="0096d-115">**AllocatedBaseSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0096d-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-118">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)\|dwTotalPageFile"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-119">配置給此分頁檔使用的實際磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="0096d-119">Actual amount of disk space allocated for use with this page file.</span></span> <span data-ttu-id="0096d-120">此值對應至在系統啟動時設定的 **InitialSize** 和 **MaximumSize** 屬性下， [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)中所建立的範圍。</span><span class="sxs-lookup"><span data-stu-id="0096d-120">This value corresponds to the range established in [**Win32\_PageFileSetting**](win32-pagefilesetting.md) under the **InitialSize** and **MaximumSize** properties, set at system startup.</span></span>

<span data-ttu-id="0096d-121">範例：178</span><span class="sxs-lookup"><span data-stu-id="0096d-121">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="0096d-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="0096d-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0096d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-125">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-126">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0096d-126">A short textual description of the object.</span></span>

<span data-ttu-id="0096d-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0096d-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0096d-128">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="0096d-128">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0096d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-131">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-132">分頁檔案目前所使用的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="0096d-132">Amount of disk space currently used by the page file.</span></span>

</dd> <dt>

<span data-ttu-id="0096d-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="0096d-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0096d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-136">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-136">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-137">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0096d-137">A textual description of the object.</span></span>

<span data-ttu-id="0096d-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0096d-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0096d-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0096d-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0096d-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-142">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0096d-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-143">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0096d-143">Indicates when the object was installed.</span></span> <span data-ttu-id="0096d-144">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0096d-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0096d-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0096d-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0096d-146">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0096d-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0096d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-149">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Name" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-149">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-150">分頁檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0096d-150">Name of the page file.</span></span>

<span data-ttu-id="0096d-151">範例： "C： \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="0096d-151">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="0096d-152">**PeakUsage**</span><span class="sxs-lookup"><span data-stu-id="0096d-152">**PeakUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-153">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0096d-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-155">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-156">最高使用分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="0096d-156">Highest use page file.</span></span>

</dd> <dt>

<span data-ttu-id="0096d-157">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0096d-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0096d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-160">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-160">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-161">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0096d-161">String that indicates the current status of the object.</span></span> <span data-ttu-id="0096d-162">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0096d-162">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0096d-163">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0096d-163">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0096d-164">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0096d-164">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0096d-165">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0096d-165">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0096d-166">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0096d-166">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0096d-167">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0096d-167">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0096d-168">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0096d-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0096d-169">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0096d-169">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0096d-170">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0096d-170">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0096d-171">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-171">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0096d-172">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-172">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0096d-173">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-173">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0096d-174">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-174">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0096d-175">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-175">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0096d-176">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-176">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0096d-177">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-177">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0096d-178">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-178">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0096d-179">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-179">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0096d-180">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-180">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0096d-181">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0096d-181">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0096d-182">**TempPageFile**</span><span class="sxs-lookup"><span data-stu-id="0096d-182">**TempPageFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0096d-183">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0096d-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0096d-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0096d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0096d-185">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| TempPageFile" ) </span><span class="sxs-lookup"><span data-stu-id="0096d-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|TempPageFile")</span></span>
</dt> </dl>

<span data-ttu-id="0096d-186">若 **為 true**，表示已建立暫時的分頁檔案，通常是因為目前的電腦系統上沒有永久的分頁檔。</span><span class="sxs-lookup"><span data-stu-id="0096d-186">If **true**, a temporary page file has been created, usually because there is no permanent page file on the current computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0096d-187">備註</span><span class="sxs-lookup"><span data-stu-id="0096d-187">Remarks</span></span>

<span data-ttu-id="0096d-188">**Win32 \_ PageFileUsage** 類別衍生自 [**CIM \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0096d-188">The **Win32\_PageFileUsage** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0096d-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="0096d-189">Requirements</span></span>



| <span data-ttu-id="0096d-190">需求</span><span class="sxs-lookup"><span data-stu-id="0096d-190">Requirement</span></span> | <span data-ttu-id="0096d-191">值</span><span class="sxs-lookup"><span data-stu-id="0096d-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0096d-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0096d-192">Minimum supported client</span></span><br/> | <span data-ttu-id="0096d-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0096d-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0096d-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0096d-194">Minimum supported server</span></span><br/> | <span data-ttu-id="0096d-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0096d-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0096d-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="0096d-196">Namespace</span></span><br/>                | <span data-ttu-id="0096d-197">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0096d-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0096d-198">MOF</span><span class="sxs-lookup"><span data-stu-id="0096d-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0096d-199"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0096d-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0096d-200">DLL</span><span class="sxs-lookup"><span data-stu-id="0096d-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0096d-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0096d-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0096d-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0096d-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0096d-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="0096d-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="0096d-204">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="0096d-204">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
