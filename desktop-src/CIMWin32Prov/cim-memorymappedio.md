---
description: CIM \_ MemoryMappedIO 類別代表電腦架構記憶體對應 i/o。 此類別會解決記憶體和埠 i/o 資源。
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: CIM_MemoryMappedIO 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025962"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="c83ee-104">CIM \_ MemoryMappedIO 類別</span><span class="sxs-lookup"><span data-stu-id="c83ee-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="c83ee-105">**CIM \_ MemoryMappedIO** 類別代表電腦架構記憶體對應 i/o。</span><span class="sxs-lookup"><span data-stu-id="c83ee-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="c83ee-106">此類別會解決記憶體和埠 i/o 資源。</span><span class="sxs-lookup"><span data-stu-id="c83ee-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c83ee-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c83ee-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c83ee-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c83ee-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c83ee-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c83ee-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c83ee-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83ee-111">語法</span><span class="sxs-lookup"><span data-stu-id="c83ee-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="c83ee-112">成員</span><span class="sxs-lookup"><span data-stu-id="c83ee-112">Members</span></span>

<span data-ttu-id="c83ee-113">**CIM \_ MemoryMappedIO** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c83ee-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="c83ee-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c83ee-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c83ee-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c83ee-115">Properties</span></span>

<span data-ttu-id="c83ee-116">**CIM \_ MemoryMappedIO** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c83ee-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c83ee-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="c83ee-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="c83ee-121">A short textual description of the object.</span></span>

<span data-ttu-id="c83ee-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c83ee-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-126">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c83ee-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="c83ee-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c83ee-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c83ee-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c83ee-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-132">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="c83ee-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-133">設定電腦系統之 **CreationClassName** 屬性的範圍。</span><span class="sxs-lookup"><span data-stu-id="c83ee-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c83ee-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-137">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c83ee-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-138">設定電腦系統的 **名稱** 屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="c83ee-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="c83ee-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-142">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-143">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c83ee-143">A textual description of the object.</span></span>

<span data-ttu-id="c83ee-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-145">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="c83ee-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-146">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c83ee-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體對應 i/o 001.2」 \| ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-149">記憶體對應 i/o 的結束位址。</span><span class="sxs-lookup"><span data-stu-id="c83ee-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="c83ee-150">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c83ee-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-152">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c83ee-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-154">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c83ee-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-155">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="c83ee-155">Indicates when the object was installed.</span></span> <span data-ttu-id="c83ee-156">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="c83ee-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c83ee-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c83ee-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-161">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-162">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c83ee-162">Label by which the object is known.</span></span> <span data-ttu-id="c83ee-163">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c83ee-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c83ee-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="c83ee-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-166">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c83ee-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-168">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體對應 i/o 001.1」 \| ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-169">記憶體對應 i/o 的起始位址。</span><span class="sxs-lookup"><span data-stu-id="c83ee-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="c83ee-170">[硬體資源識別碼] 屬性應該設定為此值，以建立對應的 i/o 資源金鑰。</span><span class="sxs-lookup"><span data-stu-id="c83ee-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="c83ee-171">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c83ee-172">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c83ee-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c83ee-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c83ee-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c83ee-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c83ee-175">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c83ee-176">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="c83ee-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="c83ee-177">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="c83ee-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c83ee-178">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="c83ee-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c83ee-179">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="c83ee-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c83ee-180">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c83ee-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c83ee-181">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="c83ee-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c83ee-182">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c83ee-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c83ee-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c83ee-184">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c83ee-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c83ee-185">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c83ee-186">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c83ee-187">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c83ee-188">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c83ee-189">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c83ee-190">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c83ee-191">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c83ee-192">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c83ee-193">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c83ee-194">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c83ee-195">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c83ee-196">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c83ee-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c83ee-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c83ee-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c83ee-198">備註</span><span class="sxs-lookup"><span data-stu-id="c83ee-198">Remarks</span></span>

<span data-ttu-id="c83ee-199">**Cim \_ MemoryMappedIO** 類別衍生自 [**cim \_ SystemResource**](cim-systemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="c83ee-200">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c83ee-200">WMI does not implement this class.</span></span> <span data-ttu-id="c83ee-201">針對衍生自 **CIM \_ MemoryMappedIO** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="c83ee-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c83ee-202">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c83ee-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c83ee-203">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c83ee-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83ee-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="c83ee-204">Requirements</span></span>



| <span data-ttu-id="c83ee-205">需求</span><span class="sxs-lookup"><span data-stu-id="c83ee-205">Requirement</span></span> | <span data-ttu-id="c83ee-206">值</span><span class="sxs-lookup"><span data-stu-id="c83ee-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c83ee-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c83ee-207">Minimum supported client</span></span><br/> | <span data-ttu-id="c83ee-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c83ee-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c83ee-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c83ee-209">Minimum supported server</span></span><br/> | <span data-ttu-id="c83ee-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c83ee-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c83ee-211">命名空間</span><span class="sxs-lookup"><span data-stu-id="c83ee-211">Namespace</span></span><br/>                | <span data-ttu-id="c83ee-212">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c83ee-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c83ee-213">MOF</span><span class="sxs-lookup"><span data-stu-id="c83ee-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c83ee-214"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c83ee-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c83ee-215">DLL</span><span class="sxs-lookup"><span data-stu-id="c83ee-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83ee-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c83ee-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c83ee-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c83ee-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83ee-218">**CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="c83ee-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

