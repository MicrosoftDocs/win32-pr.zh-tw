---
description: Win32 \_ IRQResource &\# 160;WMI 類別代表在執行 Windows 的電腦系統上 (IRQ) 號碼的插斷要求行。
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Win32_IRQResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110337"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="a3333-103">Win32 \_ IRQResource 類別</span><span class="sxs-lookup"><span data-stu-id="a3333-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="a3333-104">**Win32 \_ IRQResource**[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在執行 Windows 的電腦系統上 (IRQ) 號碼的插斷要求行。  </span><span class="sxs-lookup"><span data-stu-id="a3333-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="a3333-105">插斷要求是裝置或程式針對時間緊迫事件傳送給 CPU 的信號。</span><span class="sxs-lookup"><span data-stu-id="a3333-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="a3333-106">IRQ 可以是以硬體為基礎或以軟體為基礎。</span><span class="sxs-lookup"><span data-stu-id="a3333-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="a3333-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a3333-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a3333-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a3333-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3333-109">語法</span><span class="sxs-lookup"><span data-stu-id="a3333-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="a3333-110">成員</span><span class="sxs-lookup"><span data-stu-id="a3333-110">Members</span></span>

<span data-ttu-id="a3333-111">**Win32 \_ IRQResource** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a3333-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="a3333-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a3333-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3333-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a3333-113">Properties</span></span>

<span data-ttu-id="a3333-114">**Win32 \_ IRQResource** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a3333-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3333-115">**可用性**</span><span class="sxs-lookup"><span data-stu-id="a3333-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a3333-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-119">IRQ 的可用性。</span><span class="sxs-lookup"><span data-stu-id="a3333-119">Availability of the IRQ.</span></span>

<span data-ttu-id="a3333-120">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a3333-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a3333-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a3333-122">其他</span><span class="sxs-lookup"><span data-stu-id="a3333-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3333-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a3333-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a3333-124">Unknown</span><span class="sxs-lookup"><span data-stu-id="a3333-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3333-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="a3333-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a3333-126">可用</span><span class="sxs-lookup"><span data-stu-id="a3333-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="a3333-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**可用** (3) </span><span class="sxs-lookup"><span data-stu-id="a3333-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a3333-128">使用中或無法使用</span><span class="sxs-lookup"><span data-stu-id="a3333-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="a3333-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**使用中/無法使用** (4) </span><span class="sxs-lookup"><span data-stu-id="a3333-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a3333-130">使用中和可用或可共用</span><span class="sxs-lookup"><span data-stu-id="a3333-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="a3333-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**使用中和可用/可共用** (5) </span><span class="sxs-lookup"><span data-stu-id="a3333-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a3333-132">使用中和可用/可共用</span><span class="sxs-lookup"><span data-stu-id="a3333-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a3333-133">**標題**</span><span class="sxs-lookup"><span data-stu-id="a3333-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-136">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-137">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="a3333-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="a3333-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a3333-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-142">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a3333-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3333-143">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="a3333-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a3333-144">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="a3333-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a3333-145">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-146">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a3333-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-149">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a3333-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3333-150">範圍電腦系統建立類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3333-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="a3333-151">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a3333-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-155">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a3333-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3333-156">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3333-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="a3333-157">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-158">**說明**</span><span class="sxs-lookup"><span data-stu-id="a3333-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-161">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-162">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a3333-162">Textual description of the object.</span></span>

<span data-ttu-id="a3333-163">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-164">**硬體**</span><span class="sxs-lookup"><span data-stu-id="a3333-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-165">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a3333-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-167">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| System 結構 \| 資源 \_ 描述元 \| InterfaceType" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-168">若 **為 TRUE**，則中斷是以硬體或軟體為基礎。</span><span class="sxs-lookup"><span data-stu-id="a3333-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="a3333-169">硬體 IRQ 是從周邊到可程式化中斷控制器的實體纜線 (PIC) 晶片，可透過此晶片通知 CPU 有時間緊迫的事件。</span><span class="sxs-lookup"><span data-stu-id="a3333-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="a3333-170">某些 IRQ 線路會保留給標準裝置，例如鍵盤、磁片磁碟機和系統時鐘。</span><span class="sxs-lookup"><span data-stu-id="a3333-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="a3333-171">軟體插斷可讓應用程式注意處理器。</span><span class="sxs-lookup"><span data-stu-id="a3333-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="a3333-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a3333-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-173">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a3333-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-175">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="a3333-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-176">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a3333-176">Date and time the object was installed.</span></span> <span data-ttu-id="a3333-177">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="a3333-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a3333-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-179">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="a3333-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-180">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a3333-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-182">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.1 ") ， [**金鑰**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a3333-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a3333-183">部分物件的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="a3333-183">Part of the object's key value.</span></span>

<span data-ttu-id="a3333-184">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-185">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a3333-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-188">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-189">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a3333-189">Label by which the object is known.</span></span> <span data-ttu-id="a3333-190">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="a3333-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a3333-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-192">**共用**</span><span class="sxs-lookup"><span data-stu-id="a3333-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-193">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="a3333-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-195">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-196">若 **為 TRUE**，則可以共用 IRQ。</span><span class="sxs-lookup"><span data-stu-id="a3333-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="a3333-197">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3333-198">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a3333-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3333-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-201">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-202">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a3333-202">Current status of the object.</span></span> <span data-ttu-id="a3333-203">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="a3333-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a3333-204">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="a3333-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a3333-205">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="a3333-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a3333-206">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="a3333-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a3333-207">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="a3333-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a3333-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a3333-209">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="a3333-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a3333-210">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="a3333-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a3333-211">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a3333-212">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3333-213">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a3333-214">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a3333-215">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a3333-216">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a3333-217">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a3333-218">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a3333-219">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a3333-220">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a3333-221">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3333-222">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="a3333-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a3333-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-225">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 IRQ 資訊 \| 001.3」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-226">IRQ 觸發層級，指出 (4) 或低 (3) 的硬體信號是否觸發中斷。</span><span class="sxs-lookup"><span data-stu-id="a3333-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="a3333-227">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3333-228">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a3333-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3333-229">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="a3333-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="a3333-230">**主動低** (3) </span><span class="sxs-lookup"><span data-stu-id="a3333-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="a3333-231">**主動 High** (4) </span><span class="sxs-lookup"><span data-stu-id="a3333-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3333-232">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="a3333-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-233">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a3333-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-235">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.3 "，" MIF。DMTF \| 系統資源 IRQ 資訊 \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="a3333-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-236">IRQ 觸發程式類型，指出是否發生邊緣觸發的 (4) 或層級觸發的 (3) 中斷。</span><span class="sxs-lookup"><span data-stu-id="a3333-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="a3333-237">這個屬性繼承自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3333-238">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a3333-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3333-239">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="a3333-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="a3333-240">**層級** (3) </span><span class="sxs-lookup"><span data-stu-id="a3333-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="a3333-241">**Edge** (4) </span><span class="sxs-lookup"><span data-stu-id="a3333-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3333-242">**向量**</span><span class="sxs-lookup"><span data-stu-id="a3333-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3333-243">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a3333-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3333-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3333-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3333-245">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| System 結構 \| [**CM \_ 部分 \_ 資源 \_ 描述**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)項 \| 中斷 \| 等級" ) </span><span class="sxs-lookup"><span data-stu-id="a3333-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="a3333-246">Windows IRQ 資源的向量。</span><span class="sxs-lookup"><span data-stu-id="a3333-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="a3333-247">Vector 包含函式的記憶體位址，該函式會在 CPU 認可中斷要求之後執行。</span><span class="sxs-lookup"><span data-stu-id="a3333-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3333-248">備註</span><span class="sxs-lookup"><span data-stu-id="a3333-248">Remarks</span></span>

<span data-ttu-id="a3333-249">**Win32 \_ IRQResource** 類別衍生自 [**CIM \_ IRQ**](cim-irq.md)。</span><span class="sxs-lookup"><span data-stu-id="a3333-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3333-250">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3333-250">Requirements</span></span>



| <span data-ttu-id="a3333-251">需求</span><span class="sxs-lookup"><span data-stu-id="a3333-251">Requirement</span></span> | <span data-ttu-id="a3333-252">值</span><span class="sxs-lookup"><span data-stu-id="a3333-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3333-253">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3333-253">Minimum supported client</span></span><br/> | <span data-ttu-id="a3333-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3333-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3333-255">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3333-255">Minimum supported server</span></span><br/> | <span data-ttu-id="a3333-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3333-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3333-257">命名空間</span><span class="sxs-lookup"><span data-stu-id="a3333-257">Namespace</span></span><br/>                | <span data-ttu-id="a3333-258">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a3333-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3333-259">MOF</span><span class="sxs-lookup"><span data-stu-id="a3333-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3333-260"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3333-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3333-261">DLL</span><span class="sxs-lookup"><span data-stu-id="a3333-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3333-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3333-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3333-263">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3333-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3333-264">**CIM \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="a3333-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="a3333-265">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="a3333-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

