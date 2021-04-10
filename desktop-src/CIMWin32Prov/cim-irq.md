---
description: CIM \_ IRQ 類別代表 Intel 架構中斷要求線路 (IRQ) 。
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: CIM_IRQ 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847355"
---
# <a name="cim_irq-class"></a><span data-ttu-id="9aae5-103">CIM \_ IRQ 類別</span><span class="sxs-lookup"><span data-stu-id="9aae5-103">CIM\_IRQ class</span></span>

<span data-ttu-id="9aae5-104">**CIM \_ IRQ** 類別代表 Intel 架構中斷要求線路 (IRQ) 。</span><span class="sxs-lookup"><span data-stu-id="9aae5-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9aae5-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9aae5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9aae5-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9aae5-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9aae5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9aae5-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="9aae5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aae5-109">語法</span><span class="sxs-lookup"><span data-stu-id="9aae5-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="9aae5-110">成員</span><span class="sxs-lookup"><span data-stu-id="9aae5-110">Members</span></span>

<span data-ttu-id="9aae5-111">**CIM \_ IRQ** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9aae5-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="9aae5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9aae5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9aae5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9aae5-113">Properties</span></span>

<span data-ttu-id="9aae5-114">**CIM \_ IRQ** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9aae5-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9aae5-115">**可用性**</span><span class="sxs-lookup"><span data-stu-id="9aae5-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9aae5-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-119">IRQ 的可用性。</span><span class="sxs-lookup"><span data-stu-id="9aae5-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9aae5-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9aae5-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9aae5-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9aae5-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="9aae5-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**可用** (3) </span><span class="sxs-lookup"><span data-stu-id="9aae5-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="9aae5-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**使用中/無法使用** (4) </span><span class="sxs-lookup"><span data-stu-id="9aae5-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="9aae5-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**使用中和可用/可共用** (5) </span><span class="sxs-lookup"><span data-stu-id="9aae5-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9aae5-125">使用中和可用/可共用</span><span class="sxs-lookup"><span data-stu-id="9aae5-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9aae5-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="9aae5-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-130">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="9aae5-130">A short textual description of the object.</span></span>

<span data-ttu-id="9aae5-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9aae5-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-135">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9aae5-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-136">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aae5-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9aae5-137">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9aae5-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9aae5-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-141">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9aae5-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-142">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="9aae5-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9aae5-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-146">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="9aae5-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-147">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="9aae5-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-148">**說明**</span><span class="sxs-lookup"><span data-stu-id="9aae5-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-151">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-152">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="9aae5-152">A textual description of the object.</span></span>

<span data-ttu-id="9aae5-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9aae5-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-155">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9aae5-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-157">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="9aae5-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-158">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="9aae5-158">Indicates when the object was installed.</span></span> <span data-ttu-id="9aae5-159">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="9aae5-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9aae5-160">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-161">**IRQNumber**</span><span class="sxs-lookup"><span data-stu-id="9aae5-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9aae5-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.1 ") ， [**金鑰**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9aae5-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-165">物件的金鑰值的一部分，也就是 IRQ 號碼。</span><span class="sxs-lookup"><span data-stu-id="9aae5-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-166">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9aae5-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-169">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-170">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="9aae5-170">Label by which the object is known.</span></span> <span data-ttu-id="9aae5-171">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9aae5-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9aae5-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-173">**共用**</span><span class="sxs-lookup"><span data-stu-id="9aae5-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9aae5-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-176">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.4」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-177">若 **為 TRUE**，則可以共用 IRQ。</span><span class="sxs-lookup"><span data-stu-id="9aae5-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="9aae5-178">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9aae5-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9aae5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-181">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-182">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="9aae5-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="9aae5-183">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="9aae5-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9aae5-184">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="9aae5-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9aae5-185">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="9aae5-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9aae5-186">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="9aae5-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9aae5-187">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="9aae5-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9aae5-188">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="9aae5-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9aae5-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9aae5-190">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="9aae5-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9aae5-191">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9aae5-192">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9aae5-193">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9aae5-194">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9aae5-195">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9aae5-196">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9aae5-197">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9aae5-198">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9aae5-199">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9aae5-200">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9aae5-201">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9aae5-202">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9aae5-203">**TriggerLevel**</span><span class="sxs-lookup"><span data-stu-id="9aae5-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-204">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9aae5-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-206">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源 IRQ 資訊 \| 001.3」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-207">指出中斷是否由硬體信號（高或低）觸發。</span><span class="sxs-lookup"><span data-stu-id="9aae5-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9aae5-208">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9aae5-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9aae5-209">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9aae5-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="9aae5-210">**主動低** (3) </span><span class="sxs-lookup"><span data-stu-id="9aae5-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="9aae5-211">**主動 High** (4) </span><span class="sxs-lookup"><span data-stu-id="9aae5-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9aae5-212">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="9aae5-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9aae5-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9aae5-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9aae5-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9aae5-215">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| IRQ \| 001.3 "，" MIF。DMTF \| 系統資源 IRQ 資訊 \| 001.2」 ) </span><span class="sxs-lookup"><span data-stu-id="9aae5-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9aae5-216">可能發生的中斷類型。</span><span class="sxs-lookup"><span data-stu-id="9aae5-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9aae5-217">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9aae5-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9aae5-218">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="9aae5-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="9aae5-219">**層級** (3) </span><span class="sxs-lookup"><span data-stu-id="9aae5-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="9aae5-220">**Edge** (4) </span><span class="sxs-lookup"><span data-stu-id="9aae5-220">**Edge** (4)</span></span>


<span data-ttu-id="9aae5-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9aae5-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="9aae5-222">備註</span><span class="sxs-lookup"><span data-stu-id="9aae5-222">Remarks</span></span>

<span data-ttu-id="9aae5-223">**Cim \_ IRQ** 類別衍生自 [**cim \_ SystemResource**](cim-systemresource.md)。WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="9aae5-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="9aae5-224">請參閱衍生自 **CIM \_ IRQ** 之類別的 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9aae5-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="9aae5-225">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9aae5-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9aae5-226">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9aae5-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aae5-227">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aae5-227">Requirements</span></span>



| <span data-ttu-id="9aae5-228">需求</span><span class="sxs-lookup"><span data-stu-id="9aae5-228">Requirement</span></span> | <span data-ttu-id="9aae5-229">值</span><span class="sxs-lookup"><span data-stu-id="9aae5-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aae5-230">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aae5-230">Minimum supported client</span></span><br/> | <span data-ttu-id="9aae5-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aae5-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9aae5-232">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aae5-232">Minimum supported server</span></span><br/> | <span data-ttu-id="9aae5-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aae5-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9aae5-234">命名空間</span><span class="sxs-lookup"><span data-stu-id="9aae5-234">Namespace</span></span><br/>                | <span data-ttu-id="9aae5-235">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9aae5-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9aae5-236">MOF</span><span class="sxs-lookup"><span data-stu-id="9aae5-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aae5-237"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9aae5-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9aae5-238">DLL</span><span class="sxs-lookup"><span data-stu-id="9aae5-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aae5-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aae5-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aae5-240">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aae5-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aae5-241">**CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="9aae5-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

