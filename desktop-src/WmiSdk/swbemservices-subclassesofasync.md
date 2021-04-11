---
description: 傳回指定類別的子類別集合。
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: 'SWbemServices. SubclassesOfAsync 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944593"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="f9d90-103">SWbemServices. SubclassesOfAsync 方法</span><span class="sxs-lookup"><span data-stu-id="f9d90-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="f9d90-104">[**SWbemServices**](swbemservices.md)物件的 **SubclassesOfAsync** 方法會傳回指定類別的子類別集合。</span><span class="sxs-lookup"><span data-stu-id="f9d90-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="f9d90-105">只針對類別物件使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="f9d90-105">Only use this method for class objects.</span></span>

<span data-ttu-id="f9d90-106">在非同步模式中呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f9d90-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="f9d90-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d90-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f9d90-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d90-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d90-109">語法</span><span class="sxs-lookup"><span data-stu-id="f9d90-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f9d90-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9d90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d90-111">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="f9d90-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="f9d90-112">必要。</span><span class="sxs-lookup"><span data-stu-id="f9d90-112">Required.</span></span> <span data-ttu-id="f9d90-113">以非同步方式接收子類別的物件接收。</span><span class="sxs-lookup"><span data-stu-id="f9d90-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="f9d90-114">建立 [**SWbemSink**](swbemsink.md) 物件以接收物件。</span><span class="sxs-lookup"><span data-stu-id="f9d90-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-115">*strSuperclass* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-116">指定父類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f9d90-116">Specifies a parent class name.</span></span> <span data-ttu-id="f9d90-117">只有屬於這個類別子類別的類別會在列舉值中傳回。</span><span class="sxs-lookup"><span data-stu-id="f9d90-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="f9d90-118">如果這個參數是空白的，而且如果 *iFlags* 是 **wbemQueryFlagShallow**，則只會傳回最上層類別 (也就是沒有父類別的類別) 。</span><span class="sxs-lookup"><span data-stu-id="f9d90-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="f9d90-119">如果這個參數是空白的，而且如果 *iFlags* 為 **wbemQueryFlagDeep**，就會傳回命名空間內的所有類別。</span><span class="sxs-lookup"><span data-stu-id="f9d90-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-120">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-121">判斷呼叫列舉的深度。</span><span class="sxs-lookup"><span data-stu-id="f9d90-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="f9d90-122">此參數的預設值為 **wbemQueryFlagDeep**。</span><span class="sxs-lookup"><span data-stu-id="f9d90-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="f9d90-123">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="f9d90-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="f9d90-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="f9d90-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f9d90-125">強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="f9d90-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="f9d90-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="f9d90-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f9d90-127">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="f9d90-127">Default for this parameter.</span></span> <span data-ttu-id="f9d90-128">此值會強制遞迴列舉至所有衍生自指定父類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="f9d90-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="f9d90-129">列舉中不會傳回父類別。</span><span class="sxs-lookup"><span data-stu-id="f9d90-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="f9d90-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="f9d90-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="f9d90-131">導致非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f9d90-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="f9d90-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="f9d90-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f9d90-133">防止非同步呼叫將狀態更新傳送至物件接收的 [**OnProgress**](swbemsink-onprogress.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f9d90-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f9d90-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="f9d90-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f9d90-135">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="f9d90-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="f9d90-136">如需詳細資訊，請參閱 [當地語系化 WMI 類別資訊](localizing-wmi-class-information.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d90-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f9d90-137">*objwbemNamedValueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-138">通常，這個參數是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f9d90-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="f9d90-139">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f9d90-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f9d90-140">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="f9d90-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-141">*objWbemAsyncCoNtext* \[選\]</span><span class="sxs-lookup"><span data-stu-id="f9d90-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-142">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，這個物件會傳回物件接收以識別原始非同步呼叫的來源。</span><span class="sxs-lookup"><span data-stu-id="f9d90-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="f9d90-143">使用這個參數可使用相同的物件接收進行多個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9d90-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="f9d90-144">若要使用此參數，請建立 **SWbemNamedValueSet** 物件，並使用 [**SWbemNamedValueSet. add**](swbemnamedvalueset-add.md) 方法來新增值，以識別您正在進行的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="f9d90-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="f9d90-145">這個 **SWbemNamedValueSet** 物件會傳回物件接收，而呼叫的來源可以使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="f9d90-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="f9d90-146">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d90-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d90-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9d90-147">Return value</span></span>

<span data-ttu-id="f9d90-148">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f9d90-148">This method does not return a value.</span></span> <span data-ttu-id="f9d90-149">如果成功，接收就會收到每個實例的 [**OnObjectReady**](swbemsink-onobjectready.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f9d90-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="f9d90-150">在最後一個實例之後，物件接收會收到 [**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f9d90-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9d90-151">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f9d90-151">Error codes</span></span>

<span data-ttu-id="f9d90-152">**SubclassesOfAsync** 方法完成後， [Err](/previous-versions//sbf5ze0e(v=vs.85))物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f9d90-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="f9d90-153">具有零個元素的傳回集合不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="f9d90-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="f9d90-154">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="f9d90-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-155">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="f9d90-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-156">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="f9d90-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-157">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f9d90-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-158">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="f9d90-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-159">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="f9d90-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-160">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="f9d90-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-161">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f9d90-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f9d90-162">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="f9d90-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f9d90-163">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="f9d90-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9d90-164">備註</span><span class="sxs-lookup"><span data-stu-id="f9d90-164">Remarks</span></span>

<span data-ttu-id="f9d90-165">此呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="f9d90-165">This call returns immediately.</span></span> <span data-ttu-id="f9d90-166">要求的物件和狀態會透過回呼傳遞給 *objWbemSink* 中指定的接收，傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="f9d90-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="f9d90-167">若要在每個物件抵達時進行處理，請建立 *objWbemSink*。[**OnObjectReady**](swbemsink-onobjectready.md) 事件副程式。</span><span class="sxs-lookup"><span data-stu-id="f9d90-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="f9d90-168">傳回所有物件之後，您就可以在 *objWbemSink* 的執行中執行最終處理。[**OnCompleted**](swbemsink-oncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f9d90-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="f9d90-169">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="f9d90-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="f9d90-170">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="f9d90-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="f9d90-171">若要消除風險，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d90-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d90-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d90-172">Requirements</span></span>



| <span data-ttu-id="f9d90-173">需求</span><span class="sxs-lookup"><span data-stu-id="f9d90-173">Requirement</span></span> | <span data-ttu-id="f9d90-174">值</span><span class="sxs-lookup"><span data-stu-id="f9d90-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d90-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9d90-175">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d90-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9d90-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9d90-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9d90-177">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d90-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9d90-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9d90-179">標頭</span><span class="sxs-lookup"><span data-stu-id="f9d90-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9d90-180"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d90-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9d90-181">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f9d90-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9d90-182"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9d90-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9d90-183">DLL</span><span class="sxs-lookup"><span data-stu-id="f9d90-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9d90-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9d90-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9d90-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="f9d90-185">CLSID</span></span><br/>                    | <span data-ttu-id="f9d90-186">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="f9d90-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="f9d90-187">IID</span><span class="sxs-lookup"><span data-stu-id="f9d90-187">IID</span></span><br/>                      | <span data-ttu-id="f9d90-188">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="f9d90-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f9d90-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9d90-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d90-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="f9d90-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="f9d90-191">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="f9d90-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

