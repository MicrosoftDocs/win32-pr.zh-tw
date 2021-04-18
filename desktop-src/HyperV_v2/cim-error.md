---
description: CIM \_ 錯誤類別包含 cim 作業失敗的相關資訊。
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318035"
---
# <a name="cim_error-class"></a><span data-ttu-id="c0717-103">CIM \_ 錯誤類別</span><span class="sxs-lookup"><span data-stu-id="c0717-103">CIM\_Error class</span></span>

<span data-ttu-id="c0717-104">**Cim \_ 錯誤** 類別包含 cim 作業失敗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c0717-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0717-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0717-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
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

## <a name="members"></a><span data-ttu-id="c0717-106">成員</span><span class="sxs-lookup"><span data-stu-id="c0717-106">Members</span></span>

<span data-ttu-id="c0717-107">**CIM \_ 錯誤** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0717-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="c0717-108">屬性</span><span class="sxs-lookup"><span data-stu-id="c0717-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0717-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c0717-109">Properties</span></span>

<span data-ttu-id="c0717-110">**CIM \_ 錯誤** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c0717-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0717-111">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="c0717-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-112">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0717-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-114">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DSP0201。DMTF \| 錯誤。代碼 \| 2.3 "，" DSP0200。DMTF \| CIMError \| 1.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**CIMStatusCodeDescription**") </span><span class="sxs-lookup"><span data-stu-id="c0717-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-115">此實例的特性的 CIM 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c0717-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="c0717-116">這個屬性會定義 CIM 伺服器或接聽程式可以傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c0717-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="c0717-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_錯誤 \_ 失敗** (1) </span><span class="sxs-lookup"><span data-stu-id="c0717-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-118">發生的一般錯誤未涵蓋于更明確的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0717-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="c0717-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_錯誤 \_ \_ 拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="c0717-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-120">用戶端無法使用 CIM 資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="c0717-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="c0717-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_錯誤 \_ 不正確 \_ 命名空間** (3) </span><span class="sxs-lookup"><span data-stu-id="c0717-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-122">目標命名空間不存在。</span><span class="sxs-lookup"><span data-stu-id="c0717-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="c0717-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_錯誤 \_ 不正確 \_ 參數** (4) </span><span class="sxs-lookup"><span data-stu-id="c0717-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-124">傳遞給方法的一或多個參數值無效。</span><span class="sxs-lookup"><span data-stu-id="c0717-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="c0717-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_錯誤 \_ 不正確 \_ 類別** (5) </span><span class="sxs-lookup"><span data-stu-id="c0717-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-126">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="c0717-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="c0717-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ (6) \_ \_ 找不到錯誤**</span><span class="sxs-lookup"><span data-stu-id="c0717-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-128">找不到要求的物件。</span><span class="sxs-lookup"><span data-stu-id="c0717-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="c0717-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ (7) \_ 不 \_ 支援的錯誤**</span><span class="sxs-lookup"><span data-stu-id="c0717-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-130">不支援要求的作業。</span><span class="sxs-lookup"><span data-stu-id="c0717-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="c0717-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ERR \_ 類別 \_ 具有 \_ 子** 系 (8) </span><span class="sxs-lookup"><span data-stu-id="c0717-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-132">無法在這個類別上執行操作，因為它有實例。</span><span class="sxs-lookup"><span data-stu-id="c0717-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="c0717-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ERR \_ 類別 \_ 具有 \_ 實例** (9) </span><span class="sxs-lookup"><span data-stu-id="c0717-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-134">無法在這個類別上執行操作，因為它有實例。</span><span class="sxs-lookup"><span data-stu-id="c0717-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="c0717-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_錯誤 \_ 不正確 \_ 超類** (10) </span><span class="sxs-lookup"><span data-stu-id="c0717-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-136">因為指定的超類別不存在，所以無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c0717-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="c0717-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_錯誤 \_ 已經 \_ 存在** (11) </span><span class="sxs-lookup"><span data-stu-id="c0717-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-138">無法執行操作，因為物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="c0717-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="c0717-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_錯誤 (12) 不會有 \_ \_ 此 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="c0717-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-140">指定的屬性不存在。</span><span class="sxs-lookup"><span data-stu-id="c0717-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="c0717-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_錯誤 \_ 類型 \_ 不符** (13) </span><span class="sxs-lookup"><span data-stu-id="c0717-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-142">提供的值與類型不相容。</span><span class="sxs-lookup"><span data-stu-id="c0717-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="c0717-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_\_ \_ \_ 不 \_ 支援** (14) 的 ERR 查詢語言</span><span class="sxs-lookup"><span data-stu-id="c0717-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-144">無法辨識或支援查詢語言。</span><span class="sxs-lookup"><span data-stu-id="c0717-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="c0717-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_錯誤 \_ 不正確 \_ 查詢** (15) </span><span class="sxs-lookup"><span data-stu-id="c0717-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-146">查詢對指定的查詢語言無效。</span><span class="sxs-lookup"><span data-stu-id="c0717-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="c0717-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ (16) \_ \_ 無法 \_ 使用 ERR 方法**</span><span class="sxs-lookup"><span data-stu-id="c0717-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-148">無法執行外部方法。</span><span class="sxs-lookup"><span data-stu-id="c0717-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="c0717-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_\_ \_ \_ 找不到** (17) 的 ERR 方法</span><span class="sxs-lookup"><span data-stu-id="c0717-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-150">指定的外部方法不存在。</span><span class="sxs-lookup"><span data-stu-id="c0717-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="c0717-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_錯誤的非 \_ 預期 \_ 回應** (18) </span><span class="sxs-lookup"><span data-stu-id="c0717-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-152">對非同步作業所傳回的回應不是預期的。</span><span class="sxs-lookup"><span data-stu-id="c0717-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="c0717-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_錯誤 \_ 不正確 \_ 回應 \_ 目的地** (19) </span><span class="sxs-lookup"><span data-stu-id="c0717-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-154">非同步回應的指定目的地無效。</span><span class="sxs-lookup"><span data-stu-id="c0717-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="c0717-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_錯誤 \_ 命名空間 \_ 不是 \_ 空** 的 (20) </span><span class="sxs-lookup"><span data-stu-id="c0717-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-156">指定的命名空間不是空的。</span><span class="sxs-lookup"><span data-stu-id="c0717-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="c0717-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_錯誤 \_ 不正確 \_ 列舉 \_ 內容** (21) </span><span class="sxs-lookup"><span data-stu-id="c0717-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-158">提供的列舉內容無效。</span><span class="sxs-lookup"><span data-stu-id="c0717-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="c0717-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_錯誤 \_ 無效 \_ \_** 的作業超時 (22) </span><span class="sxs-lookup"><span data-stu-id="c0717-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-160">指定的命名空間不是空的。</span><span class="sxs-lookup"><span data-stu-id="c0717-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="c0717-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_\_ \_ \_ 已 \_ 放棄 (23) 的錯誤提取**</span><span class="sxs-lookup"><span data-stu-id="c0717-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-162">指定的命名空間不是空的。</span><span class="sxs-lookup"><span data-stu-id="c0717-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="c0717-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_\_ \_ 無法 \_ \_ 放棄** (24) 的錯誤提取</span><span class="sxs-lookup"><span data-stu-id="c0717-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-164">嘗試放棄提取作業失敗。</span><span class="sxs-lookup"><span data-stu-id="c0717-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="c0717-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ (25) \_ \_ \_ 不 \_ 支援錯誤篩選的列舉**</span><span class="sxs-lookup"><span data-stu-id="c0717-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-166">不支援篩選的 Enumeratrions。</span><span class="sxs-lookup"><span data-stu-id="c0717-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="c0717-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_\_ \_ \_ 錯誤 \_ 不 \_ 支援錯誤接續** (26) </span><span class="sxs-lookup"><span data-stu-id="c0717-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-168">不支援發生錯誤時仍繼續。</span><span class="sxs-lookup"><span data-stu-id="c0717-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="c0717-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ (27) \_ \_ \_ 超過 ERR 伺服器限制**</span><span class="sxs-lookup"><span data-stu-id="c0717-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-170">已超過 WBEM 伺服器限制 (例如記憶體、連線 ... ) 。</span><span class="sxs-lookup"><span data-stu-id="c0717-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="c0717-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ERR \_ 伺服器 \_ 正在 \_ 關閉 \_** (28) </span><span class="sxs-lookup"><span data-stu-id="c0717-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-172">WBEM 伺服器正在關閉。</span><span class="sxs-lookup"><span data-stu-id="c0717-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="c0717-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_\_ \_ \_ 不 \_ 支援** (29) 的 ERR 查詢功能</span><span class="sxs-lookup"><span data-stu-id="c0717-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-174">不支援指定的查詢功能。</span><span class="sxs-lookup"><span data-stu-id="c0717-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c0717-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c0717-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0717-176">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="c0717-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-179">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DSP0201。DMTF \| 錯誤。描述 \| 2.3 "，" DSP0200。DMTF \| CIMError \| 1.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**CIMStatusCode**") </span><span class="sxs-lookup"><span data-stu-id="c0717-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-180">自由格式的字串，其中包含人類可讀取的 **CIMStatusCode** 屬性值描述。</span><span class="sxs-lookup"><span data-stu-id="c0717-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="c0717-181">這項描述可能會延伸，但必須與 **CIMStatusCode** 的定義一致。</span><span class="sxs-lookup"><span data-stu-id="c0717-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="c0717-182">**ErrorSource**</span><span class="sxs-lookup"><span data-stu-id="c0717-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-185">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSourceFormat**") </span><span class="sxs-lookup"><span data-stu-id="c0717-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-186">識別產生錯誤之實體的資訊。</span><span class="sxs-lookup"><span data-stu-id="c0717-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="c0717-187">如果實體是由 CIM 架構模型化，則這個屬性會包含編碼為字串參數之實例的路徑。</span><span class="sxs-lookup"><span data-stu-id="c0717-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="c0717-188">否則，屬性會包含一個字串，該字串會為產生錯誤的實體命名。</span><span class="sxs-lookup"><span data-stu-id="c0717-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="c0717-189">這個屬性的格式是由 **ErrorSourceFormat** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="c0717-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="c0717-190">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="c0717-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0717-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-193">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSource**"，"**CIM \_ 錯誤**。**OtherErrorSourceFormat**") </span><span class="sxs-lookup"><span data-stu-id="c0717-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-194">**ErrorSource** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="c0717-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0717-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0717-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-196">CIM 用戶端應用程式可解譯的格式不明或不具意義。</span><span class="sxs-lookup"><span data-stu-id="c0717-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0717-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0717-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-198">格式是由 **OtherErrorSourceFormat** 屬性的值所定義。</span><span class="sxs-lookup"><span data-stu-id="c0717-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="c0717-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) </span><span class="sxs-lookup"><span data-stu-id="c0717-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-200">Cim 基礎結構規格中定義的 CIM 物件路徑。</span><span class="sxs-lookup"><span data-stu-id="c0717-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c0717-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c0717-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0717-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="c0717-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0717-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-205">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**OtherErrorType**") </span><span class="sxs-lookup"><span data-stu-id="c0717-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-206">主要錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="c0717-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0717-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0717-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0717-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0717-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="c0717-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**通訊錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="c0717-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-210">此類型的錯誤主要與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0717-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="c0717-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**服務品質錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="c0717-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-212">這種類型的錯誤主要與導致功能或效能降低的失敗有關。</span><span class="sxs-lookup"><span data-stu-id="c0717-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="c0717-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**軟體錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="c0717-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-214">此類型的錯誤主要與軟體或處理錯誤相關。</span><span class="sxs-lookup"><span data-stu-id="c0717-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="c0717-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**硬體錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="c0717-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-216">此類型的錯誤主要與設備或硬體故障相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0717-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="c0717-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**環境錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="c0717-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-218">其他環境考慮。</span><span class="sxs-lookup"><span data-stu-id="c0717-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="c0717-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**安全性錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="c0717-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-220">此類型的錯誤與安全性違規、病毒偵測和類似問題相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0717-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="c0717-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**過度訂閱錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="c0717-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-222">此類型的錯誤主要與失敗相關，無法配置足夠的資源來完成作業。</span><span class="sxs-lookup"><span data-stu-id="c0717-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="c0717-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**無法使用資源錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="c0717-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-224">此類型的錯誤主要與無法存取所需資源的相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0717-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="c0717-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span> (10) **不支援** 的作業錯誤</span><span class="sxs-lookup"><span data-stu-id="c0717-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-226">此類型的錯誤主要與不支援的要求相關聯。</span><span class="sxs-lookup"><span data-stu-id="c0717-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c0717-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c0717-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0717-228">**訊息**</span><span class="sxs-lookup"><span data-stu-id="c0717-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-231">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**MessageID**"，"**CIM \_ 錯誤**。**MessageArguments**") </span><span class="sxs-lookup"><span data-stu-id="c0717-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-232">格式化的訊息。</span><span class="sxs-lookup"><span data-stu-id="c0717-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="c0717-233">這則訊息是藉由將 **MessageArguments** 屬性的動態元素與 **MessageID** 屬性的靜態元素結合，然後將它們新增至與 **OwningEntity** 相關聯的訊息登錄或目錄來建立。</span><span class="sxs-lookup"><span data-stu-id="c0717-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="c0717-234">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="c0717-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-235">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0717-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0717-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-237">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**MessageID**"，"**CIM \_ 錯誤**。**訊息**「) </span><span class="sxs-lookup"><span data-stu-id="c0717-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-238">陣列，其中包含訊息的動態內容。</span><span class="sxs-lookup"><span data-stu-id="c0717-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="c0717-239">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="c0717-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-242">限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ Error**.**Message**"，"**CIM \_ 錯誤**。**MessageArguments**") </span><span class="sxs-lookup"><span data-stu-id="c0717-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-243">在 OwningEntity 範圍內唯一識別的不透明字串，這是訊息的格式。</span><span class="sxs-lookup"><span data-stu-id="c0717-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="c0717-244">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="c0717-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-247">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSourceFormat**") </span><span class="sxs-lookup"><span data-stu-id="c0717-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-248">當 **ErrorSourceFormat** 設定為 "1" (其他) 時，定義 **ErrorSourceFormat** 值的字串。</span><span class="sxs-lookup"><span data-stu-id="c0717-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="c0717-249">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="c0717-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-252">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorType**") </span><span class="sxs-lookup"><span data-stu-id="c0717-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-253">描述 **ErrorType** 值的自由格式字串，其設定為 "1" (其他) 。</span><span class="sxs-lookup"><span data-stu-id="c0717-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="c0717-254">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="c0717-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0717-257">擁有此實例所描述的訊息格式之實體的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0717-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="c0717-258">這個屬性必須包含受著作權、商標或唯一的名稱，該名稱是由定義訊息格式的商務實體或標準主體所擁有。</span><span class="sxs-lookup"><span data-stu-id="c0717-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="c0717-259">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="c0717-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-260">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0717-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-262">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) </span><span class="sxs-lookup"><span data-stu-id="c0717-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-263">從傳送錯誤訊息之元素的觀點來看，錯誤嚴重性的描述。</span><span class="sxs-lookup"><span data-stu-id="c0717-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0717-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0717-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-265">已知的指示嚴重性不明或不定。</span><span class="sxs-lookup"><span data-stu-id="c0717-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0717-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0717-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-267">表示可以在 **OtherSeverity** 屬性中找到嚴重性的值。</span><span class="sxs-lookup"><span data-stu-id="c0717-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="c0717-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) </span><span class="sxs-lookup"><span data-stu-id="c0717-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-269">提供資訊性回應時應使用資訊。</span><span class="sxs-lookup"><span data-stu-id="c0717-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="c0717-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) </span><span class="sxs-lookup"><span data-stu-id="c0717-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-271">如果適合讓使用者決定是否需要採取動作，則應該使用。</span><span class="sxs-lookup"><span data-stu-id="c0717-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="c0717-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) </span><span class="sxs-lookup"><span data-stu-id="c0717-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-273">需要採取動作，但這次的情況並不嚴重。</span><span class="sxs-lookup"><span data-stu-id="c0717-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="c0717-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) </span><span class="sxs-lookup"><span data-stu-id="c0717-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-275">現在需要採取動作。</span><span class="sxs-lookup"><span data-stu-id="c0717-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c0717-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) </span><span class="sxs-lookup"><span data-stu-id="c0717-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-277">現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。</span><span class="sxs-lookup"><span data-stu-id="c0717-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="c0717-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) </span><span class="sxs-lookup"><span data-stu-id="c0717-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0717-279">發生錯誤，但太晚採取補救動作。</span><span class="sxs-lookup"><span data-stu-id="c0717-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c0717-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c0717-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0717-281">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="c0717-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-282">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c0717-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-284">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。可能的原因 "，" \| M3100. probableCause "，" itu-IANA-鬧鐘-TC ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**ProbableCauseDescription**") </span><span class="sxs-lookup"><span data-stu-id="c0717-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-285">錯誤可能原因的描述。</span><span class="sxs-lookup"><span data-stu-id="c0717-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0717-286">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c0717-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0717-287">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c0717-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="c0717-288">**介面卡/卡片錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="c0717-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="c0717-289">**應用程式子系統失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="c0717-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="c0717-290">**頻寬減少** (4) </span><span class="sxs-lookup"><span data-stu-id="c0717-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="c0717-291">**連接建立錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="c0717-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="c0717-292">**通訊協定錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="c0717-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="c0717-293">**通訊子系統失敗** (7) </span><span class="sxs-lookup"><span data-stu-id="c0717-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="c0717-294">設定 **/自訂錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="c0717-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="c0717-295">**擁塞** (9) </span><span class="sxs-lookup"><span data-stu-id="c0717-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="c0717-296">**已** 損毀的資料 (10) </span><span class="sxs-lookup"><span data-stu-id="c0717-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="c0717-297">**CPU 週期限制超過** (11) </span><span class="sxs-lookup"><span data-stu-id="c0717-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="c0717-298">**資料集/數據機錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c0717-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="c0717-299">**降級的信號** (13) </span><span class="sxs-lookup"><span data-stu-id="c0717-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="c0717-300">**DTE-DCE 介面錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="c0717-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="c0717-301">**主機殼門開啟** (15) </span><span class="sxs-lookup"><span data-stu-id="c0717-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="c0717-302">**設備故障** (16) </span><span class="sxs-lookup"><span data-stu-id="c0717-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="c0717-303">**過度震動** (17) </span><span class="sxs-lookup"><span data-stu-id="c0717-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="c0717-304">**檔案格式錯誤** (18) </span><span class="sxs-lookup"><span data-stu-id="c0717-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="c0717-305">**引發偵測到** (19) </span><span class="sxs-lookup"><span data-stu-id="c0717-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="c0717-306">偵測 **到大量** (20) </span><span class="sxs-lookup"><span data-stu-id="c0717-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="c0717-307">**框架錯誤** (21) </span><span class="sxs-lookup"><span data-stu-id="c0717-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="c0717-308">**HVAC 問題** (22) </span><span class="sxs-lookup"><span data-stu-id="c0717-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="c0717-309">不 **接受濕度** (23) </span><span class="sxs-lookup"><span data-stu-id="c0717-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="c0717-310">**I/o 裝置錯誤** (24) </span><span class="sxs-lookup"><span data-stu-id="c0717-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="c0717-311">**輸入裝置錯誤** (25) </span><span class="sxs-lookup"><span data-stu-id="c0717-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="c0717-312">**區域網路錯誤** (26) </span><span class="sxs-lookup"><span data-stu-id="c0717-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="c0717-313">偵測 **到未有毒的** 流失 (27) </span><span class="sxs-lookup"><span data-stu-id="c0717-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="c0717-314">**本機節點傳輸錯誤** (28) </span><span class="sxs-lookup"><span data-stu-id="c0717-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="c0717-315">**遺失框架** (29) </span><span class="sxs-lookup"><span data-stu-id="c0717-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="c0717-316"> (30) **的信號遺失**</span><span class="sxs-lookup"><span data-stu-id="c0717-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="c0717-317">**物料供應已用盡** (31) </span><span class="sxs-lookup"><span data-stu-id="c0717-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="c0717-318">多工器 **問題** (32) </span><span class="sxs-lookup"><span data-stu-id="c0717-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="c0717-319">**記憶體不足** (33) </span><span class="sxs-lookup"><span data-stu-id="c0717-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="c0717-320">**輸出裝置錯誤** (34) </span><span class="sxs-lookup"><span data-stu-id="c0717-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="c0717-321">**效能降低** (35) </span><span class="sxs-lookup"><span data-stu-id="c0717-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="c0717-322">**電源問題** (36) </span><span class="sxs-lookup"><span data-stu-id="c0717-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="c0717-323">**不可接受的壓力** (37) </span><span class="sxs-lookup"><span data-stu-id="c0717-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="c0717-324">**處理器問題 (內部電腦錯誤)** (38) </span><span class="sxs-lookup"><span data-stu-id="c0717-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="c0717-325">提取 **失敗** (39) </span><span class="sxs-lookup"><span data-stu-id="c0717-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="c0717-326">**佇列大小超過** (40) </span><span class="sxs-lookup"><span data-stu-id="c0717-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="c0717-327">**接收失敗** (41) </span><span class="sxs-lookup"><span data-stu-id="c0717-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="c0717-328">**接收者失敗** (42) </span><span class="sxs-lookup"><span data-stu-id="c0717-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="c0717-329">**遠端節點傳輸錯誤** (43) </span><span class="sxs-lookup"><span data-stu-id="c0717-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="c0717-330">**資源或接近容量** (44) </span><span class="sxs-lookup"><span data-stu-id="c0717-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="c0717-331">**回應時間過度** (45) </span><span class="sxs-lookup"><span data-stu-id="c0717-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="c0717-332">重新 **傳輸速率過高** (46) </span><span class="sxs-lookup"><span data-stu-id="c0717-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="c0717-333">**軟體錯誤** (47) </span><span class="sxs-lookup"><span data-stu-id="c0717-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="c0717-334">**軟體程式異常終止** (48) </span><span class="sxs-lookup"><span data-stu-id="c0717-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="c0717-335">**軟體程式錯誤 (不正確的結果)** (49) </span><span class="sxs-lookup"><span data-stu-id="c0717-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="c0717-336">**儲存體容量問題** (50) </span><span class="sxs-lookup"><span data-stu-id="c0717-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="c0717-337">無法 **接受的溫度** (51) </span><span class="sxs-lookup"><span data-stu-id="c0717-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="c0717-338">**超過** (52) 的閾值</span><span class="sxs-lookup"><span data-stu-id="c0717-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="c0717-339">**計時問題** (53) </span><span class="sxs-lookup"><span data-stu-id="c0717-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="c0717-340">偵測 **到有毒** 流失 (54) </span><span class="sxs-lookup"><span data-stu-id="c0717-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="c0717-341">**傳輸失敗** (55) </span><span class="sxs-lookup"><span data-stu-id="c0717-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="c0717-342">**發送器失敗** (56) </span><span class="sxs-lookup"><span data-stu-id="c0717-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="c0717-343">**基礎資源無法使用** (57) </span><span class="sxs-lookup"><span data-stu-id="c0717-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="c0717-344">**版本不相符** (58) </span><span class="sxs-lookup"><span data-stu-id="c0717-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="c0717-345">**先前的警示已清除** (59) </span><span class="sxs-lookup"><span data-stu-id="c0717-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="c0717-346">**登入嘗試失敗** (60) </span><span class="sxs-lookup"><span data-stu-id="c0717-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="c0717-347">偵測 **到的軟體病毒** (61) </span><span class="sxs-lookup"><span data-stu-id="c0717-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="c0717-348">**硬體安全性違反** 了 (62) </span><span class="sxs-lookup"><span data-stu-id="c0717-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="c0717-349">偵測 **到拒絕服務** (63) </span><span class="sxs-lookup"><span data-stu-id="c0717-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="c0717-350">**安全性認證不符** (64) </span><span class="sxs-lookup"><span data-stu-id="c0717-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="c0717-351">**未經授權的存取** (65) </span><span class="sxs-lookup"><span data-stu-id="c0717-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="c0717-352">**已收到** (66) 的鬧鐘</span><span class="sxs-lookup"><span data-stu-id="c0717-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="c0717-353">**遺失指標** (67) </span><span class="sxs-lookup"><span data-stu-id="c0717-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="c0717-354">承載 **不符** (68) </span><span class="sxs-lookup"><span data-stu-id="c0717-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="c0717-355">**傳輸錯誤** (69) </span><span class="sxs-lookup"><span data-stu-id="c0717-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="c0717-356">**過多錯誤率** (70) </span><span class="sxs-lookup"><span data-stu-id="c0717-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="c0717-357">**追蹤問題** (71) </span><span class="sxs-lookup"><span data-stu-id="c0717-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="c0717-358">**元素無法使用** (72) </span><span class="sxs-lookup"><span data-stu-id="c0717-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="c0717-359">**遺漏的元素** (73) </span><span class="sxs-lookup"><span data-stu-id="c0717-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="c0717-360">**遺失多框架** (74) </span><span class="sxs-lookup"><span data-stu-id="c0717-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="c0717-361">**廣播通道失敗** (75) </span><span class="sxs-lookup"><span data-stu-id="c0717-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="c0717-362">**收到的訊息無效** (76) </span><span class="sxs-lookup"><span data-stu-id="c0717-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="c0717-363">**路由失敗** (77) </span><span class="sxs-lookup"><span data-stu-id="c0717-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="c0717-364">**背板失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="c0717-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="c0717-365">**識別碼重複** (79) </span><span class="sxs-lookup"><span data-stu-id="c0717-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="c0717-366">**保護路徑失敗** (80) </span><span class="sxs-lookup"><span data-stu-id="c0717-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="c0717-367">**同步遺失或** (81) 不相符</span><span class="sxs-lookup"><span data-stu-id="c0717-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="c0717-368">**終端機問題** (82) </span><span class="sxs-lookup"><span data-stu-id="c0717-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="c0717-369">**系統時鐘失敗** (83) </span><span class="sxs-lookup"><span data-stu-id="c0717-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="c0717-370">**天線失敗** (84) </span><span class="sxs-lookup"><span data-stu-id="c0717-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="c0717-371">**電池充電失敗** (85) </span><span class="sxs-lookup"><span data-stu-id="c0717-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="c0717-372">**磁片失敗** (86) </span><span class="sxs-lookup"><span data-stu-id="c0717-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="c0717-373">**頻率跳動失敗** (87) </span><span class="sxs-lookup"><span data-stu-id="c0717-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="c0717-374">**遺失冗余** (88) </span><span class="sxs-lookup"><span data-stu-id="c0717-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="c0717-375">**電源供應器失敗** (89) </span><span class="sxs-lookup"><span data-stu-id="c0717-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="c0717-376">**信號品質問題** (90) </span><span class="sxs-lookup"><span data-stu-id="c0717-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="c0717-377">**電池放電** (91) </span><span class="sxs-lookup"><span data-stu-id="c0717-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="c0717-378">**電池故障** (92) </span><span class="sxs-lookup"><span data-stu-id="c0717-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="c0717-379">**商業電源問題** (93) </span><span class="sxs-lookup"><span data-stu-id="c0717-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="c0717-380">**風扇故障** (94) </span><span class="sxs-lookup"><span data-stu-id="c0717-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="c0717-381">**引擎失敗** (95) </span><span class="sxs-lookup"><span data-stu-id="c0717-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="c0717-382">**感應器失敗** (96) </span><span class="sxs-lookup"><span data-stu-id="c0717-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="c0717-383">**保險絲故障** (97) </span><span class="sxs-lookup"><span data-stu-id="c0717-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="c0717-384">產生器 **失敗** (98) </span><span class="sxs-lookup"><span data-stu-id="c0717-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="c0717-385">**電力偏低** (99) </span><span class="sxs-lookup"><span data-stu-id="c0717-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="c0717-386">**低燃料** (100) </span><span class="sxs-lookup"><span data-stu-id="c0717-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="c0717-387">**低水位** (101) </span><span class="sxs-lookup"><span data-stu-id="c0717-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="c0717-388">**爆炸性天然氣** (102) </span><span class="sxs-lookup"><span data-stu-id="c0717-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="c0717-389">**高接近尾聲** (103) </span><span class="sxs-lookup"><span data-stu-id="c0717-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="c0717-390">**Ice 堆積** (104) </span><span class="sxs-lookup"><span data-stu-id="c0717-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="c0717-391">**冒煙** (105) </span><span class="sxs-lookup"><span data-stu-id="c0717-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="c0717-392">**記憶體不符** (106) </span><span class="sxs-lookup"><span data-stu-id="c0717-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="c0717-393">**CPU 週期** (107) </span><span class="sxs-lookup"><span data-stu-id="c0717-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="c0717-394">**軟體環境問題** (108) </span><span class="sxs-lookup"><span data-stu-id="c0717-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="c0717-395">**軟體下載失敗** (109) </span><span class="sxs-lookup"><span data-stu-id="c0717-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="c0717-396">**元素重新初始化** (110) </span><span class="sxs-lookup"><span data-stu-id="c0717-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="c0717-397">**Timeout** (111) </span><span class="sxs-lookup"><span data-stu-id="c0717-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="c0717-398">**記錄問題** (112) </span><span class="sxs-lookup"><span data-stu-id="c0717-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="c0717-399">偵測到 (113) 的 **洩漏**</span><span class="sxs-lookup"><span data-stu-id="c0717-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="c0717-400">**保護機制失敗** (114) </span><span class="sxs-lookup"><span data-stu-id="c0717-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="c0717-401">**保護資源失敗** (115) </span><span class="sxs-lookup"><span data-stu-id="c0717-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="c0717-402">**資料庫不一致** (116) </span><span class="sxs-lookup"><span data-stu-id="c0717-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="c0717-403">**驗證失敗** (117) </span><span class="sxs-lookup"><span data-stu-id="c0717-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="c0717-404"> (118) **的機密性缺口**</span><span class="sxs-lookup"><span data-stu-id="c0717-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="c0717-405">**纜線防** (119) </span><span class="sxs-lookup"><span data-stu-id="c0717-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="c0717-406">**延遲的資訊** (120) </span><span class="sxs-lookup"><span data-stu-id="c0717-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="c0717-407">**重複的資訊** (121) </span><span class="sxs-lookup"><span data-stu-id="c0717-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="c0717-408">**遺漏** (122) 的資訊</span><span class="sxs-lookup"><span data-stu-id="c0717-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="c0717-409"> (123) 的 **資訊修改**</span><span class="sxs-lookup"><span data-stu-id="c0717-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="c0717-410">**順序中的資訊** (124) </span><span class="sxs-lookup"><span data-stu-id="c0717-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="c0717-411">**金鑰已過期** (125) </span><span class="sxs-lookup"><span data-stu-id="c0717-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="c0717-412">**不可否認性失敗** (126) </span><span class="sxs-lookup"><span data-stu-id="c0717-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="c0717-413">下班 **時間活動** (127) </span><span class="sxs-lookup"><span data-stu-id="c0717-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="c0717-414">**服務** (128) </span><span class="sxs-lookup"><span data-stu-id="c0717-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="c0717-415">程式 **錯誤** (129) </span><span class="sxs-lookup"><span data-stu-id="c0717-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="c0717-416">未 **預期的資訊** (130) </span><span class="sxs-lookup"><span data-stu-id="c0717-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c0717-417">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c0717-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0717-418">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="c0717-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-419">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c0717-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0717-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0717-421">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ProbableCause**") </span><span class="sxs-lookup"><span data-stu-id="c0717-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="c0717-422">描述錯誤可能原因的自由格式字串（當 **ProbableCause** 屬性設定為 "1" (其他) 時）。</span><span class="sxs-lookup"><span data-stu-id="c0717-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="c0717-423">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="c0717-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0717-424">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c0717-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c0717-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c0717-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0717-426">自由格式字串的陣列，描述解決錯誤所採取的建議動作。</span><span class="sxs-lookup"><span data-stu-id="c0717-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0717-427">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0717-427">Requirements</span></span>



| <span data-ttu-id="c0717-428">需求</span><span class="sxs-lookup"><span data-stu-id="c0717-428">Requirement</span></span> | <span data-ttu-id="c0717-429">值</span><span class="sxs-lookup"><span data-stu-id="c0717-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0717-430">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0717-430">Minimum supported client</span></span><br/> | <span data-ttu-id="c0717-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c0717-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c0717-432">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0717-432">Minimum supported server</span></span><br/> | <span data-ttu-id="c0717-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0717-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c0717-434">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0717-434">Namespace</span></span><br/>                | <span data-ttu-id="c0717-435">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0717-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0717-436">MOF</span><span class="sxs-lookup"><span data-stu-id="c0717-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0717-437"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c0717-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0717-438">DLL</span><span class="sxs-lookup"><span data-stu-id="c0717-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0717-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0717-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

