---
description: 根據物件路徑，抓取屬於類別定義或實例的物件。
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: 'SWbemServices. GetAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848612"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="61477-103">SWbemServices. GetAsync 方法</span><span class="sxs-lookup"><span data-stu-id="61477-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="61477-104">[**SWbemServices**](swbemservices.md)物件的 **GetAsync** 方法會根據物件路徑，來抓取物件，也就是類別定義或實例。</span><span class="sxs-lookup"><span data-stu-id="61477-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="61477-105">這個方法只會從與目前 [**SWbemServices**](swbemservices.md) 物件相關聯的命名空間中，抓取物件。</span><span class="sxs-lookup"><span data-stu-id="61477-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="61477-106">在非同步模式中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="61477-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="61477-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="61477-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="61477-109">語法</span><span class="sxs-lookup"><span data-stu-id="61477-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="61477-110">參數</span><span class="sxs-lookup"><span data-stu-id="61477-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61477-111">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="61477-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="61477-112">必要。</span><span class="sxs-lookup"><span data-stu-id="61477-112">Required.</span></span> <span data-ttu-id="61477-113">以非同步方式取得物件的物件接收。</span><span class="sxs-lookup"><span data-stu-id="61477-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="61477-114">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="61477-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="61477-115">*strObjectPath* \[選\]</span><span class="sxs-lookup"><span data-stu-id="61477-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61477-116">您要取得之物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="61477-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="61477-117">如果這個值是空的，則傳回的空物件可以成為新的類別。</span><span class="sxs-lookup"><span data-stu-id="61477-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="61477-118">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="61477-119">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="61477-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61477-120">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="61477-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="61477-121">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="61477-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="61477-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="61477-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="61477-123">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="61477-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="61477-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="61477-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="61477-125">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="61477-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="61477-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="61477-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="61477-127">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="61477-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="61477-128">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61477-129">*objwbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="61477-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61477-130">通常，這個值是未定義的。</span><span class="sxs-lookup"><span data-stu-id="61477-130">Typically, this value is undefined.</span></span> <span data-ttu-id="61477-131">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="61477-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="61477-132">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="61477-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="61477-133">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="61477-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61477-134">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="61477-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="61477-135">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="61477-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="61477-136">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="61477-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="61477-137">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="61477-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="61477-138">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61477-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="61477-139">Return value</span></span>

<span data-ttu-id="61477-140">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="61477-140">This method does not return a value.</span></span> <span data-ttu-id="61477-141">如果成功，當物件可用時，接收就會收到 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="61477-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61477-142">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="61477-142">Error codes</span></span>

<span data-ttu-id="61477-143">**GetAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61477-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="61477-144">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="61477-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="61477-145">目前的使用者沒有存取該物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="61477-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="61477-146">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="61477-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="61477-147">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="61477-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="61477-148">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="61477-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="61477-149">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="61477-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61477-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A) </span><span class="sxs-lookup"><span data-stu-id="61477-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="61477-151">指定的路徑無效。</span><span class="sxs-lookup"><span data-stu-id="61477-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="61477-152">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="61477-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="61477-153">找不到要求的物件。</span><span class="sxs-lookup"><span data-stu-id="61477-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="61477-154">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="61477-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="61477-155">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="61477-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61477-156">備註</span><span class="sxs-lookup"><span data-stu-id="61477-156">Remarks</span></span>

<span data-ttu-id="61477-157">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="61477-157">This call returns immediately.</span></span> <span data-ttu-id="61477-158">要求的物件和狀態會透過傳遞給 *objWbemSink* 中所指定接收器的回呼傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="61477-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="61477-159">若要在物件傳回時處理物件，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md)或 *objWbemSink*。[**OnCompleted**](swbemsink-oncompleted.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="61477-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="61477-160">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="61477-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="61477-161">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="61477-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="61477-162">若要消除風險，請使用最半同步或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="61477-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="61477-163">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="61477-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61477-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="61477-164">Requirements</span></span>



| <span data-ttu-id="61477-165">需求</span><span class="sxs-lookup"><span data-stu-id="61477-165">Requirement</span></span> | <span data-ttu-id="61477-166">值</span><span class="sxs-lookup"><span data-stu-id="61477-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61477-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61477-167">Minimum supported client</span></span><br/> | <span data-ttu-id="61477-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61477-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61477-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61477-169">Minimum supported server</span></span><br/> | <span data-ttu-id="61477-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61477-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61477-171">標頭</span><span class="sxs-lookup"><span data-stu-id="61477-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="61477-172"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="61477-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="61477-173">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="61477-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="61477-174"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61477-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61477-175">DLL</span><span class="sxs-lookup"><span data-stu-id="61477-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61477-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61477-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="61477-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="61477-177">CLSID</span></span><br/>                    | <span data-ttu-id="61477-178">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="61477-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="61477-179">IID</span><span class="sxs-lookup"><span data-stu-id="61477-179">IID</span></span><br/>                      | <span data-ttu-id="61477-180">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="61477-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="61477-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61477-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61477-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="61477-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="61477-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="61477-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

