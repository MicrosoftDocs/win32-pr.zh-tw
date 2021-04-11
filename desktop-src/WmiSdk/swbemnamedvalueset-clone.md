---
description: SWbemNamedValueSet 物件的 Clone 方法會傳回新的物件，這個物件是目前集合的複製。
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 複製方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693291"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="f4599-103">SWbemNamedValueSet 複製方法</span><span class="sxs-lookup"><span data-stu-id="f4599-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="f4599-104">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **clone** 方法會傳回新的物件，這個物件是目前集合的複製。</span><span class="sxs-lookup"><span data-stu-id="f4599-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="f4599-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="f4599-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4599-106">語法</span><span class="sxs-lookup"><span data-stu-id="f4599-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="f4599-107">參數</span><span class="sxs-lookup"><span data-stu-id="f4599-107">Parameters</span></span>

<span data-ttu-id="f4599-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f4599-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4599-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4599-109">Return value</span></span>

<span data-ttu-id="f4599-110">如果成功，則會傳回新的 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f4599-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4599-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f4599-111">Error codes</span></span>

<span data-ttu-id="f4599-112">**複製** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f4599-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="f4599-113">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="f4599-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f4599-114">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f4599-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f4599-115">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="f4599-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f4599-116">記憶體不足，無法複製物件。</span><span class="sxs-lookup"><span data-stu-id="f4599-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4599-117">備註</span><span class="sxs-lookup"><span data-stu-id="f4599-117">Remarks</span></span>

<span data-ttu-id="f4599-118">您可以使用這個方法來複製 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="f4599-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4599-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4599-119">Requirements</span></span>



| <span data-ttu-id="f4599-120">需求</span><span class="sxs-lookup"><span data-stu-id="f4599-120">Requirement</span></span> | <span data-ttu-id="f4599-121">值</span><span class="sxs-lookup"><span data-stu-id="f4599-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4599-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4599-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4599-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4599-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4599-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4599-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4599-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4599-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4599-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f4599-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4599-127"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4599-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4599-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f4599-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4599-129"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f4599-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f4599-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f4599-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4599-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4599-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4599-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="f4599-132">CLSID</span></span><br/>                    | <span data-ttu-id="f4599-133">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="f4599-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="f4599-134">IID</span><span class="sxs-lookup"><span data-stu-id="f4599-134">IID</span></span><br/>                      | <span data-ttu-id="f4599-135">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="f4599-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="f4599-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4599-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4599-137">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="f4599-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




