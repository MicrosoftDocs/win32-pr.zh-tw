---
description: 執行查詢以擷取物件。
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecQueryAsync 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5564e53ef3ea185235e93bbbeb8e2a5fa001d67b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318856"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="c0fe9-103">SWbemServices.ExecQueryAsync 方法</span><span class="sxs-lookup"><span data-stu-id="c0fe9-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="c0fe9-104">[**SWbemServices**](swbemservices.md)物件的 **ExecQueryAsync** 方法會執行查詢來取出物件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="c0fe9-105">這個方法的呼叫會立即傳回，而結果和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c0fe9-106">若要處理每個傳回的物件，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="c0fe9-107">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="c0fe9-108">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c0fe9-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fe9-110">語法</span><span class="sxs-lookup"><span data-stu-id="c0fe9-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c0fe9-111">參數</span><span class="sxs-lookup"><span data-stu-id="c0fe9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0fe9-112">*objWbemSink* \[選\]</span><span class="sxs-lookup"><span data-stu-id="c0fe9-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-113">以非同步方式執行查詢的物件接收。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="c0fe9-114">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="c0fe9-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="c0fe9-116">必要。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-116">Required.</span></span> <span data-ttu-id="c0fe9-117">包含查詢文字的字串。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-117">String that contains the text of the query.</span></span> <span data-ttu-id="c0fe9-118">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-118">This parameter cannot be blank.</span></span> <span data-ttu-id="c0fe9-119">如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-120">*strQueryLanguage* \[選\]</span><span class="sxs-lookup"><span data-stu-id="c0fe9-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-121">字串，包含要使用的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-121">String that contains the query language to be used.</span></span> <span data-ttu-id="c0fe9-122">如果有指定，此值必須是 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-123">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="c0fe9-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-124">判斷查詢行為的整數。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="c0fe9-125">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c0fe9-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c0fe9-127">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c0fe9-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c0fe9-129">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="c0fe9-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="c0fe9-131">用於原型。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-131">Used for a prototype.</span></span> <span data-ttu-id="c0fe9-132">它會停止進行查詢，而會傳回類似一般結果物件的物件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c0fe9-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c0fe9-134">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="c0fe9-135">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0fe9-136">*objwbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="c0fe9-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-137">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-137">Typically, this is undefined.</span></span> <span data-ttu-id="c0fe9-138">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="c0fe9-139">支援或需要內容資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-140">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="c0fe9-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-141">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c0fe9-142">使用這個參數可使用相同的物件接收進行多個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c0fe9-143">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c0fe9-144">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c0fe9-145">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0fe9-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0fe9-146">Return value</span></span>

<span data-ttu-id="c0fe9-147">這個方法沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-147">This method has no return values.</span></span> <span data-ttu-id="c0fe9-148">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="c0fe9-149">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0fe9-150">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c0fe9-150">Error codes</span></span>

<span data-ttu-id="c0fe9-151">**ExecQueryAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可以包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c0fe9-152">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-153">目前的使用者沒有許可權可查看結果集。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-154">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-155">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-156">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-157">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-158">**wbemErrInvalidQuery** -2147749911 (0x80041017) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-159">查詢語法無效。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-161">不支援要求的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c0fe9-162">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="c0fe9-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c0fe9-163">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0fe9-164">備註</span><span class="sxs-lookup"><span data-stu-id="c0fe9-164">Remarks</span></span>

<span data-ttu-id="c0fe9-165">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-165">This call returns immediately.</span></span> <span data-ttu-id="c0fe9-166">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c0fe9-167">若要在每個物件返回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="c0fe9-168">傳回所有物件之後，請在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="c0fe9-169">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c0fe9-170">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c0fe9-171">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="c0fe9-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="c0fe9-172">當沒有任何物件符合查詢中的條件時， **ExecQueryAsync** 方法會傳回空的結果集。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="c0fe9-173">無論是否在 *strQuery* 參數中要求索引 [**鍵**](standard-qualifiers.md)屬性，這個方法都會傳回索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="c0fe9-174">WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="c0fe9-175">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 WBEM \_ E \_ 配額 \_ 違規錯誤碼傳回為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="c0fe9-176">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="c0fe9-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0fe9-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0fe9-177">Requirements</span></span>



| <span data-ttu-id="c0fe9-178">需求</span><span class="sxs-lookup"><span data-stu-id="c0fe9-178">Requirement</span></span> | <span data-ttu-id="c0fe9-179">值</span><span class="sxs-lookup"><span data-stu-id="c0fe9-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fe9-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0fe9-180">Minimum supported client</span></span><br/> | <span data-ttu-id="c0fe9-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0fe9-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0fe9-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0fe9-182">Minimum supported server</span></span><br/> | <span data-ttu-id="c0fe9-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0fe9-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0fe9-184">標頭</span><span class="sxs-lookup"><span data-stu-id="c0fe9-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0fe9-185"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fe9-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0fe9-186">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c0fe9-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0fe9-187"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0fe9-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0fe9-188">DLL</span><span class="sxs-lookup"><span data-stu-id="c0fe9-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0fe9-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0fe9-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0fe9-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="c0fe9-190">CLSID</span></span><br/>                    | <span data-ttu-id="c0fe9-191">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="c0fe9-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="c0fe9-192">IID</span><span class="sxs-lookup"><span data-stu-id="c0fe9-192">IID</span></span><br/>                      | <span data-ttu-id="c0fe9-193">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="c0fe9-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c0fe9-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0fe9-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0fe9-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="c0fe9-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="c0fe9-196">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="c0fe9-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="c0fe9-197">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="c0fe9-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

