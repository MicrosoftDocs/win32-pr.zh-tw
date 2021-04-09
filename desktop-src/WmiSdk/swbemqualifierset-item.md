---
description: SWbemQualifierSet 物件的 Item 方法會從集合傳回名為 SWbemQualifier 的物件。 這是這個物件的預設方法。
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: 'SWbemQualifierSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852456"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="e778b-104">SWbemQualifierSet 專案方法</span><span class="sxs-lookup"><span data-stu-id="e778b-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="e778b-105">[**SWbemQualifierSet**](swbemqualifierset.md)物件的 **Item** 方法會從集合傳回名為 [**SWbemQualifier**](swbemqualifier.md)的物件。</span><span class="sxs-lookup"><span data-stu-id="e778b-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="e778b-106">這是這個物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="e778b-106">This is the default method of this object.</span></span>

<span data-ttu-id="e778b-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e778b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e778b-108">語法</span><span class="sxs-lookup"><span data-stu-id="e778b-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e778b-109">參數</span><span class="sxs-lookup"><span data-stu-id="e778b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e778b-110">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e778b-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e778b-111">必要。</span><span class="sxs-lookup"><span data-stu-id="e778b-111">Required.</span></span> <span data-ttu-id="e778b-112">要取出的辨識符號名稱。</span><span class="sxs-lookup"><span data-stu-id="e778b-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e778b-113">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e778b-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e778b-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="e778b-114">Reserved.</span></span> <span data-ttu-id="e778b-115">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="e778b-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e778b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e778b-116">Return value</span></span>

<span data-ttu-id="e778b-117">如果成功，則會傳回要求的 [**SWbemQualifier**](swbemqualifier.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e778b-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e778b-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e778b-118">Error codes</span></span>

<span data-ttu-id="e778b-119">完成 **專案** 方法之後， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e778b-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e778b-120">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="e778b-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e778b-121">*IFlags* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e778b-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e778b-122">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="e778b-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e778b-123">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e778b-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e778b-124">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="e778b-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="e778b-125">指定的限定詞不存在。</span><span class="sxs-lookup"><span data-stu-id="e778b-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e778b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e778b-126">Requirements</span></span>



| <span data-ttu-id="e778b-127">需求</span><span class="sxs-lookup"><span data-stu-id="e778b-127">Requirement</span></span> | <span data-ttu-id="e778b-128">值</span><span class="sxs-lookup"><span data-stu-id="e778b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e778b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e778b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e778b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e778b-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e778b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e778b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e778b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e778b-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e778b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e778b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e778b-134"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e778b-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e778b-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e778b-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e778b-136"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e778b-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e778b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e778b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e778b-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e778b-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e778b-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="e778b-139">CLSID</span></span><br/>                    | <span data-ttu-id="e778b-140">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="e778b-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="e778b-141">IID</span><span class="sxs-lookup"><span data-stu-id="e778b-141">IID</span></span><br/>                      | <span data-ttu-id="e778b-142">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="e778b-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="e778b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e778b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e778b-144">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="e778b-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="e778b-145">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="e778b-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




