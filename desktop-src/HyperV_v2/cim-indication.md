---
description: '\_對於架構物件中的變更、架構物件資料、提供者和檢測所偵測到的事件，CIM 表示是所有相關通知的抽象基類。 CIM 指示的子類別 \_ 代表特定類型的通知。'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982386"
---
# <a name="cim_indication-class"></a><span data-ttu-id="058df-104">CIM \_ 指示類別</span><span class="sxs-lookup"><span data-stu-id="058df-104">CIM\_Indication class</span></span>

<span data-ttu-id="058df-105">**CIM \_** 針對架構物件中的變更、架構物件資料、提供者和檢測所偵測到的事件，其指示是所有通知的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="058df-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="058df-106">**CIM \_ 指示** 的子類別代表特定類型的通知。</span><span class="sxs-lookup"><span data-stu-id="058df-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="058df-107">語法</span><span class="sxs-lookup"><span data-stu-id="058df-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="058df-108">成員</span><span class="sxs-lookup"><span data-stu-id="058df-108">Members</span></span>

<span data-ttu-id="058df-109">**CIM \_ 指示** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="058df-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="058df-110">屬性</span><span class="sxs-lookup"><span data-stu-id="058df-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="058df-111">屬性</span><span class="sxs-lookup"><span data-stu-id="058df-111">Properties</span></span>

<span data-ttu-id="058df-112">**CIM \_ 指示** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="058df-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="058df-113">**CorrelatedIndications**</span><span class="sxs-lookup"><span data-stu-id="058df-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="058df-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="058df-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-116">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。相互關聯的通知 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 表示**。**IndicationIdentifier**") </span><span class="sxs-lookup"><span data-stu-id="058df-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="058df-117">陣列，其中包含與這個相關之通知的 **IndicationIdentifier** 值。</span><span class="sxs-lookup"><span data-stu-id="058df-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="058df-118">**IndicationFilterName**</span><span class="sxs-lookup"><span data-stu-id="058df-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="058df-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="058df-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-121">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ IndicationFilter.Name" ) </span><span class="sxs-lookup"><span data-stu-id="058df-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="058df-122">處理指示之指示篩選準則的識別碼。</span><span class="sxs-lookup"><span data-stu-id="058df-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="058df-123">傳送服務會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="058df-123">The sending service sets this property.</span></span> <span data-ttu-id="058df-124">這個屬性會與 **CIM \_ IndicationFilter** 物件的 **Name** 屬性相互關聯。</span><span class="sxs-lookup"><span data-stu-id="058df-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="058df-125">**IndicationFilterName** 的值應使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="058df-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="058df-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="058df-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="058df-127">*<OrgID>* 必須包含擁有該物件之商務實體所擁有的受著作權、商標或唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="058df-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="058df-128">*<OrgID>* 不得包含冒號 (： ) </span><span class="sxs-lookup"><span data-stu-id="058df-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="058df-129">*<LocalID>* 擁有物件之商務實體所選擇的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="058df-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="058df-130">**IndicationIdentifier**</span><span class="sxs-lookup"><span data-stu-id="058df-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="058df-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="058df-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-133">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。通知識別碼 ") </span><span class="sxs-lookup"><span data-stu-id="058df-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="058df-134">指示的識別碼。</span><span class="sxs-lookup"><span data-stu-id="058df-134">An identifier of the indication.</span></span> <span data-ttu-id="058df-135">這個屬性可用來作為 **CorrelatedIndications** 屬性陣列中的索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="058df-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="058df-136">因此， **IndicationIdentifier** 應該是這個類別實例命名空間內的唯一值。</span><span class="sxs-lookup"><span data-stu-id="058df-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="058df-137">若要確保 **IndicationIdentifier** 是唯一的，應該使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="058df-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="058df-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="058df-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="058df-139">*<OrgID>* 必須包含擁有該物件之商務實體所擁有的受著作權、商標或唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="058df-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="058df-140">*<OrgID>* 不得包含冒號 (： ) </span><span class="sxs-lookup"><span data-stu-id="058df-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="058df-141">*<LocalID>* 擁有物件之商務實體所選擇的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="058df-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="058df-142">針對 DMTF 定義的實例， *<OrgID>* 應該設為 "CIM"。</span><span class="sxs-lookup"><span data-stu-id="058df-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="058df-143">**IndicationTime**</span><span class="sxs-lookup"><span data-stu-id="058df-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-144">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="058df-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="058df-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="058df-146">指示的建立時間和日期。</span><span class="sxs-lookup"><span data-stu-id="058df-146">The time and date when the indication was created.</span></span> <span data-ttu-id="058df-147">如果建立指示的實體無法判斷這項資訊，則屬性可以設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="058df-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="058df-148">**IndicationTime** 值對於快速連續產生的指示而言可能相同。</span><span class="sxs-lookup"><span data-stu-id="058df-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="058df-149">**OtherSeverity**</span><span class="sxs-lookup"><span data-stu-id="058df-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="058df-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="058df-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-152">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**") </span><span class="sxs-lookup"><span data-stu-id="058df-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="058df-153">當 **PerceivedSeverity** 設為 "1" (其他) 時，來自通知者觀點的指示嚴重性。</span><span class="sxs-lookup"><span data-stu-id="058df-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="058df-154">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="058df-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="058df-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="058df-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-157">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="058df-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="058df-158">來自通知者觀點的指示嚴重性。</span><span class="sxs-lookup"><span data-stu-id="058df-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="058df-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="058df-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="058df-160">已知的指示嚴重性不明或不定。</span><span class="sxs-lookup"><span data-stu-id="058df-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="058df-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="058df-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="058df-162">表示可以在 **OtherSeverity** 屬性中找到嚴重性的值。</span><span class="sxs-lookup"><span data-stu-id="058df-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="058df-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) </span><span class="sxs-lookup"><span data-stu-id="058df-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="058df-164">提供資訊性回應時應使用資訊。</span><span class="sxs-lookup"><span data-stu-id="058df-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="058df-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) </span><span class="sxs-lookup"><span data-stu-id="058df-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="058df-166">如果適合讓使用者決定是否需要採取動作，則應該使用。</span><span class="sxs-lookup"><span data-stu-id="058df-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="058df-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) </span><span class="sxs-lookup"><span data-stu-id="058df-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="058df-168">需要採取動作，但這次的情況並不嚴重。</span><span class="sxs-lookup"><span data-stu-id="058df-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="058df-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) </span><span class="sxs-lookup"><span data-stu-id="058df-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="058df-170">現在需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="058df-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="058df-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) </span><span class="sxs-lookup"><span data-stu-id="058df-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="058df-172">現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。</span><span class="sxs-lookup"><span data-stu-id="058df-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="058df-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) </span><span class="sxs-lookup"><span data-stu-id="058df-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="058df-174">發生錯誤，但太晚採取補救動作。</span><span class="sxs-lookup"><span data-stu-id="058df-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="058df-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="058df-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="058df-176">**SequenceCoNtext**</span><span class="sxs-lookup"><span data-stu-id="058df-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="058df-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="058df-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-179">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 指示**」。**SequenceNumber**") </span><span class="sxs-lookup"><span data-stu-id="058df-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="058df-180">指示之序列識別碼的序列內容。</span><span class="sxs-lookup"><span data-stu-id="058df-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="058df-181">如果服務不支援指示的序列識別碼，這個屬性應該設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="058df-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="058df-182">如果重新傳遞指示，這個屬性會維持不變。</span><span class="sxs-lookup"><span data-stu-id="058df-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="058df-183">當服務嘗試 redeliver 指示、重新排列未按順序抵達的指示，以及偵測遺失的指示時，指示的序列識別碼可讓接聽程式識別重複的指示。</span><span class="sxs-lookup"><span data-stu-id="058df-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="058df-184">若要確保 **SequenceCoNtext** 是唯一的，應該使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="058df-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="058df-185">*指示-服務-名稱* \#*cim-服務-開始-識別碼* \#接聽 *程式-目的地建立時間*</span><span class="sxs-lookup"><span data-stu-id="058df-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="058df-186">*指示-服務-名稱* 是可傳遞指示之 **CIM \_ IndicationService** 實例的 **名稱** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="058df-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="058df-187">*cim-服務-開始-* 識別碼是唯一識別服務啟動作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="058df-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="058df-188">例如，這可能是開始時間的時間戳記，或每次啟動或重新開機服務時增加的計數器。</span><span class="sxs-lookup"><span data-stu-id="058df-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="058df-189">接聽 *程式-目的地建立時間* 是 **CIM \_ ListenerDestination** 實例建立時間的時間戳記，代表接聽程式目的地。 nSince 此格式只是建議，CIM 用戶端應將值視為順序內容的不透明識別碼，且不應依賴此格式。</span><span class="sxs-lookup"><span data-stu-id="058df-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="058df-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="058df-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="058df-191">資料類型： **sint64**</span><span class="sxs-lookup"><span data-stu-id="058df-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="058df-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="058df-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="058df-193">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 指示**」。**SequenceCoNtext**") </span><span class="sxs-lookup"><span data-stu-id="058df-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="058df-194">指示之序列識別碼的序號。</span><span class="sxs-lookup"><span data-stu-id="058df-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="058df-195">當服務嘗試 redeliver 指示、重新排列未按順序抵達的指示，以及偵測遺失的指示時，指示的序列識別碼可讓接聽程式識別重複的指示。</span><span class="sxs-lookup"><span data-stu-id="058df-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="058df-196">序號具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="058df-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="058df-197">每當 **SequenceCoNtext** 值變更時，序號就會重設為 "0"。</span><span class="sxs-lookup"><span data-stu-id="058df-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="058df-198">每當接聽程式目的地收到新的指示時，序號就會增加為 "1"。</span><span class="sxs-lookup"><span data-stu-id="058df-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="058df-199">當超過值範圍時，序號會換行為 "0"。</span><span class="sxs-lookup"><span data-stu-id="058df-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="058df-200">如果重新傳遞指示， **SequenceNumber** 會維持不變。</span><span class="sxs-lookup"><span data-stu-id="058df-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="058df-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="058df-201">Requirements</span></span>



| <span data-ttu-id="058df-202">需求</span><span class="sxs-lookup"><span data-stu-id="058df-202">Requirement</span></span> | <span data-ttu-id="058df-203">值</span><span class="sxs-lookup"><span data-stu-id="058df-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058df-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="058df-204">Minimum supported client</span></span><br/> | <span data-ttu-id="058df-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="058df-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="058df-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="058df-206">Minimum supported server</span></span><br/> | <span data-ttu-id="058df-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="058df-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="058df-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="058df-208">Namespace</span></span><br/>                | <span data-ttu-id="058df-209">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="058df-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="058df-210">MOF</span><span class="sxs-lookup"><span data-stu-id="058df-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="058df-211"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="058df-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="058df-212">DLL</span><span class="sxs-lookup"><span data-stu-id="058df-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="058df-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="058df-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="058df-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="058df-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058df-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="058df-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

