---
description: 執行查詢以接收事件。 呼叫會立即傳回。
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: " (>wbemdisp.tlb 的 SWbemServices.ExecNotificationQuery 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979191"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="344da-104">SWbemServices.ExecNotificationQuery 方法</span><span class="sxs-lookup"><span data-stu-id="344da-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="344da-105">[**SWbemServices**](swbemservices.md)物件的 **ExecNotificationQuery** 方法會執行查詢來接收事件。</span><span class="sxs-lookup"><span data-stu-id="344da-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="344da-106">呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="344da-106">The call returns immediately.</span></span> <span data-ttu-id="344da-107">當事件到達時，使用者可以輪詢傳回的列舉值。</span><span class="sxs-lookup"><span data-stu-id="344da-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="344da-108">方法會在半同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="344da-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="344da-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="344da-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="344da-110">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="344da-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="344da-111">語法</span><span class="sxs-lookup"><span data-stu-id="344da-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="344da-112">參數</span><span class="sxs-lookup"><span data-stu-id="344da-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344da-113">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="344da-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="344da-114">必要。</span><span class="sxs-lookup"><span data-stu-id="344da-114">Required.</span></span> <span data-ttu-id="344da-115">包含事件相關查詢之文字的字串。</span><span class="sxs-lookup"><span data-stu-id="344da-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="344da-116">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="344da-116">This parameter cannot be blank.</span></span> <span data-ttu-id="344da-117">如需建立 WMI 查詢字串的詳細資訊，請參閱 [使用 Wql 查詢](querying-with-wql.md) 和 [wql](wql-sql-for-wmi.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="344da-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="344da-118">*strQueryLanguage* \[選\]</span><span class="sxs-lookup"><span data-stu-id="344da-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="344da-119">字串，包含要使用的查詢語言。</span><span class="sxs-lookup"><span data-stu-id="344da-119">String that contains the query language to be used.</span></span> <span data-ttu-id="344da-120">如果有指定，此值必須是 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="344da-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="344da-121">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="344da-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="344da-122">這是決定查詢行為的整數。</span><span class="sxs-lookup"><span data-stu-id="344da-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="344da-123">預設值為 **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**。</span><span class="sxs-lookup"><span data-stu-id="344da-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="344da-124">如果您指定這個參數，此參數必須設定為 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** ，否則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="344da-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="344da-125">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="344da-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="344da-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="344da-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="344da-127">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="344da-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="344da-128">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="344da-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="344da-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="344da-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="344da-130">導致呼叫立即返回。</span><span class="sxs-lookup"><span data-stu-id="344da-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="344da-131">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="344da-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="344da-132">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="344da-132">Typically, this is undefined.</span></span> <span data-ttu-id="344da-133">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="344da-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="344da-134">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="344da-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344da-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="344da-135">Return value</span></span>

<span data-ttu-id="344da-136">如果沒有發生錯誤，這個方法會傳回 [**SWbemEventSource**](swbemeventsource.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="344da-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="344da-137">您可以呼叫 [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) 方法，在事件抵達時取出它們。</span><span class="sxs-lookup"><span data-stu-id="344da-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="344da-138">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="344da-138">Error codes</span></span>

<span data-ttu-id="344da-139">**ExecNotificationQuery** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="344da-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="344da-140">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="344da-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="344da-141">目前的使用者未獲授權可查看結果集。</span><span class="sxs-lookup"><span data-stu-id="344da-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="344da-142">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="344da-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="344da-143">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="344da-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="344da-144">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="344da-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="344da-145">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="344da-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="344da-146">**wbemErrInvalidQuery** -2147749911 (0x80041017) </span><span class="sxs-lookup"><span data-stu-id="344da-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="344da-147">查詢語法無效。</span><span class="sxs-lookup"><span data-stu-id="344da-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="344da-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018) </span><span class="sxs-lookup"><span data-stu-id="344da-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="344da-149">所要求的查詢語言不支援。</span><span class="sxs-lookup"><span data-stu-id="344da-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="344da-150">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="344da-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="344da-151">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="344da-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="344da-152">備註</span><span class="sxs-lookup"><span data-stu-id="344da-152">Remarks</span></span>

<span data-ttu-id="344da-153">不同于 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) 方法， **ExecNotificationQuery** 會傳回未來事件所產生的事件種類物件，而不是現有的物件。</span><span class="sxs-lookup"><span data-stu-id="344da-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="344da-154">**ExecNotificationQuery** 要求的事件物件可以是內建的 (例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) 或外建 (（例如， [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)或 SNMP 事件) 之類的登錄提供者事件）。</span><span class="sxs-lookup"><span data-stu-id="344da-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="344da-155">如需詳細資訊，請參閱 [判斷要接收](determining-the-type-of-event-to-receive.md) 和 [接收事件通知](receiving-event-notifications.md)的事件種類。</span><span class="sxs-lookup"><span data-stu-id="344da-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="344da-156">WQL 查詢中可使用的 **和** 和 **或** 關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="344da-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="344da-157">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="344da-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="344da-158">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="344da-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="344da-159">範例</span><span class="sxs-lookup"><span data-stu-id="344da-159">Examples</span></span>

<span data-ttu-id="344da-160">下列 VBScript 程式碼範例會監視本機電腦上的磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="344da-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="344da-161">請注意， [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) 是由提供者定義的外建事件，而不是內建的 WMI 定義事件。</span><span class="sxs-lookup"><span data-stu-id="344da-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="344da-162">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="344da-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="344da-163">下列 VBScript 程式碼範例會監視進程刪除。</span><span class="sxs-lookup"><span data-stu-id="344da-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="344da-164">如果您在工作管理員中刪除進程或關閉應用程式，則腳本會顯示一則訊息。</span><span class="sxs-lookup"><span data-stu-id="344da-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="344da-165">請注意，此腳本會查詢由 WMI [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)定義的內部事件。</span><span class="sxs-lookup"><span data-stu-id="344da-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="344da-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="344da-166">Requirements</span></span>



| <span data-ttu-id="344da-167">需求</span><span class="sxs-lookup"><span data-stu-id="344da-167">Requirement</span></span> | <span data-ttu-id="344da-168">值</span><span class="sxs-lookup"><span data-stu-id="344da-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="344da-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="344da-169">Minimum supported client</span></span><br/> | <span data-ttu-id="344da-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="344da-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="344da-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="344da-171">Minimum supported server</span></span><br/> | <span data-ttu-id="344da-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="344da-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="344da-173">標頭</span><span class="sxs-lookup"><span data-stu-id="344da-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="344da-174"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="344da-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="344da-175">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="344da-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="344da-176"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="344da-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="344da-177">DLL</span><span class="sxs-lookup"><span data-stu-id="344da-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="344da-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="344da-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="344da-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="344da-179">CLSID</span></span><br/>                    | <span data-ttu-id="344da-180">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="344da-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="344da-181">IID</span><span class="sxs-lookup"><span data-stu-id="344da-181">IID</span></span><br/>                      | <span data-ttu-id="344da-182">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="344da-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="344da-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="344da-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344da-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="344da-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="344da-185">**SWbemEventSource.NextEvent**</span><span class="sxs-lookup"><span data-stu-id="344da-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="344da-186">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="344da-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="344da-187">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="344da-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="344da-188">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="344da-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="344da-189">WQL (適用於 WMI 的 SQL)</span><span class="sxs-lookup"><span data-stu-id="344da-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="344da-190">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="344da-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

