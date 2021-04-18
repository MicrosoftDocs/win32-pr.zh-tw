---
description: 刪除物件路徑中指定的類別或實例。
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: 'SWbemServices. DeleteAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983401"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="50d49-103">SWbemServices. DeleteAsync 方法</span><span class="sxs-lookup"><span data-stu-id="50d49-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="50d49-104">[**SWbemServices**](swbemservices.md)物件的 **DeleteAsync** 方法會刪除物件路徑中指定的類別或實例。</span><span class="sxs-lookup"><span data-stu-id="50d49-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="50d49-105">**DeleteAsync** 的呼叫會立即傳回，而結果和狀態會透過傳遞至 *objWbemSink* 中指定之接收的事件傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="50d49-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="50d49-106">如需建立接收的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="50d49-107">您只能刪除您所連接的命名空間中的物件。</span><span class="sxs-lookup"><span data-stu-id="50d49-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="50d49-108">如果動態提供者提供類別或實例，則有時無法刪除此物件，除非提供者支援類別或實例的刪除。</span><span class="sxs-lookup"><span data-stu-id="50d49-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="50d49-109">在非同步模式中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="50d49-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="50d49-110">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="50d49-111">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50d49-112">語法</span><span class="sxs-lookup"><span data-stu-id="50d49-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="50d49-113">參數</span><span class="sxs-lookup"><span data-stu-id="50d49-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d49-114">*ObjWbemSink* \[選\]</span><span class="sxs-lookup"><span data-stu-id="50d49-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50d49-115">接收刪除結果的物件接收。</span><span class="sxs-lookup"><span data-stu-id="50d49-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="50d49-116">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="50d49-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-117">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="50d49-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="50d49-118">必要。</span><span class="sxs-lookup"><span data-stu-id="50d49-118">Required.</span></span> <span data-ttu-id="50d49-119">字串，包含您要刪除之物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="50d49-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="50d49-120">如需詳細資訊，請參閱 [描述 WMI 物件的位置](describing-the-location-of-a-wmi-object.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="50d49-121">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="50d49-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50d49-122">判斷是否傳回狀態更新。</span><span class="sxs-lookup"><span data-stu-id="50d49-122">Determines if status updates are returned.</span></span> <span data-ttu-id="50d49-123">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="50d49-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="50d49-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="50d49-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="50d49-125">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="50d49-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="50d49-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="50d49-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="50d49-127">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="50d49-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="50d49-128">*objWbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="50d49-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50d49-129">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="50d49-129">Typically, this is undefined.</span></span> <span data-ttu-id="50d49-130">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="50d49-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="50d49-131">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="50d49-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-132">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="50d49-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50d49-133">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="50d49-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="50d49-134">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="50d49-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="50d49-135">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="50d49-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="50d49-136">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="50d49-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="50d49-137">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d49-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="50d49-138">Return value</span></span>

<span data-ttu-id="50d49-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="50d49-139">This method does not return a value.</span></span> <span data-ttu-id="50d49-140">如果呼叫成功，物件接收就會收到刪除的通知。</span><span class="sxs-lookup"><span data-stu-id="50d49-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50d49-141">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="50d49-141">Error codes</span></span>

<span data-ttu-id="50d49-142">**DeleteAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="50d49-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="50d49-143">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="50d49-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-144">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="50d49-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-145">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="50d49-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-146">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="50d49-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-147">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="50d49-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-148">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="50d49-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-149">**wbemErrTransportFailure** -2147749909 (0x80041015) </span><span class="sxs-lookup"><span data-stu-id="50d49-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-150">發生網路錯誤，導致無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="50d49-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-151">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="50d49-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-152">目前或指定的使用者名稱和密碼無效或已獲授權，無法進行連接。</span><span class="sxs-lookup"><span data-stu-id="50d49-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="50d49-153">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="50d49-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="50d49-154">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="50d49-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50d49-155">備註</span><span class="sxs-lookup"><span data-stu-id="50d49-155">Remarks</span></span>

<span data-ttu-id="50d49-156">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="50d49-156">This call returns immediately.</span></span> <span data-ttu-id="50d49-157">刪除作業的狀態會透過傳遞給 *objWbemSink* 中所指定接收器的回呼傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="50d49-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="50d49-158">您可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="50d49-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="50d49-159">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="50d49-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="50d49-160">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="50d49-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="50d49-161">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="50d49-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50d49-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="50d49-162">Requirements</span></span>



| <span data-ttu-id="50d49-163">需求</span><span class="sxs-lookup"><span data-stu-id="50d49-163">Requirement</span></span> | <span data-ttu-id="50d49-164">值</span><span class="sxs-lookup"><span data-stu-id="50d49-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d49-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50d49-165">Minimum supported client</span></span><br/> | <span data-ttu-id="50d49-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50d49-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50d49-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50d49-167">Minimum supported server</span></span><br/> | <span data-ttu-id="50d49-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50d49-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50d49-169">標頭</span><span class="sxs-lookup"><span data-stu-id="50d49-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d49-170"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="50d49-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50d49-171">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="50d49-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="50d49-172"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50d49-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50d49-173">DLL</span><span class="sxs-lookup"><span data-stu-id="50d49-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d49-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d49-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="50d49-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="50d49-175">CLSID</span></span><br/>                    | <span data-ttu-id="50d49-176">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="50d49-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="50d49-177">IID</span><span class="sxs-lookup"><span data-stu-id="50d49-177">IID</span></span><br/>                      | <span data-ttu-id="50d49-178">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="50d49-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="50d49-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50d49-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d49-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="50d49-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="50d49-181">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="50d49-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

