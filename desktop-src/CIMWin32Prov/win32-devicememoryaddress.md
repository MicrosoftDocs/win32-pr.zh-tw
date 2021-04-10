---
description: Win32 \_ DEVICEMEMORYADDRESS WMI 類別代表執行 Windows 的電腦系統上的裝置記憶體位址。
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Win32_DeviceMemoryAddress 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936421"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="35ba5-103">Win32 \_ DeviceMemoryAddress 類別</span><span class="sxs-lookup"><span data-stu-id="35ba5-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="35ba5-104">**Win32 \_ DeviceMemoryAddress** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 的電腦系統上的裝置記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="35ba5-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="35ba5-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35ba5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="35ba5-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="35ba5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ba5-107">語法</span><span class="sxs-lookup"><span data-stu-id="35ba5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="35ba5-108">成員</span><span class="sxs-lookup"><span data-stu-id="35ba5-108">Members</span></span>

<span data-ttu-id="35ba5-109">**Win32 \_ DeviceMemoryAddress** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35ba5-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="35ba5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="35ba5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35ba5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35ba5-111">Properties</span></span>

<span data-ttu-id="35ba5-112">**Win32 \_ DeviceMemoryAddress** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35ba5-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35ba5-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="35ba5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-116">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-117">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="35ba5-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="35ba5-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35ba5-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35ba5-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-123">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="35ba5-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="35ba5-124">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="35ba5-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="35ba5-125">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35ba5-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-129">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="35ba5-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-130">範圍電腦系統建立類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="35ba5-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="35ba5-131">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="35ba5-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-135">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35ba5-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-136">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="35ba5-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="35ba5-137">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="35ba5-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-141">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-142">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="35ba5-142">Description of the object.</span></span>

<span data-ttu-id="35ba5-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="35ba5-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-145">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="35ba5-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-147">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體對應 i/o 001.2」 \| ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-148">記憶體對應 i/o 的結束位址。</span><span class="sxs-lookup"><span data-stu-id="35ba5-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="35ba5-149">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="35ba5-150">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35ba5-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-152">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="35ba5-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-154">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="35ba5-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-155">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="35ba5-155">Date and time the object was installed.</span></span> <span data-ttu-id="35ba5-156">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="35ba5-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="35ba5-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-158">**MemoryType**</span><span class="sxs-lookup"><span data-stu-id="35ba5-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-161">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| SystemStructures \| CM \_ 部分 \_ 資源 \_ 描述元 \| 旗標" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-162">執行 Windows 之電腦系統上的記憶體資源特性。</span><span class="sxs-lookup"><span data-stu-id="35ba5-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="35ba5-163">值如下所示。</span><span class="sxs-lookup"><span data-stu-id="35ba5-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="35ba5-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**Readwrite** ( "readwrite" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-165">記憶體可以是讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="35ba5-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="35ba5-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**Readonly** ( "readonly" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-167">記憶體是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="35ba5-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="35ba5-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**Writeonly** ( "writeonly" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-169">只能寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="35ba5-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="35ba5-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ( "Prefetchable" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-171">記憶體區塊會從主儲存體複製到記憶體晶片所管理的小型緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35ba5-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="35ba5-172">具有 prefetchable 記憶體的相同記憶體部分的重複讀取作業會更快速。</span><span class="sxs-lookup"><span data-stu-id="35ba5-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="35ba5-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ( "CombinedWrite" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-174">TBD</span><span class="sxs-lookup"><span data-stu-id="35ba5-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="35ba5-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ( "Type24" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-176">TBD</span><span class="sxs-lookup"><span data-stu-id="35ba5-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="35ba5-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>可快取 **的 ( 「** 可快取」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-178">TBD</span><span class="sxs-lookup"><span data-stu-id="35ba5-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="35ba5-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ( "WindowDecode" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-180">TBD</span><span class="sxs-lookup"><span data-stu-id="35ba5-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="35ba5-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**橫條** ( "bar" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="35ba5-182">TBD</span><span class="sxs-lookup"><span data-stu-id="35ba5-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="35ba5-183">**名稱**</span><span class="sxs-lookup"><span data-stu-id="35ba5-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-186">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-187">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="35ba5-187">Label by which the object is known.</span></span> <span data-ttu-id="35ba5-188">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="35ba5-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="35ba5-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-190">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="35ba5-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-191">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="35ba5-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-193">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "StartingAddress" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體對應 i/o 001.1」 \| ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-194">記憶體對應 i/o 的起始位址。</span><span class="sxs-lookup"><span data-stu-id="35ba5-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="35ba5-195">[硬體資源識別碼] 屬性應該設定為此值，以建立對應的 i/o 資源金鑰。</span><span class="sxs-lookup"><span data-stu-id="35ba5-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="35ba5-196">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="35ba5-197">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="35ba5-198">**狀態**</span><span class="sxs-lookup"><span data-stu-id="35ba5-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ba5-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35ba5-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35ba5-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ba5-201">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="35ba5-202">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="35ba5-202">Current status of the object.</span></span> <span data-ttu-id="35ba5-203">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="35ba5-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="35ba5-204">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="35ba5-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="35ba5-205">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="35ba5-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35ba5-206">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="35ba5-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35ba5-207">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="35ba5-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35ba5-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="35ba5-209">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="35ba5-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="35ba5-210">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="35ba5-211">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="35ba5-212">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35ba5-213">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="35ba5-214">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="35ba5-215">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="35ba5-216">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="35ba5-217">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="35ba5-218">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="35ba5-219">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="35ba5-220">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="35ba5-221">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="35ba5-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="35ba5-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="35ba5-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="35ba5-223">備註</span><span class="sxs-lookup"><span data-stu-id="35ba5-223">Remarks</span></span>

<span data-ttu-id="35ba5-224">**Win32 \_ DeviceMemoryAddress** 類別衍生自 [**win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)。</span><span class="sxs-lookup"><span data-stu-id="35ba5-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35ba5-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="35ba5-225">Requirements</span></span>



| <span data-ttu-id="35ba5-226">需求</span><span class="sxs-lookup"><span data-stu-id="35ba5-226">Requirement</span></span> | <span data-ttu-id="35ba5-227">值</span><span class="sxs-lookup"><span data-stu-id="35ba5-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35ba5-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35ba5-228">Minimum supported client</span></span><br/> | <span data-ttu-id="35ba5-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35ba5-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35ba5-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35ba5-230">Minimum supported server</span></span><br/> | <span data-ttu-id="35ba5-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35ba5-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35ba5-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="35ba5-232">Namespace</span></span><br/>                | <span data-ttu-id="35ba5-233">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="35ba5-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35ba5-234">MOF</span><span class="sxs-lookup"><span data-stu-id="35ba5-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35ba5-235"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="35ba5-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35ba5-236">DLL</span><span class="sxs-lookup"><span data-stu-id="35ba5-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ba5-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ba5-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ba5-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35ba5-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ba5-239">**Win32 \_ SystemMemoryResource**</span><span class="sxs-lookup"><span data-stu-id="35ba5-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="35ba5-240">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="35ba5-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

