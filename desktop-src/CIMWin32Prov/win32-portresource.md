---
description: Win32 \_ PORTRESOURCE WMI 類別代表執行 Windows 的電腦系統上的 i/o 埠。
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Win32_PortResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936135"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="18dfe-103">Win32 \_ PortResource 類別</span><span class="sxs-lookup"><span data-stu-id="18dfe-103">Win32\_PortResource class</span></span>

<span data-ttu-id="18dfe-104">**Win32 \_ PortResource** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的 i/o 埠。</span><span class="sxs-lookup"><span data-stu-id="18dfe-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="18dfe-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18dfe-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="18dfe-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="18dfe-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18dfe-107">語法</span><span class="sxs-lookup"><span data-stu-id="18dfe-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="18dfe-108">成員</span><span class="sxs-lookup"><span data-stu-id="18dfe-108">Members</span></span>

<span data-ttu-id="18dfe-109">**Win32 \_ PortResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18dfe-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="18dfe-110">屬性</span><span class="sxs-lookup"><span data-stu-id="18dfe-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18dfe-111">屬性</span><span class="sxs-lookup"><span data-stu-id="18dfe-111">Properties</span></span>

<span data-ttu-id="18dfe-112">**Win32 \_ PortResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18dfe-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18dfe-113">**別名**</span><span class="sxs-lookup"><span data-stu-id="18dfe-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-114">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18dfe-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 設定管理員結構 \| IO \_ 資訊" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-117">若 **為 TRUE**，表示這個實例代表其中一個具有別名的範圍。</span><span class="sxs-lookup"><span data-stu-id="18dfe-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="18dfe-118">如果 **為 FALSE**，則表示實例代表基底埠位址。</span><span class="sxs-lookup"><span data-stu-id="18dfe-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="18dfe-119">基底位址是專用於特定服務或裝置的預先決定通訊埠位址。</span><span class="sxs-lookup"><span data-stu-id="18dfe-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="18dfe-120">埠別名位址是裝置回應的位址，就像是 i/o 埠的實際位址一樣。</span><span class="sxs-lookup"><span data-stu-id="18dfe-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="18dfe-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-124">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-125">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="18dfe-125">Short description of the object.</span></span>

<span data-ttu-id="18dfe-126">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18dfe-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-130">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18dfe-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-131">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="18dfe-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="18dfe-132">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="18dfe-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="18dfe-133">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18dfe-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-137">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="18dfe-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-138">範圍電腦系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="18dfe-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="18dfe-139">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="18dfe-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-143">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") ， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18dfe-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-144">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="18dfe-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="18dfe-145">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="18dfe-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-149">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-150">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="18dfe-150">Description of the object.</span></span>

<span data-ttu-id="18dfe-151">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-152">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="18dfe-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-153">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="18dfe-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-155">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體對應 i/o 001.2」 \| ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-156">記憶體對應 i/o 的結束位址。</span><span class="sxs-lookup"><span data-stu-id="18dfe-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="18dfe-157">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="18dfe-158">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18dfe-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-160">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18dfe-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-162">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="18dfe-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-163">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="18dfe-163">Date and time the object was installed.</span></span> <span data-ttu-id="18dfe-164">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="18dfe-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="18dfe-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-166">**名稱**</span><span class="sxs-lookup"><span data-stu-id="18dfe-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-169">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-170">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="18dfe-170">Label by which the object is known.</span></span> <span data-ttu-id="18dfe-171">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="18dfe-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="18dfe-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-173">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="18dfe-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-174">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="18dfe-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-176">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "StartingAddress" ) ， [**Key**](../wmisdk/key-qualifier.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體對應 i/o 001.1」 \| ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-177">記憶體對應 i/o 的起始位址。</span><span class="sxs-lookup"><span data-stu-id="18dfe-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="18dfe-178">[硬體資源識別碼] 屬性應該設定為此值，以建立對應的 i/o 資源金鑰。</span><span class="sxs-lookup"><span data-stu-id="18dfe-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="18dfe-179">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="18dfe-180">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="18dfe-181">**狀態**</span><span class="sxs-lookup"><span data-stu-id="18dfe-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18dfe-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18dfe-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18dfe-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18dfe-184">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="18dfe-185">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18dfe-185">Current status of the object.</span></span> <span data-ttu-id="18dfe-186">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="18dfe-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="18dfe-187">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="18dfe-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="18dfe-188">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="18dfe-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="18dfe-189">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="18dfe-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="18dfe-190">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="18dfe-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="18dfe-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="18dfe-192">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="18dfe-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="18dfe-193">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="18dfe-194">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="18dfe-195">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18dfe-196">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="18dfe-197">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="18dfe-198">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="18dfe-199">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="18dfe-200">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="18dfe-201">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="18dfe-202">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="18dfe-203">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="18dfe-204">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="18dfe-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="18dfe-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="18dfe-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="18dfe-206">備註</span><span class="sxs-lookup"><span data-stu-id="18dfe-206">Remarks</span></span>

<span data-ttu-id="18dfe-207">**Win32 \_ PortResource** 類別衍生自 [**win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18dfe-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="18dfe-208">Requirements</span></span>



| <span data-ttu-id="18dfe-209">需求</span><span class="sxs-lookup"><span data-stu-id="18dfe-209">Requirement</span></span> | <span data-ttu-id="18dfe-210">值</span><span class="sxs-lookup"><span data-stu-id="18dfe-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18dfe-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18dfe-211">Minimum supported client</span></span><br/> | <span data-ttu-id="18dfe-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18dfe-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18dfe-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18dfe-213">Minimum supported server</span></span><br/> | <span data-ttu-id="18dfe-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18dfe-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18dfe-215">命名空間</span><span class="sxs-lookup"><span data-stu-id="18dfe-215">Namespace</span></span><br/>                | <span data-ttu-id="18dfe-216">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18dfe-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18dfe-217">MOF</span><span class="sxs-lookup"><span data-stu-id="18dfe-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18dfe-218"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="18dfe-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18dfe-219">DLL</span><span class="sxs-lookup"><span data-stu-id="18dfe-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18dfe-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18dfe-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18dfe-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18dfe-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18dfe-222">**Win32 \_ SystemMemoryResource**</span><span class="sxs-lookup"><span data-stu-id="18dfe-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="18dfe-223">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="18dfe-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
