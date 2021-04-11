---
description: 根據使用者指定的準則，抓取指定類別的實例。
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: 'SWbemServices. InstancesOfAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848611"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="8a8b1-103">SWbemServices. InstancesOfAsync 方法</span><span class="sxs-lookup"><span data-stu-id="8a8b1-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="8a8b1-104">[**SWbemServices**](swbemservices.md)物件的 **InstancesOfAsync** 方法會根據使用者指定的準則，來抓取指定類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="8a8b1-105">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="8a8b1-106">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8a8b1-107">如需語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8b1-108">語法</span><span class="sxs-lookup"><span data-stu-id="8a8b1-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8a8b1-109">參數</span><span class="sxs-lookup"><span data-stu-id="8a8b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8b1-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="8a8b1-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="8a8b1-111">非同步接收實例的物件接收。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="8a8b1-112">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="8a8b1-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="8a8b1-114">必要。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-114">Required.</span></span> <span data-ttu-id="8a8b1-115">字串，其中包含您想要之實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="8a8b1-116">此參數不可以是空白。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-117">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8a8b1-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-118">判斷呼叫列舉的深度，以及呼叫是否立即傳回。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="8a8b1-119">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="8a8b1-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8a8b1-121">強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="8a8b1-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8a8b1-123">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-123">Default for this parameter.</span></span> <span data-ttu-id="8a8b1-124">此值會強制列舉包含階層中的所有類別。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8a8b1-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8a8b1-126">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8a8b1-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8a8b1-128">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="8a8b1-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="8a8b1-130">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="8a8b1-131">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8a8b1-132">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8a8b1-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-133">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-133">Typically, this is undefined.</span></span> <span data-ttu-id="8a8b1-134">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8a8b1-135">支援或需要內容資訊資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-136">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="8a8b1-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-137">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8a8b1-138">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8a8b1-139">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8a8b1-140">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8b1-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a8b1-141">Return value</span></span>

<span data-ttu-id="8a8b1-142">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-142">This method does not return a value.</span></span> <span data-ttu-id="8a8b1-143">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="8a8b1-144">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a8b1-145">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8a8b1-145">Error codes</span></span>

<span data-ttu-id="8a8b1-146">**InstancesOfAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8a8b1-147">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-148">目前的使用者沒有許可權可查看指定之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-149">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-150">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-151">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-152">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-153">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-154">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8a8b1-155">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="8a8b1-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8a8b1-156">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a8b1-157">備註</span><span class="sxs-lookup"><span data-stu-id="8a8b1-157">Remarks</span></span>

<span data-ttu-id="8a8b1-158">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-158">This call returns immediately.</span></span> <span data-ttu-id="8a8b1-159">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8a8b1-160">若要在每個物件返回時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8a8b1-161">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8a8b1-162">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8a8b1-163">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8a8b1-164">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="8a8b1-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="8a8b1-165">**InstancesOfAsync** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="8a8b1-166">傳回的列舉值不會有零 (0) 元素的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a8b1-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8b1-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a8b1-167">Requirements</span></span>



| <span data-ttu-id="8a8b1-168">需求</span><span class="sxs-lookup"><span data-stu-id="8a8b1-168">Requirement</span></span> | <span data-ttu-id="8a8b1-169">值</span><span class="sxs-lookup"><span data-stu-id="8a8b1-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8b1-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a8b1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8b1-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a8b1-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a8b1-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a8b1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8b1-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a8b1-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a8b1-174">標頭</span><span class="sxs-lookup"><span data-stu-id="8a8b1-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a8b1-175"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a8b1-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a8b1-176">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8a8b1-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a8b1-177"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a8b1-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a8b1-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8b1-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8b1-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8b1-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a8b1-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a8b1-180">CLSID</span></span><br/>                    | <span data-ttu-id="8a8b1-181">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="8a8b1-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="8a8b1-182">IID</span><span class="sxs-lookup"><span data-stu-id="8a8b1-182">IID</span></span><br/>                      | <span data-ttu-id="8a8b1-183">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="8a8b1-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8a8b1-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a8b1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8b1-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8a8b1-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="8a8b1-186">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="8a8b1-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

