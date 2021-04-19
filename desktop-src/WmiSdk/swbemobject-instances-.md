---
description: '\_SWbemObject 物件的 instance 方法會建立一個列舉值，這個列舉值會傳回目前類別物件的實例。 這個方法會執行簡單的查詢。 更複雜的查詢可能需要使用 SWbemServices.ExecQuery。'
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: 'SWbemObject.Instances_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981209"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="c4637-105">SWbemObject 實例 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="c4637-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="c4637-106">SWbemObject 物件的 instance 方法 [](swbemobject.md)會建立一個列舉值，這個列舉值會傳回目前類別物件的實例。 **\_**</span><span class="sxs-lookup"><span data-stu-id="c4637-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="c4637-107">這個方法會執行簡單的查詢。</span><span class="sxs-lookup"><span data-stu-id="c4637-107">This method implements a simple query.</span></span> <span data-ttu-id="c4637-108">更複雜的查詢可能需要使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md)。</span><span class="sxs-lookup"><span data-stu-id="c4637-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="c4637-109">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="c4637-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4637-110">語法</span><span class="sxs-lookup"><span data-stu-id="c4637-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c4637-111">參數</span><span class="sxs-lookup"><span data-stu-id="c4637-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4637-112">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c4637-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4637-113">判斷呼叫行為的整數。</span><span class="sxs-lookup"><span data-stu-id="c4637-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="c4637-114">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="c4637-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="c4637-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-116">使順向列舉值傳回。</span><span class="sxs-lookup"><span data-stu-id="c4637-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="c4637-117">順向列舉值的速度通常會比傳統列舉值更快，且使用的記憶體較少，但不允許呼叫 [**SWbemObject。 \_**](swbemobject-clone-.md)</span><span class="sxs-lookup"><span data-stu-id="c4637-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="c4637-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-119">讓 WMI 保留列舉物件的指標，直到用戶端釋放列舉值為止。</span><span class="sxs-lookup"><span data-stu-id="c4637-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="c4637-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-121">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="c4637-121">Default value for this parameter.</span></span> <span data-ttu-id="c4637-122">此旗標會立即傳回呼叫。</span><span class="sxs-lookup"><span data-stu-id="c4637-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="c4637-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* ( 0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-124">導致此呼叫封鎖，直到查詢完成為止。</span><span class="sxs-lookup"><span data-stu-id="c4637-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="c4637-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-126">強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="c4637-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="c4637-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-128">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="c4637-128">Default for this parameter.</span></span> <span data-ttu-id="c4637-129">此值會強制列舉包含階層中的所有類別。</span><span class="sxs-lookup"><span data-stu-id="c4637-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c4637-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="c4637-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c4637-131">讓 WMI 以基類定義傳回類別修訂資料。</span><span class="sxs-lookup"><span data-stu-id="c4637-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c4637-132">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c4637-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4637-133">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="c4637-133">Typically, this is undefined.</span></span> <span data-ttu-id="c4637-134">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="c4637-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c4637-135">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="c4637-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4637-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4637-136">Return value</span></span>

<span data-ttu-id="c4637-137">如果方法成功， [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件會傳回。</span><span class="sxs-lookup"><span data-stu-id="c4637-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4637-138">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c4637-138">Error codes</span></span>

<span data-ttu-id="c4637-139">在完成 **實例 \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c4637-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c4637-140">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="c4637-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c4637-141">目前的使用者沒有許可權可查看指定之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c4637-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="c4637-142">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="c4637-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c4637-143">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4637-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c4637-144">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="c4637-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="c4637-145">指定的類別無效。</span><span class="sxs-lookup"><span data-stu-id="c4637-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c4637-146">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="c4637-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c4637-147">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="c4637-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c4637-148">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="c4637-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c4637-149">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="c4637-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4637-150">備註</span><span class="sxs-lookup"><span data-stu-id="c4637-150">Remarks</span></span>

<span data-ttu-id="c4637-151">**實例 \_** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="c4637-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="c4637-152">傳回的集合沒有零個元素時，不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c4637-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="c4637-153">由於預設的 *IFlags* 值 **wbemFlagReturnImmediately**，此方法的預設行為是最 [*半*](gloss-s.md)的。</span><span class="sxs-lookup"><span data-stu-id="c4637-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4637-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4637-154">Requirements</span></span>



| <span data-ttu-id="c4637-155">需求</span><span class="sxs-lookup"><span data-stu-id="c4637-155">Requirement</span></span> | <span data-ttu-id="c4637-156">值</span><span class="sxs-lookup"><span data-stu-id="c4637-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4637-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4637-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c4637-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4637-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4637-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4637-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c4637-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4637-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4637-161">標頭</span><span class="sxs-lookup"><span data-stu-id="c4637-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4637-162"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4637-163">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c4637-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4637-164"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4637-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c4637-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4637-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4637-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4637-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="c4637-167">CLSID</span></span><br/>                    | <span data-ttu-id="c4637-168">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c4637-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c4637-169">IID</span><span class="sxs-lookup"><span data-stu-id="c4637-169">IID</span></span><br/>                      | <span data-ttu-id="c4637-170">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="c4637-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c4637-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4637-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4637-172">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c4637-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c4637-173">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="c4637-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




