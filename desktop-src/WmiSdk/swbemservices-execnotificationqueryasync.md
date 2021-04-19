---
description: 執行查詢以接收事件。
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecNotificationQueryAsync 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996655"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="454f4-103">SWbemServices.ExecNotificationQueryAsync 方法</span><span class="sxs-lookup"><span data-stu-id="454f4-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="454f4-104">[**SWbemServices**](swbemservices.md)物件的 **ExecNotificationQueryAsync** 方法會執行查詢來接收事件。</span><span class="sxs-lookup"><span data-stu-id="454f4-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="454f4-105">這個呼叫會立即傳回，而結果和狀態會透過傳遞給 *objWbemSink* 中指定之接收的事件傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="454f4-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="454f4-106">查詢中指定的事件可以是內建的 Windows Management Instrumentation (WMI) 事件（例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)）或內建事件（例如 [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)或 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)）。</span><span class="sxs-lookup"><span data-stu-id="454f4-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="454f4-107">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="454f4-108">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="454f4-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="454f4-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="454f4-110">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="454f4-111">語法</span><span class="sxs-lookup"><span data-stu-id="454f4-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="454f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="454f4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="454f4-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="454f4-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="454f4-114">必要。</span><span class="sxs-lookup"><span data-stu-id="454f4-114">Required.</span></span> <span data-ttu-id="454f4-115">接收非同步事件通知的物件接收。</span><span class="sxs-lookup"><span data-stu-id="454f4-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="454f4-116">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="454f4-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-117">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="454f4-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="454f4-118">必要。</span><span class="sxs-lookup"><span data-stu-id="454f4-118">Required.</span></span> <span data-ttu-id="454f4-119">包含事件相關查詢之文字的字串。</span><span class="sxs-lookup"><span data-stu-id="454f4-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="454f4-120">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="454f4-120">This parameter cannot be blank.</span></span> <span data-ttu-id="454f4-121">如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="454f4-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-122">*strQueryLanguage* \[選\]</span><span class="sxs-lookup"><span data-stu-id="454f4-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="454f4-123">字串，包含要使用的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="454f4-123">String that contains the query language to be used.</span></span> <span data-ttu-id="454f4-124">如果有指定，此值必須是 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="454f4-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="454f4-125">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="454f4-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="454f4-126">判斷查詢行為的整數。</span><span class="sxs-lookup"><span data-stu-id="454f4-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="454f4-127">這個參數可以設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="454f4-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="454f4-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="454f4-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="454f4-129">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="454f4-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="454f4-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="454f4-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="454f4-131">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="454f4-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="454f4-132">*objwbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="454f4-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="454f4-133">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="454f4-133">Typically, this is undefined.</span></span> <span data-ttu-id="454f4-134">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="454f4-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="454f4-135">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="454f4-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-136">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="454f4-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="454f4-137">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="454f4-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="454f4-138">使用這個參數可使用相同的物件接收進行多個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="454f4-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="454f4-139">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="454f4-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="454f4-140">**SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md)方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="454f4-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="454f4-141">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="454f4-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="454f4-142">Return value</span></span>

<span data-ttu-id="454f4-143">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="454f4-143">This method does not return a value.</span></span> <span data-ttu-id="454f4-144">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="454f4-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="454f4-145">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="454f4-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="454f4-146">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="454f4-146">Error codes</span></span>

<span data-ttu-id="454f4-147">**ExecNotificationQueryAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中所識別的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="454f4-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="454f4-148">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="454f4-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-149">目前的使用者未獲授權可查看結果集。</span><span class="sxs-lookup"><span data-stu-id="454f4-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-150">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="454f4-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-151">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="454f4-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-152">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="454f4-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-153">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="454f4-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-154">**wbemErrInvalidQuery** -2147749911 (0x80041017) </span><span class="sxs-lookup"><span data-stu-id="454f4-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-155">查詢語法無效。</span><span class="sxs-lookup"><span data-stu-id="454f4-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018) </span><span class="sxs-lookup"><span data-stu-id="454f4-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-157">不支援要求的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="454f4-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="454f4-158">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="454f4-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="454f4-159">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="454f4-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="454f4-160">備註</span><span class="sxs-lookup"><span data-stu-id="454f4-160">Remarks</span></span>

<span data-ttu-id="454f4-161">**ExecNotificationQueryAsync** 方法會傳回未來事件所產生的事件種類物件。</span><span class="sxs-lookup"><span data-stu-id="454f4-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="454f4-162">**ExecNotificationQueryAsync** 要求的事件物件可以是內建的 (例如， [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) 或外部 (例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)或 SNMP 事件) 。</span><span class="sxs-lookup"><span data-stu-id="454f4-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="454f4-163">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="454f4-164">對 **ExecNotificationQueryAsync** 的呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="454f4-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="454f4-165">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="454f4-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="454f4-166">若要在每個物件傳回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="454f4-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="454f4-167">傳回所有物件之後，請執行最後的處理，以執行 *objWbemSink*。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="454f4-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="454f4-168">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="454f4-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="454f4-169">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="454f4-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="454f4-170">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="454f4-171">WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="454f4-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="454f4-172">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 傳回 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼 asan **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="454f4-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="454f4-173">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="454f4-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="454f4-174">範例</span><span class="sxs-lookup"><span data-stu-id="454f4-174">Examples</span></span>

<span data-ttu-id="454f4-175">下列 VBScript 程式碼範例示範一個腳本，該腳本會等候表示進程已結束的 WMI 事件通知。</span><span class="sxs-lookup"><span data-stu-id="454f4-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="454f4-176">它正在等候 WMI 內建事件，事件類別的實例 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="454f4-177">**\_ \_ InstanceDeletionEvent** 必須代表刪除 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的實例。</span><span class="sxs-lookup"><span data-stu-id="454f4-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="454f4-178">如需 WMI 內建事件的詳細資訊，請參閱 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="454f4-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="454f4-179">下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。</span><span class="sxs-lookup"><span data-stu-id="454f4-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="454f4-180">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="454f4-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="454f4-181">若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="454f4-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="454f4-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="454f4-182">Requirements</span></span>



| <span data-ttu-id="454f4-183">需求</span><span class="sxs-lookup"><span data-stu-id="454f4-183">Requirement</span></span> | <span data-ttu-id="454f4-184">值</span><span class="sxs-lookup"><span data-stu-id="454f4-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="454f4-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="454f4-185">Minimum supported client</span></span><br/> | <span data-ttu-id="454f4-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="454f4-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="454f4-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="454f4-187">Minimum supported server</span></span><br/> | <span data-ttu-id="454f4-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="454f4-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="454f4-189">標頭</span><span class="sxs-lookup"><span data-stu-id="454f4-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="454f4-190"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="454f4-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="454f4-191">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="454f4-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="454f4-192"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="454f4-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="454f4-193">DLL</span><span class="sxs-lookup"><span data-stu-id="454f4-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="454f4-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="454f4-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="454f4-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="454f4-195">CLSID</span></span><br/>                    | <span data-ttu-id="454f4-196">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="454f4-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="454f4-197">IID</span><span class="sxs-lookup"><span data-stu-id="454f4-197">IID</span></span><br/>                      | <span data-ttu-id="454f4-198">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="454f4-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="454f4-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="454f4-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="454f4-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="454f4-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="454f4-201">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="454f4-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="454f4-202">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="454f4-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="454f4-203">註冊系統登錄事件</span><span class="sxs-lookup"><span data-stu-id="454f4-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="454f4-204">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="454f4-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="454f4-205">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="454f4-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="454f4-206">在非同步呼叫上設定安全性</span><span class="sxs-lookup"><span data-stu-id="454f4-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

