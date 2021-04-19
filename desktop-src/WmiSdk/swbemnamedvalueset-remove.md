---
description: SWbemNamedValueSet 物件的 Remove 方法會從內容中刪除命名值。
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d41ecd7d28b95534c8e6d88d1c57756c269cf790
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975433"
---
# <a name="swbemnamedvaluesetremove-method"></a><span data-ttu-id="ccb6c-103">SWbemNamedValueSet 方法</span><span class="sxs-lookup"><span data-stu-id="ccb6c-103">SWbemNamedValueSet.Remove method</span></span>

<span data-ttu-id="ccb6c-104">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Remove** 方法會從內容中刪除命名值。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-104">The **Remove** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object deletes a named value from the context.</span></span>

<span data-ttu-id="ccb6c-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb6c-106">語法</span><span class="sxs-lookup"><span data-stu-id="ccb6c-106">Syntax</span></span>


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ccb6c-107">參數</span><span class="sxs-lookup"><span data-stu-id="ccb6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb6c-108">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccb6c-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb6c-109">必要。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-109">Required.</span></span> <span data-ttu-id="ccb6c-110">要移除之值的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-110">Name of the value to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ccb6c-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ccb6c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb6c-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-112">Reserved.</span></span> <span data-ttu-id="ccb6c-113">如果有指定，此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb6c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccb6c-114">Return value</span></span>

<span data-ttu-id="ccb6c-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccb6c-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ccb6c-116">Error codes</span></span>

<span data-ttu-id="ccb6c-117">完成 **移除** 方法時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-117">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ccb6c-118">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="ccb6c-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ccb6c-119">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ccb6c-120">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="ccb6c-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ccb6c-121">指定的參數無效，或無法剖析命名空間。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="ccb6c-122">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="ccb6c-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ccb6c-123">找不到要求的項目。</span><span class="sxs-lookup"><span data-stu-id="ccb6c-123">The requested item was not found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccb6c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccb6c-124">Requirements</span></span>



| <span data-ttu-id="ccb6c-125">需求</span><span class="sxs-lookup"><span data-stu-id="ccb6c-125">Requirement</span></span> | <span data-ttu-id="ccb6c-126">值</span><span class="sxs-lookup"><span data-stu-id="ccb6c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb6c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccb6c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb6c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccb6c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ccb6c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccb6c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb6c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccb6c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ccb6c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="ccb6c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccb6c-132"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6c-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccb6c-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ccb6c-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccb6c-134"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6c-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccb6c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb6c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb6c-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6c-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccb6c-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="ccb6c-137">CLSID</span></span><br/>                    | <span data-ttu-id="ccb6c-138">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="ccb6c-138">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="ccb6c-139">IID</span><span class="sxs-lookup"><span data-stu-id="ccb6c-139">IID</span></span><br/>                      | <span data-ttu-id="ccb6c-140">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="ccb6c-140">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="ccb6c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccb6c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb6c-142">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="ccb6c-142">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




