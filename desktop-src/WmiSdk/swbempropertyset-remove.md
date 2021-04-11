---
description: 內含物件的 Remove 方法會刪除內含集合中的屬性。
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: '內含： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114864"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="4cafb-103">內含方法</span><span class="sxs-lookup"><span data-stu-id="4cafb-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="4cafb-104">[**內含**](swbempropertyset.md)物件的 **Remove** 方法會刪除 **內含** 集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="4cafb-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="4cafb-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4cafb-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cafb-106">語法</span><span class="sxs-lookup"><span data-stu-id="4cafb-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4cafb-107">參數</span><span class="sxs-lookup"><span data-stu-id="4cafb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cafb-108">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4cafb-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-109">必要。</span><span class="sxs-lookup"><span data-stu-id="4cafb-109">Required.</span></span> <span data-ttu-id="4cafb-110">要移除之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cafb-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4cafb-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="4cafb-112">Reserved.</span></span> <span data-ttu-id="4cafb-113">如果有指定，此值必須為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4cafb-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cafb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cafb-114">Return value</span></span>

<span data-ttu-id="4cafb-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4cafb-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cafb-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4cafb-116">Error codes</span></span>

<span data-ttu-id="4cafb-117">完成 **移除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4cafb-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4cafb-118">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="4cafb-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-119">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="4cafb-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-120">**wbemErrInvalidOperation** -2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="4cafb-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-121">使用者嘗試刪除無法刪除的屬性。</span><span class="sxs-lookup"><span data-stu-id="4cafb-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-122">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="4cafb-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-123">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="4cafb-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-124">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="4cafb-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-125">指定的屬性不存在。</span><span class="sxs-lookup"><span data-stu-id="4cafb-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-126">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="4cafb-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-127">記憶體不足，無法執行此方法。</span><span class="sxs-lookup"><span data-stu-id="4cafb-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-128">**wbemErrPropagatedProperty** -142927303552 (0x2147219380) </span><span class="sxs-lookup"><span data-stu-id="4cafb-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-129">使用者嘗試刪除未擁有的屬性。</span><span class="sxs-lookup"><span data-stu-id="4cafb-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="4cafb-130">屬性繼承自父代 (Parent) 類別。</span><span class="sxs-lookup"><span data-stu-id="4cafb-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="4cafb-131">**wbemErrResetToDefault** -2147758082 (0x80043002) </span><span class="sxs-lookup"><span data-stu-id="4cafb-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="4cafb-132">使用者已刪除目前類別的覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="4cafb-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="4cafb-133">父類別中這個屬性的預設值已重新開機。</span><span class="sxs-lookup"><span data-stu-id="4cafb-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cafb-134">備註</span><span class="sxs-lookup"><span data-stu-id="4cafb-134">Remarks</span></span>

<span data-ttu-id="4cafb-135">無法從類別實例或具有繼承屬性的衍生類別移除屬性。</span><span class="sxs-lookup"><span data-stu-id="4cafb-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="4cafb-136">這類刪除嘗試會引發錯誤，而且不會移除屬性;屬性會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="4cafb-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="4cafb-137">您無法在移除專案時逐一查看集合，因為當您從集合中移除專案時，集合指標會移至下一個元素。</span><span class="sxs-lookup"><span data-stu-id="4cafb-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="4cafb-138">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="4cafb-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4cafb-139">範例</span><span class="sxs-lookup"><span data-stu-id="4cafb-139">Examples</span></span>

<span data-ttu-id="4cafb-140">如需使用此方法的程式碼範例，請參閱 [**內含**](swbempropertyset.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="4cafb-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cafb-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cafb-141">Requirements</span></span>



| <span data-ttu-id="4cafb-142">需求</span><span class="sxs-lookup"><span data-stu-id="4cafb-142">Requirement</span></span> | <span data-ttu-id="4cafb-143">值</span><span class="sxs-lookup"><span data-stu-id="4cafb-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cafb-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cafb-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4cafb-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cafb-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cafb-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cafb-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4cafb-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cafb-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cafb-148">標頭</span><span class="sxs-lookup"><span data-stu-id="4cafb-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cafb-149"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cafb-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cafb-150">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4cafb-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cafb-151"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4cafb-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4cafb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4cafb-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cafb-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cafb-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4cafb-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="4cafb-154">CLSID</span></span><br/>                    | <span data-ttu-id="4cafb-155">CLSID \_ 內含</span><span class="sxs-lookup"><span data-stu-id="4cafb-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="4cafb-156">IID</span><span class="sxs-lookup"><span data-stu-id="4cafb-156">IID</span></span><br/>                      | <span data-ttu-id="4cafb-157">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="4cafb-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="4cafb-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cafb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cafb-159">**內含**</span><span class="sxs-lookup"><span data-stu-id="4cafb-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="4cafb-160">**內含新增**</span><span class="sxs-lookup"><span data-stu-id="4cafb-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




