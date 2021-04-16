---
description: SWbemQualifierSet 物件的 Remove 方法會從集合中刪除已命名的辨識符號。
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: 'SWbemQualifierSet： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512976"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="849ad-103">SWbemQualifierSet 方法</span><span class="sxs-lookup"><span data-stu-id="849ad-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="849ad-104">[**SWbemQualifierSet**](swbemqualifierset.md)物件的 **Remove** 方法會從集合中刪除已命名的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="849ad-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="849ad-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="849ad-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="849ad-106">語法</span><span class="sxs-lookup"><span data-stu-id="849ad-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="849ad-107">參數</span><span class="sxs-lookup"><span data-stu-id="849ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849ad-108">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="849ad-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="849ad-109">必要。</span><span class="sxs-lookup"><span data-stu-id="849ad-109">Required.</span></span> <span data-ttu-id="849ad-110">要移除的辨識符號名稱。</span><span class="sxs-lookup"><span data-stu-id="849ad-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="849ad-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="849ad-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="849ad-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="849ad-112">Reserved.</span></span> <span data-ttu-id="849ad-113">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="849ad-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849ad-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="849ad-114">Return value</span></span>

<span data-ttu-id="849ad-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="849ad-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="849ad-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="849ad-116">Error codes</span></span>

<span data-ttu-id="849ad-117">完成 **移除** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="849ad-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="849ad-118">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="849ad-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="849ad-119">*IFlags* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="849ad-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="849ad-120">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="849ad-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="849ad-121">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="849ad-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="849ad-122">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="849ad-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="849ad-123">指定的限定詞不存在。</span><span class="sxs-lookup"><span data-stu-id="849ad-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="849ad-124">**wbemErrInvalidOperation** -2147749910 (0x80041016) </span><span class="sxs-lookup"><span data-stu-id="849ad-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="849ad-125">移除此辨識符號不合法。</span><span class="sxs-lookup"><span data-stu-id="849ad-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="849ad-126">備註</span><span class="sxs-lookup"><span data-stu-id="849ad-126">Remarks</span></span>

<span data-ttu-id="849ad-127">您無法在移除專案時逐一查看集合，因為當您從集合中移除專案時，集合指標會移至下一個元素。</span><span class="sxs-lookup"><span data-stu-id="849ad-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="849ad-128">如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。</span><span class="sxs-lookup"><span data-stu-id="849ad-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="849ad-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="849ad-129">Requirements</span></span>



| <span data-ttu-id="849ad-130">需求</span><span class="sxs-lookup"><span data-stu-id="849ad-130">Requirement</span></span> | <span data-ttu-id="849ad-131">值</span><span class="sxs-lookup"><span data-stu-id="849ad-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="849ad-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="849ad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="849ad-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="849ad-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="849ad-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="849ad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="849ad-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="849ad-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="849ad-136">標頭</span><span class="sxs-lookup"><span data-stu-id="849ad-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="849ad-137"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="849ad-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="849ad-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="849ad-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="849ad-139"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="849ad-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="849ad-140">DLL</span><span class="sxs-lookup"><span data-stu-id="849ad-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="849ad-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="849ad-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="849ad-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="849ad-142">CLSID</span></span><br/>                    | <span data-ttu-id="849ad-143">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="849ad-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="849ad-144">IID</span><span class="sxs-lookup"><span data-stu-id="849ad-144">IID</span></span><br/>                      | <span data-ttu-id="849ad-145">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="849ad-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="849ad-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="849ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="849ad-147">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="849ad-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="849ad-148">**SWbemQualifierSet 新增**</span><span class="sxs-lookup"><span data-stu-id="849ad-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




