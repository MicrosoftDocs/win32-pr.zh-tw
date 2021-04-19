---
description: SWbemMethodSet 物件的 Item 方法會從集合傳回名為 SWbemMethod 的物件。
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: 'SWbemMethodSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986837"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="f2a7c-103">SWbemMethodSet 專案方法</span><span class="sxs-lookup"><span data-stu-id="f2a7c-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="f2a7c-104">[**SWbemMethodSet**](swbemmethodset.md)物件的 **Item** 方法會從集合傳回名為 [**SWbemMethod**](swbemmethod.md)的物件。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="f2a7c-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a7c-106">語法</span><span class="sxs-lookup"><span data-stu-id="f2a7c-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2a7c-107">參數</span><span class="sxs-lookup"><span data-stu-id="f2a7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2a7c-108">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2a7c-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a7c-109">必要。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-109">Required.</span></span> <span data-ttu-id="f2a7c-110">要取出之方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f2a7c-111">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f2a7c-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2a7c-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-112">Reserved.</span></span> <span data-ttu-id="f2a7c-113">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2a7c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2a7c-114">Return value</span></span>

<span data-ttu-id="f2a7c-115">如果成功，要求的 [**SWbemMethod**](swbemmethod.md) 物件就會傳回。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2a7c-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f2a7c-116">Error codes</span></span>

<span data-ttu-id="f2a7c-117">當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f2a7c-118">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="f2a7c-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f2a7c-119">*IFlags* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f2a7c-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="f2a7c-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="f2a7c-121">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f2a7c-122">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="f2a7c-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f2a7c-123">指定的方法不存在。</span><span class="sxs-lookup"><span data-stu-id="f2a7c-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2a7c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2a7c-124">Requirements</span></span>



| <span data-ttu-id="f2a7c-125">需求</span><span class="sxs-lookup"><span data-stu-id="f2a7c-125">Requirement</span></span> | <span data-ttu-id="f2a7c-126">值</span><span class="sxs-lookup"><span data-stu-id="f2a7c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a7c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2a7c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a7c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2a7c-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2a7c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2a7c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a7c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2a7c-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2a7c-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f2a7c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2a7c-132"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7c-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2a7c-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f2a7c-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2a7c-134"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7c-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2a7c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a7c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a7c-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2a7c-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2a7c-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2a7c-137">CLSID</span></span><br/>                    | <span data-ttu-id="f2a7c-138">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="f2a7c-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="f2a7c-139">IID</span><span class="sxs-lookup"><span data-stu-id="f2a7c-139">IID</span></span><br/>                      | <span data-ttu-id="f2a7c-140">IID \_ ISWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="f2a7c-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="f2a7c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2a7c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a7c-142">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="f2a7c-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="f2a7c-143">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="f2a7c-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




