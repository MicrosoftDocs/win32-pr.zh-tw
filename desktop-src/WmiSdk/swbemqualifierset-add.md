---
description: SWbemQualifierSet 物件的 Add 方法會將 SWbemQualifier 物件加入至 SWbemQualifierSet 集合。 如果集合中已經存在具有相同名稱的辨識符號，則會予以取代。
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: 'SWbemQualifierSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320656"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="4f034-104">SWbemQualifierSet 新增方法</span><span class="sxs-lookup"><span data-stu-id="4f034-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="4f034-105">[**SWbemQualifierSet**](swbemqualifierset.md)物件的 **Add** 方法會將 [**SWbemQualifier**](swbemqualifier.md)物件加入至 **SWbemQualifierSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="4f034-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="4f034-106">如果集合中已經存在具有相同名稱的辨識符號，則會予以取代。</span><span class="sxs-lookup"><span data-stu-id="4f034-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="4f034-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4f034-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f034-108">語法</span><span class="sxs-lookup"><span data-stu-id="4f034-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4f034-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f034-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f034-110">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f034-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-111">必要。</span><span class="sxs-lookup"><span data-stu-id="4f034-111">Required.</span></span> <span data-ttu-id="4f034-112">新限定詞的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f034-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-113">*varVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f034-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-114">必要。</span><span class="sxs-lookup"><span data-stu-id="4f034-114">Required.</span></span> <span data-ttu-id="4f034-115">新限定詞的變異值。</span><span class="sxs-lookup"><span data-stu-id="4f034-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-116">*bPropagatesToSubclasses* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4f034-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-117">布林值，指出這個新的辨識符號是否會傳播至子類別。</span><span class="sxs-lookup"><span data-stu-id="4f034-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="4f034-118">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4f034-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-119">*bPropagatesToInstances* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4f034-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-120">布林值，指出這個新的辨識符號是否會傳播至實例。</span><span class="sxs-lookup"><span data-stu-id="4f034-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="4f034-121">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4f034-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-122">*bOverridable* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4f034-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-123">指出是否可以在傳播時覆寫此限定詞的布林值。</span><span class="sxs-lookup"><span data-stu-id="4f034-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="4f034-124">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4f034-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-125">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4f034-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f034-126">保留的。</span><span class="sxs-lookup"><span data-stu-id="4f034-126">Reserved.</span></span> <span data-ttu-id="4f034-127">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="4f034-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f034-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f034-128">Return value</span></span>

<span data-ttu-id="4f034-129">如果成功，這個方法會傳回代表新辨識符號的 [**SWbemQualifier**](swbemqualifier.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4f034-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="4f034-130">否則，會傳回 **null** 物件。</span><span class="sxs-lookup"><span data-stu-id="4f034-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f034-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4f034-131">Error codes</span></span>

<span data-ttu-id="4f034-132">完成 **Add** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4f034-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4f034-133">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="4f034-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4f034-134">*IFlags* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="4f034-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-135">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="4f034-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4f034-136">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f034-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-137">**wbemErrCannotBeKey** -2147749919 (0x8004101F) </span><span class="sxs-lookup"><span data-stu-id="4f034-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="4f034-138">在不能是索引鍵的屬性上，指定索引 **鍵** 限定詞的嘗試不合法。</span><span class="sxs-lookup"><span data-stu-id="4f034-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="4f034-139">索引鍵會在物件的類別定義中指定，並且不能對每個執行個體進行變更。</span><span class="sxs-lookup"><span data-stu-id="4f034-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029) </span><span class="sxs-lookup"><span data-stu-id="4f034-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="4f034-141">*VarVal* 參數不是合法的辨識符號類型。</span><span class="sxs-lookup"><span data-stu-id="4f034-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="4f034-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A) </span><span class="sxs-lookup"><span data-stu-id="4f034-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="4f034-143">因為擁有物件不允許覆寫，所以無法對此限定詞執行 **SWbemQualifierSet。**</span><span class="sxs-lookup"><span data-stu-id="4f034-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f034-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f034-144">Requirements</span></span>



| <span data-ttu-id="4f034-145">需求</span><span class="sxs-lookup"><span data-stu-id="4f034-145">Requirement</span></span> | <span data-ttu-id="4f034-146">值</span><span class="sxs-lookup"><span data-stu-id="4f034-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f034-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f034-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4f034-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f034-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f034-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f034-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4f034-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f034-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f034-151">標頭</span><span class="sxs-lookup"><span data-stu-id="4f034-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f034-152"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f034-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f034-153">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4f034-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f034-154"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4f034-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4f034-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4f034-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f034-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f034-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f034-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="4f034-157">CLSID</span></span><br/>                    | <span data-ttu-id="4f034-158">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="4f034-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="4f034-159">IID</span><span class="sxs-lookup"><span data-stu-id="4f034-159">IID</span></span><br/>                      | <span data-ttu-id="4f034-160">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="4f034-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4f034-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f034-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f034-162">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="4f034-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="4f034-163">**SWbemQualifierSet。移除**</span><span class="sxs-lookup"><span data-stu-id="4f034-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




