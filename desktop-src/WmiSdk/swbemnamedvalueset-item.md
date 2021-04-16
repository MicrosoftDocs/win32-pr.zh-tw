---
description: SWbemNamedValueSet 物件的 Item 方法會從集合取得 SWbemNamedValue 物件。
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512980"
---
# <a name="swbemnamedvaluesetitem-method"></a><span data-ttu-id="17e37-103">SWbemNamedValueSet 專案方法</span><span class="sxs-lookup"><span data-stu-id="17e37-103">SWbemNamedValueSet.Item method</span></span>

<span data-ttu-id="17e37-104">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Item** 方法會從集合取得 [**SWbemNamedValue**](swbemnamedvalue.md)物件。</span><span class="sxs-lookup"><span data-stu-id="17e37-104">The **Item** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object gets an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span>

<span data-ttu-id="17e37-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="17e37-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17e37-106">語法</span><span class="sxs-lookup"><span data-stu-id="17e37-106">Syntax</span></span>


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="17e37-107">參數</span><span class="sxs-lookup"><span data-stu-id="17e37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e37-108">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17e37-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17e37-109">必要。</span><span class="sxs-lookup"><span data-stu-id="17e37-109">Required.</span></span> <span data-ttu-id="17e37-110">要取出的值名稱。</span><span class="sxs-lookup"><span data-stu-id="17e37-110">Name of the value to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="17e37-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="17e37-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17e37-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="17e37-112">Reserved.</span></span> <span data-ttu-id="17e37-113">如果有指定，此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="17e37-113">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e37-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="17e37-114">Return value</span></span>

<span data-ttu-id="17e37-115">如果成功，則會傳回要求的 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="17e37-115">If successful, the requested [**SWbemNamedValue**](swbemnamedvalue.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="17e37-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="17e37-116">Error codes</span></span>

<span data-ttu-id="17e37-117">當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="17e37-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="17e37-118">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="17e37-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="17e37-119">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="17e37-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="17e37-120">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="17e37-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="17e37-121">指定的參數無效，或無法剖析命名空間。</span><span class="sxs-lookup"><span data-stu-id="17e37-121">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="17e37-122">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="17e37-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="17e37-123">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="17e37-123">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="17e37-124">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="17e37-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="17e37-125">找不到要求的項目。</span><span class="sxs-lookup"><span data-stu-id="17e37-125">The requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17e37-126">備註</span><span class="sxs-lookup"><span data-stu-id="17e37-126">Remarks</span></span>

<span data-ttu-id="17e37-127">如需新增和取出命名值的範例，請參閱 [**SWbemNamedValue。**](swbemnamedvalue-value.md)</span><span class="sxs-lookup"><span data-stu-id="17e37-127">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17e37-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="17e37-128">Requirements</span></span>



| <span data-ttu-id="17e37-129">需求</span><span class="sxs-lookup"><span data-stu-id="17e37-129">Requirement</span></span> | <span data-ttu-id="17e37-130">值</span><span class="sxs-lookup"><span data-stu-id="17e37-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17e37-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17e37-131">Minimum supported client</span></span><br/> | <span data-ttu-id="17e37-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17e37-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17e37-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17e37-133">Minimum supported server</span></span><br/> | <span data-ttu-id="17e37-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17e37-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17e37-135">標頭</span><span class="sxs-lookup"><span data-stu-id="17e37-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="17e37-136"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="17e37-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17e37-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17e37-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="17e37-138"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17e37-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17e37-139">DLL</span><span class="sxs-lookup"><span data-stu-id="17e37-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17e37-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17e37-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="17e37-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="17e37-141">CLSID</span></span><br/>                    | <span data-ttu-id="17e37-142">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="17e37-142">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="17e37-143">IID</span><span class="sxs-lookup"><span data-stu-id="17e37-143">IID</span></span><br/>                      | <span data-ttu-id="17e37-144">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="17e37-144">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="17e37-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17e37-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e37-146">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="17e37-146">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




