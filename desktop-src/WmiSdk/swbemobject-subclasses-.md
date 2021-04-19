---
description: SWbemObject 物件的子類別方法會傳回 \_ swbemobjectset 搭配使用物件。
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: 'SWbemObject.Subclasses_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979061"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="d4ed3-103">SWbemObject 類別 \_ 方法</span><span class="sxs-lookup"><span data-stu-id="d4ed3-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="d4ed3-104">[**SWbemObject**](swbemobject.md)物件的子 **類別 \_** 方法會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="d4ed3-105">此物件是目前物件的子類別集合，必須是類別。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="d4ed3-106">傳回之集合中的專案可以使用標準的收集方法來取得。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="d4ed3-107">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="d4ed3-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ed3-109">語法</span><span class="sxs-lookup"><span data-stu-id="d4ed3-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d4ed3-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4ed3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ed3-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d4ed3-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-112">判斷呼叫列舉詳細程度的整數。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="d4ed3-113">此參數可接受下列值。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="d4ed3-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d4ed3-115">強制遞迴列舉至所有衍生自指定父類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="d4ed3-116">父類別本身不會在列舉中傳回。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="d4ed3-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d4ed3-118">此參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-118">Default value for this parameter.</span></span> <span data-ttu-id="d4ed3-119">它會強制列舉只包含指定之父類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="d4ed3-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d4ed3-121">導致呼叫立即返回</span><span class="sxs-lookup"><span data-stu-id="d4ed3-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="d4ed3-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d4ed3-123">導致此呼叫封鎖，直到呼叫完成為止。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="d4ed3-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="d4ed3-125">導致 WMI 傳回類別修訂資料以及基類定義。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d4ed3-126">*objwbemNamedValueSet* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d4ed3-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-127">一般而言，這是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-127">Typically, this is undefined.</span></span> <span data-ttu-id="d4ed3-128">否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其元素代表服務要求的提供者所能使用的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d4ed3-129">支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ed3-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4ed3-130">Return value</span></span>

<span data-ttu-id="d4ed3-131">如果呼叫成功，則會傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4ed3-132">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d4ed3-132">Error codes</span></span>

<span data-ttu-id="d4ed3-133">在完成子 **類別 \_** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d4ed3-134">**wbemErrAccessDenied** -2147749891 (0x80041003) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-135">目前的使用者沒有許可權可查看呼叫所傳回的一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed3-136">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-137">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed3-138">**wbemErrInvalidClass** -2147749904 (0x80041010) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-139">指定的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed3-140">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-141">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed3-142">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="d4ed3-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d4ed3-143">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4ed3-144">備註</span><span class="sxs-lookup"><span data-stu-id="d4ed3-144">Remarks</span></span>

<span data-ttu-id="d4ed3-145">如果沒有目前物件的子類別，則傳回的集合不會有零個元素的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="d4ed3-146">子 **類別 \_** 方法只適用于類別物件。</span><span class="sxs-lookup"><span data-stu-id="d4ed3-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ed3-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ed3-147">Requirements</span></span>



| <span data-ttu-id="d4ed3-148">需求</span><span class="sxs-lookup"><span data-stu-id="d4ed3-148">Requirement</span></span> | <span data-ttu-id="d4ed3-149">值</span><span class="sxs-lookup"><span data-stu-id="d4ed3-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ed3-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4ed3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ed3-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4ed3-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4ed3-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4ed3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ed3-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4ed3-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4ed3-154">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ed3-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ed3-155"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ed3-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4ed3-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d4ed3-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4ed3-157"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4ed3-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4ed3-158">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ed3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ed3-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ed3-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4ed3-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4ed3-160">CLSID</span></span><br/>                    | <span data-ttu-id="d4ed3-161">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d4ed3-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d4ed3-162">IID</span><span class="sxs-lookup"><span data-stu-id="d4ed3-162">IID</span></span><br/>                      | <span data-ttu-id="d4ed3-163">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="d4ed3-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d4ed3-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ed3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ed3-165">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="d4ed3-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="d4ed3-166">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="d4ed3-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




