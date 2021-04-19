---
description: SWbemObject 的 DeleteAsync \_ 方法會以非同步方式刪除目前的類別或目前的實例。
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: 'SWbemObject.DeleteAsync_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989932"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="4d812-103">SWbemObject. DeleteAsync \_ 方法</span><span class="sxs-lookup"><span data-stu-id="4d812-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="4d812-104">[**SWbemObject**](swbemobject.md)的 **DeleteAsync \_** 方法會以非同步方式刪除目前的類別或目前的實例。</span><span class="sxs-lookup"><span data-stu-id="4d812-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="4d812-105">如果動態提供者提供類別或實例，則有時無法刪除此物件，除非提供者支援類別或實例的刪除。</span><span class="sxs-lookup"><span data-stu-id="4d812-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="4d812-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4d812-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d812-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d812-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4d812-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d812-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d812-109">*objWbemSink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d812-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d812-110">傳回刪除操作結果的物件接收。</span><span class="sxs-lookup"><span data-stu-id="4d812-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d812-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d812-112">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="4d812-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="4d812-113">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="4d812-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4d812-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="4d812-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4d812-115">導致非同步呼叫將狀態更新傳送至物件接收的 [**SWbemSink. OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4d812-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4d812-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* ( 0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="4d812-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4d812-117">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="4d812-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4d812-118">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d812-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d812-119">此參數通常是未定義的。</span><span class="sxs-lookup"><span data-stu-id="4d812-119">This parameter is typically undefined.</span></span> <span data-ttu-id="4d812-120">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="4d812-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4d812-121">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="4d812-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-122">*objWbemAsyncCoNtext* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d812-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d812-123">這是一個 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，它會返回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="4d812-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4d812-124">如果您要使用相同的物件接收進行多個非同步呼叫，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="4d812-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4d812-125">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="4d812-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4d812-126">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="4d812-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4d812-127">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4d812-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d812-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d812-128">Return value</span></span>

<span data-ttu-id="4d812-129">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d812-129">This method does not return a value.</span></span> <span data-ttu-id="4d812-130">如果此呼叫成功，則會透過提供的物件接收來提供刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="4d812-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d812-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4d812-131">Error codes</span></span>

<span data-ttu-id="4d812-132">**DeleteAsync \_** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4d812-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4d812-133">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="4d812-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-134">目前的內容沒有足夠的安全性許可權可刪除物件。</span><span class="sxs-lookup"><span data-stu-id="4d812-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-135">**wbemErrFailed** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="4d812-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-136">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d812-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-137">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="4d812-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-138">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="4d812-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-139">**wbemErrInvalidOperation** -2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="4d812-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-140">無法刪除物件。</span><span class="sxs-lookup"><span data-stu-id="4d812-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-141">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="4d812-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-142">物件不存在。</span><span class="sxs-lookup"><span data-stu-id="4d812-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4d812-143">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="4d812-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4d812-144">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="4d812-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d812-145">備註</span><span class="sxs-lookup"><span data-stu-id="4d812-145">Remarks</span></span>

<span data-ttu-id="4d812-146">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4d812-146">This call returns immediately.</span></span> <span data-ttu-id="4d812-147">狀態會透過傳遞給 *objWbemSink* 中所指定接收器的回呼傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="4d812-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="4d812-148">非同步回呼可讓 nonauthenticated 使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="4d812-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="4d812-149">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="4d812-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4d812-150">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="4d812-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="4d812-151">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4d812-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d812-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d812-152">Requirements</span></span>



| <span data-ttu-id="4d812-153">需求</span><span class="sxs-lookup"><span data-stu-id="4d812-153">Requirement</span></span> | <span data-ttu-id="4d812-154">值</span><span class="sxs-lookup"><span data-stu-id="4d812-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d812-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d812-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4d812-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d812-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d812-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d812-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4d812-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d812-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d812-159">標頭</span><span class="sxs-lookup"><span data-stu-id="4d812-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d812-160"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d812-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d812-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4d812-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d812-162"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d812-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d812-163">DLL</span><span class="sxs-lookup"><span data-stu-id="4d812-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d812-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d812-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d812-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="4d812-165">CLSID</span></span><br/>                    | <span data-ttu-id="4d812-166">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4d812-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="4d812-167">IID</span><span class="sxs-lookup"><span data-stu-id="4d812-167">IID</span></span><br/>                      | <span data-ttu-id="4d812-168">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="4d812-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

