---
description: 代表每次 Msvm \_ ResourcePool 或 Msvm LogicalDisk 類別的 OperationalStatus 屬性變更時引發的事件 \_ 。
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Msvm_StorageAlert 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027036"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="f1ada-103">Msvm \_ StorageAlert 類別</span><span class="sxs-lookup"><span data-stu-id="f1ada-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="f1ada-104">代表每次 [**Msvm \_ ResourcePool**](msvm-resourcepool.md)或 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)類別的 **OperationalStatus** 屬性變更時引發的事件。</span><span class="sxs-lookup"><span data-stu-id="f1ada-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="f1ada-105">下列語法已從 MOF 程式碼簡化，並包含這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1ada-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ada-106">語法</span><span class="sxs-lookup"><span data-stu-id="f1ada-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="f1ada-107">成員</span><span class="sxs-lookup"><span data-stu-id="f1ada-107">Members</span></span>

<span data-ttu-id="f1ada-108">**Msvm \_ StorageAlert** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f1ada-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="f1ada-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f1ada-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1ada-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f1ada-110">Properties</span></span>

<span data-ttu-id="f1ada-111">**Msvm \_ StorageAlert** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f1ada-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1ada-112">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="f1ada-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1ada-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-115">限定詞： **ModelCorrespondence** ( "cim \_ AlertIndication. AlertingManagedElement"，"Cim \_ AlertIndication. OtherAlertingElementFormat" ) </span><span class="sxs-lookup"><span data-stu-id="f1ada-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-116">指定 **AlertingManagedElement** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="f1ada-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="f1ada-117">格式為 CIMObjectPath，格式為 *<NamespacePath> ： <ClassName> . <Prop1> = \\ " <Value1> \\ "，" <Prop2> = \\ " <Value2> \\*"，這會在 CIM 架構中指定實例。</span><span class="sxs-lookup"><span data-stu-id="f1ada-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="f1ada-118">這個屬性繼承自 **CIM \_ AlertIndication** 類別。</span><span class="sxs-lookup"><span data-stu-id="f1ada-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="f1ada-119">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="f1ada-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="f1ada-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f1ada-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f1ada-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) </span><span class="sxs-lookup"><span data-stu-id="f1ada-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1ada-123">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f1ada-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-124">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1ada-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-126">產生警示之實例的 WMI 路徑。</span><span class="sxs-lookup"><span data-stu-id="f1ada-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="f1ada-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1ada-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-130">指定警示的主要分類。</span><span class="sxs-lookup"><span data-stu-id="f1ada-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="f1ada-131">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="f1ada-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="f1ada-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**服務品質警示** (3) </span><span class="sxs-lookup"><span data-stu-id="f1ada-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1ada-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="f1ada-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-134">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f1ada-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-136">偵測到基礎事件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f1ada-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-137">**訊息**</span><span class="sxs-lookup"><span data-stu-id="f1ada-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1ada-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-140">藉由將 **MessageArguments** 屬性中所指定之部分或全部動態元素與 **OwningEntity** 屬性相關聯的其他目錄中的 **MessageID** 屬性唯一識別的靜態元素組合在一起所建立的格式化訊息。</span><span class="sxs-lookup"><span data-stu-id="f1ada-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-141">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="f1ada-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-142">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f1ada-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-144">陣列，其中包含訊息的動態內容。</span><span class="sxs-lookup"><span data-stu-id="f1ada-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="f1ada-145">如果 **MessageID** 的值為32930，則位置為0的引數就是產生警示之 [**Msvm \_ ResourcePool**](msvm-resourcepoolcomponent.md)實例的 **PoolID** 。</span><span class="sxs-lookup"><span data-stu-id="f1ada-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-146">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="f1ada-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1ada-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-149">在 **OwningEntity** 屬性的範圍內唯一識別 **訊息** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="f1ada-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="f1ada-150">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="f1ada-150">The possible values for this property are:</span></span>

<span data-ttu-id="f1ada-151">32930 ( 「儲存集區 QoS 不足的輸送量訊息」 ) </span><span class="sxs-lookup"><span data-stu-id="f1ada-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-152">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="f1ada-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1ada-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-155">為 **AlertingManagedElement** 定義「其他」值的字串。</span><span class="sxs-lookup"><span data-stu-id="f1ada-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="f1ada-156">當 **AlertingManagedElement** 設定為 1 ( "Other" ) 的值時，此值必須設定為非 Null 值。</span><span class="sxs-lookup"><span data-stu-id="f1ada-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="f1ada-157">對於 **AlertingManagedElement** 的所有其他值，此字串的值必須設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="f1ada-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="f1ada-158">這個屬性繼承自 **CIM \_ AlertIndication** 類別。</span><span class="sxs-lookup"><span data-stu-id="f1ada-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-159">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="f1ada-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1ada-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-162">唯一識別擁有此實例中所描述之 **訊息** 格式定義的實體。</span><span class="sxs-lookup"><span data-stu-id="f1ada-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="f1ada-163">這個屬性的值一律是 "Microsoft-Windows-Hyper-v"。</span><span class="sxs-lookup"><span data-stu-id="f1ada-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="f1ada-164">"Microsoft-Windows-Hyper-v"</span><span class="sxs-lookup"><span data-stu-id="f1ada-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="f1ada-165">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="f1ada-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1ada-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-168">描述警示指示的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="f1ada-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="f1ada-169">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="f1ada-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="f1ada-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) </span><span class="sxs-lookup"><span data-stu-id="f1ada-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) </span><span class="sxs-lookup"><span data-stu-id="f1ada-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1ada-172">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="f1ada-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f1ada-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-175">描述導致警示表示之情況的可能原因。</span><span class="sxs-lookup"><span data-stu-id="f1ada-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="f1ada-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**儲存體容量問題** (50) </span><span class="sxs-lookup"><span data-stu-id="f1ada-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**先前的警示已清除** (59) </span><span class="sxs-lookup"><span data-stu-id="f1ada-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f1ada-178">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="f1ada-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1ada-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f1ada-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1ada-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f1ada-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1ada-181">對應于 **ProbableCause** 屬性值的文字描述。</span><span class="sxs-lookup"><span data-stu-id="f1ada-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1ada-182">備註</span><span class="sxs-lookup"><span data-stu-id="f1ada-182">Remarks</span></span>

<span data-ttu-id="f1ada-183">Hyper-v WMI 提供者不會引發個別虛擬磁片的事件，以避免在基礎儲存系統發生大規模故障時，對用戶端發出事件。</span><span class="sxs-lookup"><span data-stu-id="f1ada-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="f1ada-184">當用戶端收到 **Msvm \_ StorageAlert** 事件時，如果 **ProbableCause** 屬性的值為 50 ( 儲存體容量問題 ) ，用戶端就可以使用下列其中一個程式，來探索哪些虛擬磁片在其 QoS 原則之外運作：</span><span class="sxs-lookup"><span data-stu-id="f1ada-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="f1ada-185">查詢從產生事件的資源集區配置的所有 [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="f1ada-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="f1ada-186">這些 **Msvm \_ LogicalDisk** 實例會透過 [**Msvm \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) 關聯與資源集區相關聯。</span><span class="sxs-lookup"><span data-stu-id="f1ada-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="f1ada-187">選取 [OperationalStatus] 包含 [輸送量不足] 的實例，以篩選結果清單。</span><span class="sxs-lookup"><span data-stu-id="f1ada-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ada-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1ada-188">Requirements</span></span>



| <span data-ttu-id="f1ada-189">需求</span><span class="sxs-lookup"><span data-stu-id="f1ada-189">Requirement</span></span> | <span data-ttu-id="f1ada-190">值</span><span class="sxs-lookup"><span data-stu-id="f1ada-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ada-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1ada-191">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ada-192">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1ada-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f1ada-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1ada-193">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ada-194">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1ada-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f1ada-195">命名空間</span><span class="sxs-lookup"><span data-stu-id="f1ada-195">Namespace</span></span><br/>                | <span data-ttu-id="f1ada-196">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f1ada-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1ada-197">MOF</span><span class="sxs-lookup"><span data-stu-id="f1ada-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1ada-198"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f1ada-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1ada-199">DLL</span><span class="sxs-lookup"><span data-stu-id="f1ada-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1ada-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1ada-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1ada-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1ada-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ada-202">**CIM \_ AlertIndication**</span><span class="sxs-lookup"><span data-stu-id="f1ada-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="f1ada-203">**Msvm \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="f1ada-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="f1ada-204">**Msvm \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="f1ada-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




