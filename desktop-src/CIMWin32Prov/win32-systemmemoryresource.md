---
description: Win32 \_ SystemMemoryResource ABSTRACT WMI 類別代表執行 Windows 的電腦系統上的系統記憶體資源。
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Win32_SystemMemoryResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847563"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="01ba8-103">Win32 \_ SystemMemoryResource 類別</span><span class="sxs-lookup"><span data-stu-id="01ba8-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="01ba8-104">**Win32 \_ SystemMemoryResource** abstract [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的系統記憶體資源。</span><span class="sxs-lookup"><span data-stu-id="01ba8-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="01ba8-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="01ba8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="01ba8-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="01ba8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ba8-107">語法</span><span class="sxs-lookup"><span data-stu-id="01ba8-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="01ba8-108">成員</span><span class="sxs-lookup"><span data-stu-id="01ba8-108">Members</span></span>

<span data-ttu-id="01ba8-109">**Win32 \_ SystemMemoryResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01ba8-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="01ba8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="01ba8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01ba8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="01ba8-111">Properties</span></span>

<span data-ttu-id="01ba8-112">**Win32 \_ SystemMemoryResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="01ba8-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01ba8-113">**標題**</span><span class="sxs-lookup"><span data-stu-id="01ba8-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-116">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-117">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="01ba8-117">A short textual description of the object.</span></span>

<span data-ttu-id="01ba8-118">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="01ba8-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-122">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="01ba8-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-123">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="01ba8-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="01ba8-124">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="01ba8-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="01ba8-125">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="01ba8-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-129">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="01ba8-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-130">設定電腦系統之 **CreationClassName** 屬性的範圍。</span><span class="sxs-lookup"><span data-stu-id="01ba8-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="01ba8-131">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="01ba8-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-135">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") ， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="01ba8-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-136">設定電腦系統的 **名稱** 屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="01ba8-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="01ba8-137">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="01ba8-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-141">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-142">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="01ba8-142">A textual description of the object.</span></span>

<span data-ttu-id="01ba8-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="01ba8-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-145">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="01ba8-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-147">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 記憶體對應 i/o 001.2」 \| ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-148">記憶體對應 i/o 的結束位址。</span><span class="sxs-lookup"><span data-stu-id="01ba8-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="01ba8-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="01ba8-150">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="01ba8-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-152">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="01ba8-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-154">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="01ba8-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-155">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="01ba8-155">Indicates when the object was installed.</span></span> <span data-ttu-id="01ba8-156">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="01ba8-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="01ba8-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="01ba8-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-161">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-162">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="01ba8-162">Label by which the object is known.</span></span> <span data-ttu-id="01ba8-163">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="01ba8-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="01ba8-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="01ba8-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-166">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="01ba8-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-168">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 記憶體對應 i/o 001.1」 \| ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-169">記憶體對應 i/o 的起始位址。</span><span class="sxs-lookup"><span data-stu-id="01ba8-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="01ba8-170">[硬體資源識別碼] 屬性應該設定為此值，以建立對應的 i/o 資源金鑰。</span><span class="sxs-lookup"><span data-stu-id="01ba8-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="01ba8-171">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="01ba8-172">這個屬性繼承自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="01ba8-173">**狀態**</span><span class="sxs-lookup"><span data-stu-id="01ba8-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01ba8-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="01ba8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="01ba8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01ba8-176">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="01ba8-177">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="01ba8-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="01ba8-178">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="01ba8-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="01ba8-179">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="01ba8-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="01ba8-180">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="01ba8-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="01ba8-181">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="01ba8-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="01ba8-182">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="01ba8-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="01ba8-183">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="01ba8-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="01ba8-184">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="01ba8-185">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="01ba8-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="01ba8-186">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="01ba8-187">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="01ba8-188">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01ba8-189">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="01ba8-190">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="01ba8-191">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="01ba8-192">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="01ba8-193">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="01ba8-194">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="01ba8-195">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="01ba8-196">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="01ba8-197">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="01ba8-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="01ba8-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="01ba8-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="01ba8-199">備註</span><span class="sxs-lookup"><span data-stu-id="01ba8-199">Remarks</span></span>

<span data-ttu-id="01ba8-200">**Win32 \_ SystemMemoryResource** 類別衍生自 [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)。</span><span class="sxs-lookup"><span data-stu-id="01ba8-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01ba8-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="01ba8-201">Requirements</span></span>



| <span data-ttu-id="01ba8-202">需求</span><span class="sxs-lookup"><span data-stu-id="01ba8-202">Requirement</span></span> | <span data-ttu-id="01ba8-203">值</span><span class="sxs-lookup"><span data-stu-id="01ba8-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01ba8-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01ba8-204">Minimum supported client</span></span><br/> | <span data-ttu-id="01ba8-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01ba8-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01ba8-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01ba8-206">Minimum supported server</span></span><br/> | <span data-ttu-id="01ba8-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01ba8-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01ba8-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="01ba8-208">Namespace</span></span><br/>                | <span data-ttu-id="01ba8-209">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="01ba8-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01ba8-210">MOF</span><span class="sxs-lookup"><span data-stu-id="01ba8-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01ba8-211"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="01ba8-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01ba8-212">DLL</span><span class="sxs-lookup"><span data-stu-id="01ba8-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ba8-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01ba8-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01ba8-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01ba8-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ba8-215">**CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="01ba8-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="01ba8-216">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="01ba8-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
