---
description: 包含嚴重性、原因、建議動作，以及與 CIM 作業失敗相關之其他資料的相關資訊。
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026817"
---
# <a name="msvm_error-class"></a><span data-ttu-id="deba3-103">Msvm \_ Error 類別</span><span class="sxs-lookup"><span data-stu-id="deba3-103">Msvm\_Error class</span></span>

<span data-ttu-id="deba3-104">特製化類別，其中包含有關「嚴重性」、「原因」、「建議的動作」和「CIM」作業失敗的其他資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="deba3-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="deba3-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="deba3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="deba3-106">語法</span><span class="sxs-lookup"><span data-stu-id="deba3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="deba3-107">成員</span><span class="sxs-lookup"><span data-stu-id="deba3-107">Members</span></span>

<span data-ttu-id="deba3-108">**Msvm \_ Error** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="deba3-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="deba3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="deba3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="deba3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="deba3-110">Properties</span></span>

<span data-ttu-id="deba3-111">**Msvm \_ 錯誤** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="deba3-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="deba3-112">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="deba3-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="deba3-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-115">此實例的特性的 CIM 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="deba3-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="deba3-116">這個屬性會定義符合的 CIM 伺服器或接聽程式可能傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="deba3-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="deba3-117">並非所有狀態碼都對每項作業都有效。</span><span class="sxs-lookup"><span data-stu-id="deba3-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="deba3-118">每項作業的規格都應該定義該作業可能傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="deba3-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="deba3-119">系統會定義 CIM 狀態碼的下列值。</span><span class="sxs-lookup"><span data-stu-id="deba3-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="deba3-120">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="deba3-121">值</span><span class="sxs-lookup"><span data-stu-id="deba3-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="deba3-122">意義</span><span class="sxs-lookup"><span data-stu-id="deba3-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="deba3-123"><dt>**CIM \_錯誤 \_ 失敗**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="deba3-124">發生的一般錯誤未涵蓋于更明確的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="deba3-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="deba3-125"><dt>**CIM \_錯誤 \_ \_ 拒絕存取**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="deba3-126">用戶端無法使用 CIM 資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="deba3-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="deba3-127"><dt>**CIM \_錯誤 \_ 不正確 \_ 命名空間**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="deba3-128">目標命名空間不存在。</span><span class="sxs-lookup"><span data-stu-id="deba3-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="deba3-129"><dt>**CIM \_錯誤 \_ 不正確 \_ 參數**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="deba3-130">傳遞給方法的一或多個參數值無效。</span><span class="sxs-lookup"><span data-stu-id="deba3-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="deba3-131"><dt>**CIM \_錯誤 \_ \_ 類別**</dt> <dt>5</dt>無效</span><span class="sxs-lookup"><span data-stu-id="deba3-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="deba3-132">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="deba3-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="deba3-133"><dt>**CIM \_\_找不 \_ 到錯誤**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="deba3-134">找不到要求的物件。</span><span class="sxs-lookup"><span data-stu-id="deba3-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="deba3-135"><dt>**CIM \_錯誤 \_ 不 \_ 支援**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="deba3-136">不支援要求的作業。</span><span class="sxs-lookup"><span data-stu-id="deba3-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="deba3-137"><dt>**CIM \_ERR \_ 類別 \_ 有 \_ 子**</dt>系 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="deba3-138">無法在這個類別上執行操作，因為它有實例。</span><span class="sxs-lookup"><span data-stu-id="deba3-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="deba3-139"><dt>**CIM \_ERR \_ 類別 \_ 具有 \_ 實例**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="deba3-140">無法在這個類別上執行操作，因為它有實例。</span><span class="sxs-lookup"><span data-stu-id="deba3-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="deba3-141"><dt>**CIM \_錯誤 \_ 不正確 \_ 超類別**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="deba3-142">因為指定的超類別不存在，所以無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="deba3-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="deba3-143"><dt>**CIM \_錯誤 \_ 已經 \_ 存在**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="deba3-144">無法執行操作，因為物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="deba3-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="deba3-145"><dt>**CIM \_錯誤 \_ 沒有 \_ 這類的 \_ 屬性**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="deba3-146">指定的屬性不存在。</span><span class="sxs-lookup"><span data-stu-id="deba3-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="deba3-147"><dt>**CIM \_錯誤 \_ 類型 \_ 不符**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="deba3-148">提供的值與類型不相容。</span><span class="sxs-lookup"><span data-stu-id="deba3-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="deba3-149"><dt>**CIM \_\_ \_ \_ 不 \_ 支援的 ERR 查詢語言**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="deba3-150">無法辨識或支援查詢語言。</span><span class="sxs-lookup"><span data-stu-id="deba3-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="deba3-151"><dt>**CIM \_錯誤 \_ 不正確 \_ 查詢**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="deba3-152">查詢對指定的查詢語言無效。</span><span class="sxs-lookup"><span data-stu-id="deba3-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="deba3-153"><dt>**CIM \_ERR \_ 方法 \_ 不可 \_ 用**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="deba3-154">無法執行外部方法。</span><span class="sxs-lookup"><span data-stu-id="deba3-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="deba3-155"><dt>**CIM \_\_ \_ \_ 找不到錯誤的方法**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="deba3-156">指定的外部方法不存在。</span><span class="sxs-lookup"><span data-stu-id="deba3-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="deba3-157"><dt>**CIM \_錯誤的未 \_ 預期 \_ 回應**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="deba3-158">對非同步作業所傳回的回應不是預期的。</span><span class="sxs-lookup"><span data-stu-id="deba3-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="deba3-159"><dt>**CIM \_錯誤 \_ 不正確 \_ 回應 \_ 目的地**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="deba3-160">非同步回應的指定目的地無效。</span><span class="sxs-lookup"><span data-stu-id="deba3-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="deba3-161"><dt>**CIM \_ERR \_ 命名空間 \_ 不是 \_ 空**</dt>的 <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="deba3-162">指定的命名空間不是空的。</span><span class="sxs-lookup"><span data-stu-id="deba3-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="deba3-163"><dt>已 **保留 DMTF**</dt><dt>21 =*值*</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="deba3-164">保留值。</span><span class="sxs-lookup"><span data-stu-id="deba3-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="deba3-165">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="deba3-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-168">字串，包含使用者可讀取的 **CIMStatusCode** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="deba3-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="deba3-169">這項描述可延伸，但必須與 **CIMStatusCode** 定義一致。</span><span class="sxs-lookup"><span data-stu-id="deba3-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="deba3-170">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-171">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="deba3-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-174"> (實例) 產生錯誤之實體的識別資訊。</span><span class="sxs-lookup"><span data-stu-id="deba3-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="deba3-175">如果此實體在 CIM 架構中建立模型，這個屬性會包含編碼為字串參數之實例的路徑。</span><span class="sxs-lookup"><span data-stu-id="deba3-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="deba3-176">如果未建立模型，屬性會包含一些識別字串來為產生錯誤的實體命名。</span><span class="sxs-lookup"><span data-stu-id="deba3-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="deba3-177">路徑或識別字串會根據 **ErrorSourceFormat** 屬性格式化。</span><span class="sxs-lookup"><span data-stu-id="deba3-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="deba3-178">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-179">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="deba3-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="deba3-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-182">**ErrorSource** 屬性的格式會根據此屬性的值可解譯。</span><span class="sxs-lookup"><span data-stu-id="deba3-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="deba3-183">這個屬性是從 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))繼承而來，而且一律設定為0。</span><span class="sxs-lookup"><span data-stu-id="deba3-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="deba3-184">值</span><span class="sxs-lookup"><span data-stu-id="deba3-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="deba3-185">意義</span><span class="sxs-lookup"><span data-stu-id="deba3-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="deba3-186"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="deba3-187">CIM 用戶端應用程式可解譯的格式不明或不具意義。</span><span class="sxs-lookup"><span data-stu-id="deba3-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="deba3-188"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="deba3-189">格式是由 **OtherErrorSourceFormat** 屬性的值所定義。</span><span class="sxs-lookup"><span data-stu-id="deba3-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="deba3-190"><dt>**CIMObjectHandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="deba3-191">使用針對 objectHandle 非終端機定義之 MOF 語法編碼的 CIM 物件控制碼，會用來識別實體。</span><span class="sxs-lookup"><span data-stu-id="deba3-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="deba3-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="deba3-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="deba3-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-195">錯誤的主要分類。</span><span class="sxs-lookup"><span data-stu-id="deba3-195">Primary classification of the error.</span></span> <span data-ttu-id="deba3-196">以下是定義的值。</span><span class="sxs-lookup"><span data-stu-id="deba3-196">The following values are defined.</span></span> <span data-ttu-id="deba3-197">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="deba3-198">值</span><span class="sxs-lookup"><span data-stu-id="deba3-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="deba3-199">意義</span><span class="sxs-lookup"><span data-stu-id="deba3-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="deba3-200"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="deba3-201"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="deba3-202"><dt>**通訊錯誤**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="deba3-203">此類型的錯誤主要與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="deba3-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="deba3-204"><dt>**服務品質錯誤**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="deba3-205">這種類型的錯誤主要與導致功能或效能降低的失敗有關。</span><span class="sxs-lookup"><span data-stu-id="deba3-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="deba3-206"><dt>**軟體錯誤**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="deba3-207">此類型的錯誤主要與軟體或處理錯誤相關。</span><span class="sxs-lookup"><span data-stu-id="deba3-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="deba3-208"><dt>**硬體錯誤**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="deba3-209">此類型的錯誤主要與設備或硬體故障相關聯。</span><span class="sxs-lookup"><span data-stu-id="deba3-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="deba3-210"><dt>**環境錯誤**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="deba3-211">此類型的錯誤主要與設備相關的失敗狀況或其他環境考慮相關。</span><span class="sxs-lookup"><span data-stu-id="deba3-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="deba3-212"><dt>**安全性錯誤**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="deba3-213">此類型的錯誤與安全性違規、病毒偵測和類似問題相關聯。</span><span class="sxs-lookup"><span data-stu-id="deba3-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="deba3-214"><dt>**過度訂閱錯誤**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="deba3-215">此類型的錯誤主要與失敗相關，無法配置足夠的資源來完成作業。</span><span class="sxs-lookup"><span data-stu-id="deba3-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="deba3-216"><dt>**無法使用的資源錯誤**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="deba3-217">此類型的錯誤主要與無法存取所需資源的相關聯。</span><span class="sxs-lookup"><span data-stu-id="deba3-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="deba3-218"><dt>**不支援的操作錯誤**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="deba3-219">此類型的錯誤主要與不支援的要求相關聯。</span><span class="sxs-lookup"><span data-stu-id="deba3-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="deba3-220">**訊息**</span><span class="sxs-lookup"><span data-stu-id="deba3-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-223">格式化的訊息。</span><span class="sxs-lookup"><span data-stu-id="deba3-223">The formatted message.</span></span> <span data-ttu-id="deba3-224">此訊息的建立方式是將訊息的動態內容（如 **MessageArguments** 所述）套用至 **OwningEntity** 範圍內唯一識別的格式字串（藉由 **MessageID**）。</span><span class="sxs-lookup"><span data-stu-id="deba3-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="deba3-225">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-226">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="deba3-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-227">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="deba3-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="deba3-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-229">陣列，其中包含訊息的動態內容。</span><span class="sxs-lookup"><span data-stu-id="deba3-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="deba3-230">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-231">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="deba3-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-234">在 **OwningEntity** 範圍內唯一識別的不透明字串，這是訊息的格式。</span><span class="sxs-lookup"><span data-stu-id="deba3-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="deba3-235">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-236">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="deba3-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-239">為 **ErrorSourceFormat** 定義「其他」值的字串。</span><span class="sxs-lookup"><span data-stu-id="deba3-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="deba3-240">當 **ErrorSourceFormat** 設定為 1 (其他) 的值時，此值必須設定為非 Null 值。</span><span class="sxs-lookup"><span data-stu-id="deba3-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="deba3-241">對於 **ErrorSourceFormat** 的所有其他值，此字串的值必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="deba3-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="deba3-242">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-243">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="deba3-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-246">描述當1， (其他) 指定為 **ErrorType** 時，描述 **ErrorType** 的字串。</span><span class="sxs-lookup"><span data-stu-id="deba3-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="deba3-247">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-248">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="deba3-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-251">唯一識別實體的字串，該實體擁有此實例中所描述之訊息格式的定義。</span><span class="sxs-lookup"><span data-stu-id="deba3-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="deba3-252">**OwningEntity** 必須包含由商務實體或定義格式的標準內容所擁有的受著作權、商標或其他唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="deba3-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="deba3-253">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-254">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="deba3-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-255">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="deba3-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-257">列舉值，描述來自通知者觀點之錯誤的嚴重性： 2-低應用於非嚴重問題，例如不正確參數、不正確的使用方式、不支援的功能。</span><span class="sxs-lookup"><span data-stu-id="deba3-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="deba3-258">應該使用 3-Medium 來指出需要採取動作，但目前的情況並不嚴重。</span><span class="sxs-lookup"><span data-stu-id="deba3-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="deba3-259">4-High 應該用來指出現在需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="deba3-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="deba3-260">5-嚴重應用來指出資料遺失或無法復原的系統或服務失敗。</span><span class="sxs-lookup"><span data-stu-id="deba3-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="deba3-261">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="deba3-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="deba3-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (2) </span><span class="sxs-lookup"><span data-stu-id="deba3-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**中型** (3) </span><span class="sxs-lookup"><span data-stu-id="deba3-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (4) </span><span class="sxs-lookup"><span data-stu-id="deba3-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**嚴重** (5 ) </span><span class="sxs-lookup"><span data-stu-id="deba3-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="deba3-267">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="deba3-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-268">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="deba3-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-270">描述錯誤可能原因的列舉值。</span><span class="sxs-lookup"><span data-stu-id="deba3-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="deba3-271">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="deba3-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="deba3-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="deba3-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**介面卡/卡片錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="deba3-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**應用程式子系統失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="deba3-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**頻寬減少** (4) </span><span class="sxs-lookup"><span data-stu-id="deba3-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**連接建立錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="deba3-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**通訊協定錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="deba3-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**通訊子系統失敗** (7) </span><span class="sxs-lookup"><span data-stu-id="deba3-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>設定 **/自訂錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="deba3-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**擁塞** (9) </span><span class="sxs-lookup"><span data-stu-id="deba3-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**已** 損毀的資料 (10) </span><span class="sxs-lookup"><span data-stu-id="deba3-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU 週期限制超過** (11) </span><span class="sxs-lookup"><span data-stu-id="deba3-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**資料集/數據機錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="deba3-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**降級的信號** (13) </span><span class="sxs-lookup"><span data-stu-id="deba3-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE 介面錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="deba3-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**主機殼門開啟** (15) </span><span class="sxs-lookup"><span data-stu-id="deba3-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**設備故障** (16) </span><span class="sxs-lookup"><span data-stu-id="deba3-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**過度震動** (17) </span><span class="sxs-lookup"><span data-stu-id="deba3-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**檔案格式錯誤** (18) </span><span class="sxs-lookup"><span data-stu-id="deba3-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**引發偵測到** (19) </span><span class="sxs-lookup"><span data-stu-id="deba3-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>偵測 **到大量** (20) </span><span class="sxs-lookup"><span data-stu-id="deba3-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**框架錯誤** (21) </span><span class="sxs-lookup"><span data-stu-id="deba3-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC 問題** (22) </span><span class="sxs-lookup"><span data-stu-id="deba3-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>不 **接受濕度** (23) </span><span class="sxs-lookup"><span data-stu-id="deba3-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/o 裝置錯誤** (24) </span><span class="sxs-lookup"><span data-stu-id="deba3-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**輸入裝置錯誤** (25) </span><span class="sxs-lookup"><span data-stu-id="deba3-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**區域網路錯誤** (26) </span><span class="sxs-lookup"><span data-stu-id="deba3-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>偵測 **到未有毒的** 流失 (27) </span><span class="sxs-lookup"><span data-stu-id="deba3-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**本機節點傳輸錯誤** (28) </span><span class="sxs-lookup"><span data-stu-id="deba3-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**遺失框架** (29) </span><span class="sxs-lookup"><span data-stu-id="deba3-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span> (30) **的信號遺失**</span><span class="sxs-lookup"><span data-stu-id="deba3-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**31** 個數據供應已用盡 (31) </span><span class="sxs-lookup"><span data-stu-id="deba3-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>多工器 **問題** (32) </span><span class="sxs-lookup"><span data-stu-id="deba3-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**記憶體不足** (33) </span><span class="sxs-lookup"><span data-stu-id="deba3-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**輸出裝置錯誤** (34) </span><span class="sxs-lookup"><span data-stu-id="deba3-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**效能降低** (35) </span><span class="sxs-lookup"><span data-stu-id="deba3-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**電源問題** (36) </span><span class="sxs-lookup"><span data-stu-id="deba3-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**不可接受的壓力** (37) </span><span class="sxs-lookup"><span data-stu-id="deba3-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**處理器問題 (內部電腦錯誤)** (38) </span><span class="sxs-lookup"><span data-stu-id="deba3-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>提取 **失敗** (39) </span><span class="sxs-lookup"><span data-stu-id="deba3-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**佇列大小超過** (40) </span><span class="sxs-lookup"><span data-stu-id="deba3-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**接收失敗** (41) </span><span class="sxs-lookup"><span data-stu-id="deba3-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**接收者失敗** (42) </span><span class="sxs-lookup"><span data-stu-id="deba3-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**遠端節點傳輸錯誤** (43) </span><span class="sxs-lookup"><span data-stu-id="deba3-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**資源或接近容量** (44) </span><span class="sxs-lookup"><span data-stu-id="deba3-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**回應時間過度** (45) </span><span class="sxs-lookup"><span data-stu-id="deba3-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>重新 **傳輸速率過高** (46) </span><span class="sxs-lookup"><span data-stu-id="deba3-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**軟體錯誤** (47) </span><span class="sxs-lookup"><span data-stu-id="deba3-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**軟體程式異常終止** (48) </span><span class="sxs-lookup"><span data-stu-id="deba3-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**軟體程式錯誤 (不正確的結果)** (49) </span><span class="sxs-lookup"><span data-stu-id="deba3-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**儲存體容量問題** (50) </span><span class="sxs-lookup"><span data-stu-id="deba3-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>無法 **接受的溫度** (51) </span><span class="sxs-lookup"><span data-stu-id="deba3-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**超過** (52) 的閾值</span><span class="sxs-lookup"><span data-stu-id="deba3-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**計時問題** (53) </span><span class="sxs-lookup"><span data-stu-id="deba3-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>偵測 **到有毒** 流失 (54) </span><span class="sxs-lookup"><span data-stu-id="deba3-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**傳輸失敗** (55) </span><span class="sxs-lookup"><span data-stu-id="deba3-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**發送器失敗** (56) </span><span class="sxs-lookup"><span data-stu-id="deba3-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**基礎資源無法使用** (57) </span><span class="sxs-lookup"><span data-stu-id="deba3-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**版本不相符** (58) </span><span class="sxs-lookup"><span data-stu-id="deba3-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**先前的警示已清除** (59) </span><span class="sxs-lookup"><span data-stu-id="deba3-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 登入嘗試失敗** (60) </span><span class="sxs-lookup"><span data-stu-id="deba3-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>偵測 **到的軟體病毒** (61) </span><span class="sxs-lookup"><span data-stu-id="deba3-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**硬體安全性違反** 了 (62) </span><span class="sxs-lookup"><span data-stu-id="deba3-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>偵測 **到拒絕服務** (63) </span><span class="sxs-lookup"><span data-stu-id="deba3-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**安全性認證不符** (64) </span><span class="sxs-lookup"><span data-stu-id="deba3-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**未經授權的存取** (65) </span><span class="sxs-lookup"><span data-stu-id="deba3-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**已收到** (66) 的鬧鐘</span><span class="sxs-lookup"><span data-stu-id="deba3-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**遺失指標** (67) </span><span class="sxs-lookup"><span data-stu-id="deba3-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>承載 **不符** (68) </span><span class="sxs-lookup"><span data-stu-id="deba3-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**傳輸錯誤** (69) </span><span class="sxs-lookup"><span data-stu-id="deba3-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**過多錯誤率** (70) </span><span class="sxs-lookup"><span data-stu-id="deba3-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**追蹤問題** (71) </span><span class="sxs-lookup"><span data-stu-id="deba3-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**元素無法使用** (72) </span><span class="sxs-lookup"><span data-stu-id="deba3-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**遺漏的元素** (73) </span><span class="sxs-lookup"><span data-stu-id="deba3-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**遺失多框架** (74) </span><span class="sxs-lookup"><span data-stu-id="deba3-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**廣播通道失敗** (75) </span><span class="sxs-lookup"><span data-stu-id="deba3-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**收到的訊息無效** (76) </span><span class="sxs-lookup"><span data-stu-id="deba3-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**路由失敗** (77) </span><span class="sxs-lookup"><span data-stu-id="deba3-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**背板失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="deba3-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**識別碼重複** (79) </span><span class="sxs-lookup"><span data-stu-id="deba3-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**保護路徑失敗** (80) </span><span class="sxs-lookup"><span data-stu-id="deba3-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**同步遺失或** (81) 不相符</span><span class="sxs-lookup"><span data-stu-id="deba3-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**終端機問題** (82) </span><span class="sxs-lookup"><span data-stu-id="deba3-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**系統時鐘失敗** (83) </span><span class="sxs-lookup"><span data-stu-id="deba3-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**天線失敗** (84) </span><span class="sxs-lookup"><span data-stu-id="deba3-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**電池充電失敗** (85) </span><span class="sxs-lookup"><span data-stu-id="deba3-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**磁片失敗** (86) </span><span class="sxs-lookup"><span data-stu-id="deba3-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**頻率跳動失敗** (87) </span><span class="sxs-lookup"><span data-stu-id="deba3-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**遺失冗余** (88) </span><span class="sxs-lookup"><span data-stu-id="deba3-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**電源供應器失敗** (89) </span><span class="sxs-lookup"><span data-stu-id="deba3-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**信號品質問題** (90) </span><span class="sxs-lookup"><span data-stu-id="deba3-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**91 電池放電** (91) </span><span class="sxs-lookup"><span data-stu-id="deba3-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**電池故障** (92) </span><span class="sxs-lookup"><span data-stu-id="deba3-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**商業電源問題** (93) </span><span class="sxs-lookup"><span data-stu-id="deba3-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**風扇故障** (94) </span><span class="sxs-lookup"><span data-stu-id="deba3-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**引擎失敗** (95) </span><span class="sxs-lookup"><span data-stu-id="deba3-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**感應器失敗** (96) </span><span class="sxs-lookup"><span data-stu-id="deba3-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**保險絲故障** (97) </span><span class="sxs-lookup"><span data-stu-id="deba3-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>產生器 **失敗** (98) </span><span class="sxs-lookup"><span data-stu-id="deba3-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**電力偏低** (99) </span><span class="sxs-lookup"><span data-stu-id="deba3-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**低燃料** (100) </span><span class="sxs-lookup"><span data-stu-id="deba3-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**低水位** (101) </span><span class="sxs-lookup"><span data-stu-id="deba3-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**爆炸性天然氣** (102) </span><span class="sxs-lookup"><span data-stu-id="deba3-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**高接近尾聲** (103) </span><span class="sxs-lookup"><span data-stu-id="deba3-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice 堆積** (104) </span><span class="sxs-lookup"><span data-stu-id="deba3-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**冒煙** (105) </span><span class="sxs-lookup"><span data-stu-id="deba3-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**記憶體不符** (106) </span><span class="sxs-lookup"><span data-stu-id="deba3-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**CPU 週期** (107) </span><span class="sxs-lookup"><span data-stu-id="deba3-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**軟體環境問題** (108) </span><span class="sxs-lookup"><span data-stu-id="deba3-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**軟體下載失敗** (109) </span><span class="sxs-lookup"><span data-stu-id="deba3-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**元素重新初始化** (110) </span><span class="sxs-lookup"><span data-stu-id="deba3-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111) </span><span class="sxs-lookup"><span data-stu-id="deba3-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**記錄問題** (112) </span><span class="sxs-lookup"><span data-stu-id="deba3-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>偵測到 (113) 的 **洩漏**</span><span class="sxs-lookup"><span data-stu-id="deba3-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**保護機制失敗** (114) </span><span class="sxs-lookup"><span data-stu-id="deba3-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 保護資源失敗** (115) </span><span class="sxs-lookup"><span data-stu-id="deba3-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**資料庫不一致** (116) </span><span class="sxs-lookup"><span data-stu-id="deba3-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**驗證失敗** (117) </span><span class="sxs-lookup"><span data-stu-id="deba3-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span> (118) **的機密性缺口**</span><span class="sxs-lookup"><span data-stu-id="deba3-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**纜線防** (119) </span><span class="sxs-lookup"><span data-stu-id="deba3-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**延遲的資訊** (120) </span><span class="sxs-lookup"><span data-stu-id="deba3-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**重複的資訊** (121) </span><span class="sxs-lookup"><span data-stu-id="deba3-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**遺漏** (122) 的資訊</span><span class="sxs-lookup"><span data-stu-id="deba3-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span> (123) 的 **資訊修改**</span><span class="sxs-lookup"><span data-stu-id="deba3-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**順序中的資訊** (124) </span><span class="sxs-lookup"><span data-stu-id="deba3-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**金鑰已過期** (125) </span><span class="sxs-lookup"><span data-stu-id="deba3-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**不可否認性失敗** (126) </span><span class="sxs-lookup"><span data-stu-id="deba3-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>下班 **時間活動** (127) </span><span class="sxs-lookup"><span data-stu-id="deba3-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**服務** (128) </span><span class="sxs-lookup"><span data-stu-id="deba3-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>程式 **錯誤** (129) </span><span class="sxs-lookup"><span data-stu-id="deba3-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="deba3-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>未 **預期的資訊** (130 ) </span><span class="sxs-lookup"><span data-stu-id="deba3-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="deba3-403">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="deba3-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-404">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="deba3-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="deba3-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-406">描述錯誤可能原因的字串。</span><span class="sxs-lookup"><span data-stu-id="deba3-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="deba3-407">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="deba3-408">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="deba3-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="deba3-409">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="deba3-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="deba3-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="deba3-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="deba3-411">描述要採取以解決錯誤之建議動作的字串。</span><span class="sxs-lookup"><span data-stu-id="deba3-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="deba3-412">這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="deba3-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="deba3-413">備註</span><span class="sxs-lookup"><span data-stu-id="deba3-413">Remarks</span></span>

<span data-ttu-id="deba3-414">**Msvm \_ 錯誤** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="deba3-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="deba3-415">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="deba3-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="deba3-416">規格需求</span><span class="sxs-lookup"><span data-stu-id="deba3-416">Requirements</span></span>



| <span data-ttu-id="deba3-417">需求</span><span class="sxs-lookup"><span data-stu-id="deba3-417">Requirement</span></span> | <span data-ttu-id="deba3-418">值</span><span class="sxs-lookup"><span data-stu-id="deba3-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deba3-419">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="deba3-419">Minimum supported client</span></span><br/> | <span data-ttu-id="deba3-420">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deba3-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="deba3-421">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="deba3-421">Minimum supported server</span></span><br/> | <span data-ttu-id="deba3-422">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deba3-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="deba3-423">命名空間</span><span class="sxs-lookup"><span data-stu-id="deba3-423">Namespace</span></span><br/>                | <span data-ttu-id="deba3-424">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="deba3-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="deba3-425">MOF</span><span class="sxs-lookup"><span data-stu-id="deba3-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="deba3-426"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="deba3-427">DLL</span><span class="sxs-lookup"><span data-stu-id="deba3-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deba3-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="deba3-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="deba3-429">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deba3-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deba3-430">**CIM \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="deba3-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="deba3-431">[**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="deba3-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="deba3-432">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="deba3-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

