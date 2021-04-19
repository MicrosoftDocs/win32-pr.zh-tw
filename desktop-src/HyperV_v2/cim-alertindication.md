---
description: CIM 警示通知的具體超類別。
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970755"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="13eae-103">CIM \_ AlertIndication 類別</span><span class="sxs-lookup"><span data-stu-id="13eae-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="13eae-104">CIM 警示通知的具體超類別。</span><span class="sxs-lookup"><span data-stu-id="13eae-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="13eae-105">**CIM \_AlertIndication** 是 **CIM \_ 指示** 類別的特製化類型，其中包含有關「真實世界」事件的嚴重性、原因、建議動作和其他資料的資訊。</span><span class="sxs-lookup"><span data-stu-id="13eae-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="13eae-106">此事件和其資料可能不會在 CIM 類別階層中建立模型。</span><span class="sxs-lookup"><span data-stu-id="13eae-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="13eae-107">語法</span><span class="sxs-lookup"><span data-stu-id="13eae-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="13eae-108">成員</span><span class="sxs-lookup"><span data-stu-id="13eae-108">Members</span></span>

<span data-ttu-id="13eae-109">**CIM \_ AlertIndication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13eae-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="13eae-110">屬性</span><span class="sxs-lookup"><span data-stu-id="13eae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13eae-111">屬性</span><span class="sxs-lookup"><span data-stu-id="13eae-111">Properties</span></span>

<span data-ttu-id="13eae-112">**CIM \_ AlertIndication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13eae-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13eae-113">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="13eae-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="13eae-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-116">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingManagedElement**"，"**CIM \_ AlertIndication**.**OtherAlertingElementFormat**") </span><span class="sxs-lookup"><span data-stu-id="13eae-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-117">**AlertingManagedElement** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="13eae-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13eae-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="13eae-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-119">CIM 用戶端應用程式可解譯的格式不明或不具意義。</span><span class="sxs-lookup"><span data-stu-id="13eae-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13eae-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="13eae-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-121">格式是由 OtherAlertingElementFormat 屬性的值所定義。</span><span class="sxs-lookup"><span data-stu-id="13eae-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="13eae-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) </span><span class="sxs-lookup"><span data-stu-id="13eae-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-123">格式為 CIMObjectPath，指定 CIM 架構中的實例。</span><span class="sxs-lookup"><span data-stu-id="13eae-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13eae-124">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="13eae-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-127">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingElementFormat**") </span><span class="sxs-lookup"><span data-stu-id="13eae-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-128">實體 (的識別資訊，即產生此指示的實例) 。</span><span class="sxs-lookup"><span data-stu-id="13eae-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="13eae-129">屬性包含實例的路徑，編碼為字串參數-如果實例在 CIM 架構中建立模型。</span><span class="sxs-lookup"><span data-stu-id="13eae-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="13eae-130">如果不是 CIM 實例，屬性會包含一些識別字串來為產生警示的實體命名。</span><span class="sxs-lookup"><span data-stu-id="13eae-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="13eae-131">路徑或識別字串會根據 AlertingElementFormat 屬性格式化。</span><span class="sxs-lookup"><span data-stu-id="13eae-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="13eae-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="13eae-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-135">限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。事件種類 ") </span><span class="sxs-lookup"><span data-stu-id="13eae-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-136">指示的主要分類。</span><span class="sxs-lookup"><span data-stu-id="13eae-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13eae-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="13eae-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-138">\- 其他。</span><span class="sxs-lookup"><span data-stu-id="13eae-138">\- Other.</span></span> <span data-ttu-id="13eae-139">指示的 OtherAlertType 屬性會傳達其分類。</span><span class="sxs-lookup"><span data-stu-id="13eae-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="13eae-140">列舉中的「其他」使用是標準的 CIM 慣例。</span><span class="sxs-lookup"><span data-stu-id="13eae-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="13eae-141">這表示目前的指示不符合此列舉所描述的類別。</span><span class="sxs-lookup"><span data-stu-id="13eae-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="13eae-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**通訊警示** (2) </span><span class="sxs-lookup"><span data-stu-id="13eae-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-143">這種類型的指示主要是與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="13eae-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="13eae-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**服務品質警示** (3) </span><span class="sxs-lookup"><span data-stu-id="13eae-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-145">這種類型的表示主要與實體的效能或功能中的效能或錯誤相關。</span><span class="sxs-lookup"><span data-stu-id="13eae-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="13eae-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**處理錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="13eae-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-147">這種類型的表示主要與軟體或處理錯誤相關。</span><span class="sxs-lookup"><span data-stu-id="13eae-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="13eae-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**裝置警示** (5) </span><span class="sxs-lookup"><span data-stu-id="13eae-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-149">這種類型的表示主要與設備或硬體錯誤相關。</span><span class="sxs-lookup"><span data-stu-id="13eae-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="13eae-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**環境警示** (6) </span><span class="sxs-lookup"><span data-stu-id="13eae-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-151">環境警示。</span><span class="sxs-lookup"><span data-stu-id="13eae-151">Environmental Alert.</span></span> <span data-ttu-id="13eae-152">這種類型的指示主要是與硬體所在主機殼相關的條件相關聯，或其他環境考慮。</span><span class="sxs-lookup"><span data-stu-id="13eae-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="13eae-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**模型變更** (7) </span><span class="sxs-lookup"><span data-stu-id="13eae-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-154">指示會解決資訊模型中的變更。</span><span class="sxs-lookup"><span data-stu-id="13eae-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="13eae-155">例如，它可能會內嵌生命週期指示，以傳達要警示的特定模型變更。</span><span class="sxs-lookup"><span data-stu-id="13eae-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="13eae-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**安全性警示** (8) </span><span class="sxs-lookup"><span data-stu-id="13eae-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-157">.</span><span class="sxs-lookup"><span data-stu-id="13eae-157">.</span></span> <span data-ttu-id="13eae-158">這種類型的指示會相關聯。</span><span class="sxs-lookup"><span data-stu-id="13eae-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13eae-159">**說明**</span><span class="sxs-lookup"><span data-stu-id="13eae-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-162">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。其他文字 ") </span><span class="sxs-lookup"><span data-stu-id="13eae-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-163">指示的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="13eae-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="13eae-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-167">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") </span><span class="sxs-lookup"><span data-stu-id="13eae-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-168">檢測或提供者特定的值，用來描述以指示表示的基礎真實世界事件。</span><span class="sxs-lookup"><span data-stu-id="13eae-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="13eae-169">具有相同非 Null **EventID** 值的指標會被建立實體考慮，以代表相同的事件。</span><span class="sxs-lookup"><span data-stu-id="13eae-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="13eae-170">兩個 **EventID** 值的比較只會針對具有相同、非 Null 值 **SystemCreateClassName**、 **SystemName** 和 **ProviderName** 屬性的警示指示而定義。</span><span class="sxs-lookup"><span data-stu-id="13eae-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="13eae-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-172">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="13eae-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-174">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") </span><span class="sxs-lookup"><span data-stu-id="13eae-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-175">指出第一次偵測到基礎事件的時間和日期。</span><span class="sxs-lookup"><span data-stu-id="13eae-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="13eae-176">如果指定了此值，且建立的實體無法提供這項資訊，則此屬性必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="13eae-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="13eae-177">此值是以產生指示之 **CIM \_ ManageSystemElement** 物件的本地日期和時間的概念為基礎。</span><span class="sxs-lookup"><span data-stu-id="13eae-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-178">**訊息**</span><span class="sxs-lookup"><span data-stu-id="13eae-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-181">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**MessageID**"，"**CIM \_ AlertIndication**。**MessageArguments**") </span><span class="sxs-lookup"><span data-stu-id="13eae-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-182">警示指示的格式化訊息。</span><span class="sxs-lookup"><span data-stu-id="13eae-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="13eae-183">這則訊息的格式化方式是結合 **MessageArguments** 屬性中指定的一或多個動態元素，以及 **MessageID** 屬性唯一識別的靜態專案。</span><span class="sxs-lookup"><span data-stu-id="13eae-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-184">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="13eae-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-185">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="13eae-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13eae-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-187">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**Message**"，"**CIM \_ AlertIndication**。**MessageID**") </span><span class="sxs-lookup"><span data-stu-id="13eae-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-188">陣列，其中包含警示指示之訊息的動態內容。</span><span class="sxs-lookup"><span data-stu-id="13eae-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-189">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="13eae-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-192">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**Message**"，"**CIM \_ AlertIndication**。**MessageArguments**") </span><span class="sxs-lookup"><span data-stu-id="13eae-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-193">訊息格式的唯一識別碼，遷移在 **OwningEntity** 中指定之組織的範圍。</span><span class="sxs-lookup"><span data-stu-id="13eae-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-194">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="13eae-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-197">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingElementFormat**") </span><span class="sxs-lookup"><span data-stu-id="13eae-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-198">當 **AlertingElementFormat** 屬性設定為 "1" (其他) 時，定義 **AlertingManagedElement** 屬性的格式;否則，此值必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="13eae-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-199">**OtherAlertType**</span><span class="sxs-lookup"><span data-stu-id="13eae-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-202">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertType**") </span><span class="sxs-lookup"><span data-stu-id="13eae-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-203">當 **AlertType** 屬性設定為 "1" (其他狀態變更) 時，描述 **AlertType** 值的字串。</span><span class="sxs-lookup"><span data-stu-id="13eae-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="13eae-204">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="13eae-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13eae-207">擁有 **Message** 屬性格式定義之組織的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="13eae-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="13eae-208">**OwningEntity** 必須包含受著作權、商標或唯一的名稱，該名稱是由定義訊息格式的商務實體或標準主體所擁有。</span><span class="sxs-lookup"><span data-stu-id="13eae-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-209">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="13eae-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-210">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="13eae-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-212">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PerceivedSeverity" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="13eae-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-213">從引發警示之元素的觀點來指出警示的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="13eae-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13eae-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="13eae-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-215">遵循常見的使用方式。</span><span class="sxs-lookup"><span data-stu-id="13eae-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13eae-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="13eae-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-217">表示可以在 OtherSeverity 屬性中找到嚴重性的值。</span><span class="sxs-lookup"><span data-stu-id="13eae-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="13eae-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) </span><span class="sxs-lookup"><span data-stu-id="13eae-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-219">遵循常見的使用方式。</span><span class="sxs-lookup"><span data-stu-id="13eae-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="13eae-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) </span><span class="sxs-lookup"><span data-stu-id="13eae-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-221">如果適合讓使用者決定是否需要採取動作，則應該使用。</span><span class="sxs-lookup"><span data-stu-id="13eae-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="13eae-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) </span><span class="sxs-lookup"><span data-stu-id="13eae-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-223">指出需要採取動作，但目前的情況並不嚴重。</span><span class="sxs-lookup"><span data-stu-id="13eae-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="13eae-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) </span><span class="sxs-lookup"><span data-stu-id="13eae-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-225">指出現在需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="13eae-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="13eae-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) </span><span class="sxs-lookup"><span data-stu-id="13eae-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-227">現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。</span><span class="sxs-lookup"><span data-stu-id="13eae-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="13eae-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) </span><span class="sxs-lookup"><span data-stu-id="13eae-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="13eae-229">指出發生錯誤，但太晚採取補救動作。</span><span class="sxs-lookup"><span data-stu-id="13eae-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13eae-230">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="13eae-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-231">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="13eae-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-233">限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。可能的原因 "、" \| M3100. probableCause "、" itu-IANA-鬧鐘-TC ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**。**ProbableCauseDescription**"，"**CIM \_ AlertIndication**.**EventID**"，"**CIM \_ AlertIndication**。**EventTime**") </span><span class="sxs-lookup"><span data-stu-id="13eae-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-234">導致警示指示的情況可能原因。</span><span class="sxs-lookup"><span data-stu-id="13eae-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13eae-235">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="13eae-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13eae-236">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="13eae-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="13eae-237">**介面卡/卡片錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="13eae-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="13eae-238">**應用程式子系統失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="13eae-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="13eae-239">**頻寬減少** (4) </span><span class="sxs-lookup"><span data-stu-id="13eae-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="13eae-240">**連接建立錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="13eae-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="13eae-241">**通訊協定錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="13eae-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="13eae-242">**通訊子系統失敗** (7) </span><span class="sxs-lookup"><span data-stu-id="13eae-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="13eae-243">設定 **/自訂錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="13eae-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="13eae-244">**擁塞** (9) </span><span class="sxs-lookup"><span data-stu-id="13eae-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="13eae-245">**已** 損毀的資料 (10) </span><span class="sxs-lookup"><span data-stu-id="13eae-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="13eae-246">**CPU 週期限制超過** (11) </span><span class="sxs-lookup"><span data-stu-id="13eae-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="13eae-247">**資料集/數據機錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="13eae-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="13eae-248">**降級的信號** (13) </span><span class="sxs-lookup"><span data-stu-id="13eae-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="13eae-249">**DTE-DCE 介面錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="13eae-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="13eae-250">**主機殼門開啟** (15) </span><span class="sxs-lookup"><span data-stu-id="13eae-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="13eae-251">**設備故障** (16) </span><span class="sxs-lookup"><span data-stu-id="13eae-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="13eae-252">**過度震動** (17) </span><span class="sxs-lookup"><span data-stu-id="13eae-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="13eae-253">**檔案格式錯誤** (18) </span><span class="sxs-lookup"><span data-stu-id="13eae-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="13eae-254">**引發偵測到** (19) </span><span class="sxs-lookup"><span data-stu-id="13eae-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="13eae-255">偵測 **到大量** (20) </span><span class="sxs-lookup"><span data-stu-id="13eae-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="13eae-256">**框架錯誤** (21) </span><span class="sxs-lookup"><span data-stu-id="13eae-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="13eae-257">**HVAC 問題** (22) </span><span class="sxs-lookup"><span data-stu-id="13eae-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="13eae-258">不 **接受濕度** (23) </span><span class="sxs-lookup"><span data-stu-id="13eae-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="13eae-259">**I/o 裝置錯誤** (24) </span><span class="sxs-lookup"><span data-stu-id="13eae-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="13eae-260">**輸入裝置錯誤** (25) </span><span class="sxs-lookup"><span data-stu-id="13eae-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="13eae-261">**區域網路錯誤** (26) </span><span class="sxs-lookup"><span data-stu-id="13eae-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="13eae-262">偵測 **到未有毒的** 流失 (27) </span><span class="sxs-lookup"><span data-stu-id="13eae-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="13eae-263">**本機節點傳輸錯誤** (28) </span><span class="sxs-lookup"><span data-stu-id="13eae-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="13eae-264">**遺失框架** (29) </span><span class="sxs-lookup"><span data-stu-id="13eae-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="13eae-265"> (30) **的信號遺失**</span><span class="sxs-lookup"><span data-stu-id="13eae-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="13eae-266">**物料供應已用盡** (31) </span><span class="sxs-lookup"><span data-stu-id="13eae-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="13eae-267">多工器 **問題** (32) </span><span class="sxs-lookup"><span data-stu-id="13eae-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="13eae-268">**記憶體不足** (33) </span><span class="sxs-lookup"><span data-stu-id="13eae-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="13eae-269">**輸出裝置錯誤** (34) </span><span class="sxs-lookup"><span data-stu-id="13eae-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="13eae-270">**效能降低** (35) </span><span class="sxs-lookup"><span data-stu-id="13eae-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="13eae-271">**電源問題** (36) </span><span class="sxs-lookup"><span data-stu-id="13eae-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="13eae-272">**不可接受的壓力** (37) </span><span class="sxs-lookup"><span data-stu-id="13eae-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="13eae-273">**處理器問題 (內部電腦錯誤)** (38) </span><span class="sxs-lookup"><span data-stu-id="13eae-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="13eae-274">提取 **失敗** (39) </span><span class="sxs-lookup"><span data-stu-id="13eae-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="13eae-275">**佇列大小超過** (40) </span><span class="sxs-lookup"><span data-stu-id="13eae-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="13eae-276">**接收失敗** (41) </span><span class="sxs-lookup"><span data-stu-id="13eae-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="13eae-277">**接收者失敗** (42) </span><span class="sxs-lookup"><span data-stu-id="13eae-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="13eae-278">**遠端節點傳輸錯誤** (43) </span><span class="sxs-lookup"><span data-stu-id="13eae-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="13eae-279">**資源或接近容量** (44) </span><span class="sxs-lookup"><span data-stu-id="13eae-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="13eae-280">**回應時間過度** (45) </span><span class="sxs-lookup"><span data-stu-id="13eae-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="13eae-281">重新 **傳輸速率過高** (46) </span><span class="sxs-lookup"><span data-stu-id="13eae-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="13eae-282">**軟體錯誤** (47) </span><span class="sxs-lookup"><span data-stu-id="13eae-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="13eae-283">**軟體程式異常終止** (48) </span><span class="sxs-lookup"><span data-stu-id="13eae-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="13eae-284">**軟體程式錯誤 (不正確的結果)** (49) </span><span class="sxs-lookup"><span data-stu-id="13eae-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="13eae-285">**儲存體容量問題** (50) </span><span class="sxs-lookup"><span data-stu-id="13eae-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="13eae-286">無法 **接受的溫度** (51) </span><span class="sxs-lookup"><span data-stu-id="13eae-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="13eae-287">**超過** (52) 的閾值</span><span class="sxs-lookup"><span data-stu-id="13eae-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="13eae-288">**計時問題** (53) </span><span class="sxs-lookup"><span data-stu-id="13eae-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="13eae-289">偵測 **到有毒** 流失 (54) </span><span class="sxs-lookup"><span data-stu-id="13eae-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="13eae-290">**傳輸失敗** (55) </span><span class="sxs-lookup"><span data-stu-id="13eae-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="13eae-291">**發送器失敗** (56) </span><span class="sxs-lookup"><span data-stu-id="13eae-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="13eae-292">**基礎資源無法使用** (57) </span><span class="sxs-lookup"><span data-stu-id="13eae-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="13eae-293">**版本不相符** (58) </span><span class="sxs-lookup"><span data-stu-id="13eae-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="13eae-294">**先前的警示已清除** (59) </span><span class="sxs-lookup"><span data-stu-id="13eae-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="13eae-295">**登入嘗試失敗** (60) </span><span class="sxs-lookup"><span data-stu-id="13eae-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="13eae-296">偵測 **到的軟體病毒** (61) </span><span class="sxs-lookup"><span data-stu-id="13eae-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="13eae-297">**硬體安全性違反** 了 (62) </span><span class="sxs-lookup"><span data-stu-id="13eae-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="13eae-298">偵測 **到拒絕服務** (63) </span><span class="sxs-lookup"><span data-stu-id="13eae-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="13eae-299">**安全性認證不符** (64) </span><span class="sxs-lookup"><span data-stu-id="13eae-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="13eae-300">**未經授權的存取** (65) </span><span class="sxs-lookup"><span data-stu-id="13eae-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="13eae-301">**已收到** (66) 的鬧鐘</span><span class="sxs-lookup"><span data-stu-id="13eae-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="13eae-302">**遺失指標** (67) </span><span class="sxs-lookup"><span data-stu-id="13eae-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="13eae-303">承載 **不符** (68) </span><span class="sxs-lookup"><span data-stu-id="13eae-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="13eae-304">**傳輸錯誤** (69) </span><span class="sxs-lookup"><span data-stu-id="13eae-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="13eae-305">**過多錯誤率** (70) </span><span class="sxs-lookup"><span data-stu-id="13eae-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="13eae-306">**追蹤問題** (71) </span><span class="sxs-lookup"><span data-stu-id="13eae-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="13eae-307">**元素無法使用** (72) </span><span class="sxs-lookup"><span data-stu-id="13eae-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="13eae-308">**遺漏的元素** (73) </span><span class="sxs-lookup"><span data-stu-id="13eae-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="13eae-309">**遺失多框架** (74) </span><span class="sxs-lookup"><span data-stu-id="13eae-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="13eae-310">**廣播通道失敗** (75) </span><span class="sxs-lookup"><span data-stu-id="13eae-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="13eae-311">**收到的訊息無效** (76) </span><span class="sxs-lookup"><span data-stu-id="13eae-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="13eae-312">**路由失敗** (77) </span><span class="sxs-lookup"><span data-stu-id="13eae-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="13eae-313">**背板失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="13eae-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="13eae-314">**識別碼重複** (79) </span><span class="sxs-lookup"><span data-stu-id="13eae-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="13eae-315">**保護路徑失敗** (80) </span><span class="sxs-lookup"><span data-stu-id="13eae-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="13eae-316">**同步遺失或** (81) 不相符</span><span class="sxs-lookup"><span data-stu-id="13eae-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="13eae-317">**終端機問題** (82) </span><span class="sxs-lookup"><span data-stu-id="13eae-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="13eae-318">**系統時鐘失敗** (83) </span><span class="sxs-lookup"><span data-stu-id="13eae-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="13eae-319">**天線失敗** (84) </span><span class="sxs-lookup"><span data-stu-id="13eae-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="13eae-320">**電池充電失敗** (85) </span><span class="sxs-lookup"><span data-stu-id="13eae-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="13eae-321">**磁片失敗** (86) </span><span class="sxs-lookup"><span data-stu-id="13eae-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="13eae-322">**頻率跳動失敗** (87) </span><span class="sxs-lookup"><span data-stu-id="13eae-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="13eae-323">**遺失冗余** (88) </span><span class="sxs-lookup"><span data-stu-id="13eae-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="13eae-324">**電源供應器失敗** (89) </span><span class="sxs-lookup"><span data-stu-id="13eae-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="13eae-325">**信號品質問題** (90) </span><span class="sxs-lookup"><span data-stu-id="13eae-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="13eae-326">**電池放電** (91) </span><span class="sxs-lookup"><span data-stu-id="13eae-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="13eae-327">**電池故障** (92) </span><span class="sxs-lookup"><span data-stu-id="13eae-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="13eae-328">**商業電源問題** (93) </span><span class="sxs-lookup"><span data-stu-id="13eae-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="13eae-329">**風扇故障** (94) </span><span class="sxs-lookup"><span data-stu-id="13eae-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="13eae-330">**引擎失敗** (95) </span><span class="sxs-lookup"><span data-stu-id="13eae-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="13eae-331">**感應器失敗** (96) </span><span class="sxs-lookup"><span data-stu-id="13eae-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="13eae-332">**保險絲故障** (97) </span><span class="sxs-lookup"><span data-stu-id="13eae-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="13eae-333">產生器 **失敗** (98) </span><span class="sxs-lookup"><span data-stu-id="13eae-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="13eae-334">**電力偏低** (99) </span><span class="sxs-lookup"><span data-stu-id="13eae-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="13eae-335">**低燃料** (100) </span><span class="sxs-lookup"><span data-stu-id="13eae-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="13eae-336">**低水位** (101) </span><span class="sxs-lookup"><span data-stu-id="13eae-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="13eae-337">**爆炸性天然氣** (102) </span><span class="sxs-lookup"><span data-stu-id="13eae-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="13eae-338">**高接近尾聲** (103) </span><span class="sxs-lookup"><span data-stu-id="13eae-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="13eae-339">**Ice 堆積** (104) </span><span class="sxs-lookup"><span data-stu-id="13eae-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="13eae-340">**冒煙** (105) </span><span class="sxs-lookup"><span data-stu-id="13eae-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="13eae-341">**記憶體不符** (106) </span><span class="sxs-lookup"><span data-stu-id="13eae-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="13eae-342">**CPU 週期** (107) </span><span class="sxs-lookup"><span data-stu-id="13eae-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="13eae-343">**軟體環境問題** (108) </span><span class="sxs-lookup"><span data-stu-id="13eae-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="13eae-344">**軟體下載失敗** (109) </span><span class="sxs-lookup"><span data-stu-id="13eae-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="13eae-345">**元素重新初始化** (110) </span><span class="sxs-lookup"><span data-stu-id="13eae-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="13eae-346">**Timeout** (111) </span><span class="sxs-lookup"><span data-stu-id="13eae-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="13eae-347">**記錄問題** (112) </span><span class="sxs-lookup"><span data-stu-id="13eae-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="13eae-348">偵測到 (113) 的 **洩漏**</span><span class="sxs-lookup"><span data-stu-id="13eae-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="13eae-349">**保護機制失敗** (114) </span><span class="sxs-lookup"><span data-stu-id="13eae-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="13eae-350">**保護資源失敗** (115) </span><span class="sxs-lookup"><span data-stu-id="13eae-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="13eae-351">**資料庫不一致** (116) </span><span class="sxs-lookup"><span data-stu-id="13eae-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="13eae-352">**驗證失敗** (117) </span><span class="sxs-lookup"><span data-stu-id="13eae-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="13eae-353"> (118) **的機密性缺口**</span><span class="sxs-lookup"><span data-stu-id="13eae-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="13eae-354">**纜線防** (119) </span><span class="sxs-lookup"><span data-stu-id="13eae-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="13eae-355">**延遲的資訊** (120) </span><span class="sxs-lookup"><span data-stu-id="13eae-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="13eae-356">**重複的資訊** (121) </span><span class="sxs-lookup"><span data-stu-id="13eae-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="13eae-357">**遺漏** (122) 的資訊</span><span class="sxs-lookup"><span data-stu-id="13eae-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="13eae-358"> (123) 的 **資訊修改**</span><span class="sxs-lookup"><span data-stu-id="13eae-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="13eae-359">**順序中的資訊** (124) </span><span class="sxs-lookup"><span data-stu-id="13eae-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="13eae-360">**金鑰已過期** (125) </span><span class="sxs-lookup"><span data-stu-id="13eae-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="13eae-361">**不可否認性失敗** (126) </span><span class="sxs-lookup"><span data-stu-id="13eae-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="13eae-362">下班 **時間活動** (127) </span><span class="sxs-lookup"><span data-stu-id="13eae-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="13eae-363">**服務** (128) </span><span class="sxs-lookup"><span data-stu-id="13eae-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="13eae-364">程式 **錯誤** (129) </span><span class="sxs-lookup"><span data-stu-id="13eae-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="13eae-365">未 **預期的資訊** (130) </span><span class="sxs-lookup"><span data-stu-id="13eae-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13eae-366">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="13eae-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-369">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") </span><span class="sxs-lookup"><span data-stu-id="13eae-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-370">**ProbableCause** 屬性的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13eae-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="13eae-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-372">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-374">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="13eae-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13eae-375">產生指示的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="13eae-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-376">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="13eae-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-377">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="13eae-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="13eae-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-379">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。建議的修復動作」 ) </span><span class="sxs-lookup"><span data-stu-id="13eae-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-380">用於解決通知原因之建議動作的自由形式描述。</span><span class="sxs-lookup"><span data-stu-id="13eae-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-381">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13eae-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-384">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="13eae-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13eae-385">產生指示之提供者的範圍系統的 **CreationClassName** 值。</span><span class="sxs-lookup"><span data-stu-id="13eae-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="13eae-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13eae-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-389">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="13eae-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="13eae-390">產生指示之提供者的範圍系統名稱。</span><span class="sxs-lookup"><span data-stu-id="13eae-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="13eae-391">**趨勢**</span><span class="sxs-lookup"><span data-stu-id="13eae-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eae-392">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="13eae-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eae-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13eae-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eae-394">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。TrendIndication ") </span><span class="sxs-lookup"><span data-stu-id="13eae-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="13eae-395">提供趨勢趨勢-向上、向下或無變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13eae-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13eae-396">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="13eae-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="13eae-397">**不適用** (1) </span><span class="sxs-lookup"><span data-stu-id="13eae-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="13eae-398">**趨勢向上** (2) </span><span class="sxs-lookup"><span data-stu-id="13eae-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="13eae-399"> (3) 的 **趨勢**</span><span class="sxs-lookup"><span data-stu-id="13eae-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="13eae-400">**沒有變更** (4) </span><span class="sxs-lookup"><span data-stu-id="13eae-400">**No Change** (4)</span></span>


<span data-ttu-id="13eae-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="13eae-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="13eae-402">規格需求</span><span class="sxs-lookup"><span data-stu-id="13eae-402">Requirements</span></span>



| <span data-ttu-id="13eae-403">需求</span><span class="sxs-lookup"><span data-stu-id="13eae-403">Requirement</span></span> | <span data-ttu-id="13eae-404">值</span><span class="sxs-lookup"><span data-stu-id="13eae-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13eae-405">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13eae-405">Minimum supported client</span></span><br/> | <span data-ttu-id="13eae-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13eae-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13eae-407">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13eae-407">Minimum supported server</span></span><br/> | <span data-ttu-id="13eae-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13eae-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13eae-409">命名空間</span><span class="sxs-lookup"><span data-stu-id="13eae-409">Namespace</span></span><br/>                | <span data-ttu-id="13eae-410">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="13eae-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13eae-411">MOF</span><span class="sxs-lookup"><span data-stu-id="13eae-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13eae-412"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="13eae-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13eae-413">DLL</span><span class="sxs-lookup"><span data-stu-id="13eae-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13eae-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13eae-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13eae-415">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13eae-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13eae-416">**CIM \_ ProcessIndication**</span><span class="sxs-lookup"><span data-stu-id="13eae-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

