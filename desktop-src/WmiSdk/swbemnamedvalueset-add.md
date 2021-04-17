---
description: SWbemNamedValueSet 物件的 Add 方法會將 SWbemNamedValue 物件加入至集合。 如果專案已經存在相同名稱的集合中，則新的元素會取代它。
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512981"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="15eaf-104">SWbemNamedValueSet 新增方法</span><span class="sxs-lookup"><span data-stu-id="15eaf-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="15eaf-105">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Add** 方法會將 [**SWbemNamedValue**](swbemnamedvalue.md)物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="15eaf-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="15eaf-106">如果專案已經存在相同名稱的集合中，則新的元素會取代它。</span><span class="sxs-lookup"><span data-stu-id="15eaf-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="15eaf-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="15eaf-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15eaf-108">語法</span><span class="sxs-lookup"><span data-stu-id="15eaf-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="15eaf-109">參數</span><span class="sxs-lookup"><span data-stu-id="15eaf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15eaf-110">*strName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15eaf-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15eaf-111">必要。</span><span class="sxs-lookup"><span data-stu-id="15eaf-111">Required.</span></span> <span data-ttu-id="15eaf-112">新值的名稱。</span><span class="sxs-lookup"><span data-stu-id="15eaf-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="15eaf-113">*varVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15eaf-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15eaf-114">必要。</span><span class="sxs-lookup"><span data-stu-id="15eaf-114">Required.</span></span> <span data-ttu-id="15eaf-115">表示新值的 Variant。</span><span class="sxs-lookup"><span data-stu-id="15eaf-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="15eaf-116">*iFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="15eaf-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15eaf-117">如果有指定，則必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="15eaf-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15eaf-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="15eaf-118">Return value</span></span>

<span data-ttu-id="15eaf-119">如果成功，這個方法會傳回新修改或新建立的 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="15eaf-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="15eaf-120">備註</span><span class="sxs-lookup"><span data-stu-id="15eaf-120">Remarks</span></span>

<span data-ttu-id="15eaf-121">如需新增和取出命名值的範例，請參閱 [**SWbemNamedValue。**](swbemnamedvalue-value.md)</span><span class="sxs-lookup"><span data-stu-id="15eaf-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15eaf-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="15eaf-122">Requirements</span></span>



| <span data-ttu-id="15eaf-123">需求</span><span class="sxs-lookup"><span data-stu-id="15eaf-123">Requirement</span></span> | <span data-ttu-id="15eaf-124">值</span><span class="sxs-lookup"><span data-stu-id="15eaf-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15eaf-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15eaf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="15eaf-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15eaf-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15eaf-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15eaf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="15eaf-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15eaf-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15eaf-129">標頭</span><span class="sxs-lookup"><span data-stu-id="15eaf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="15eaf-130"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="15eaf-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15eaf-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="15eaf-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="15eaf-132"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15eaf-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15eaf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="15eaf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15eaf-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15eaf-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15eaf-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="15eaf-135">CLSID</span></span><br/>                    | <span data-ttu-id="15eaf-136">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="15eaf-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="15eaf-137">IID</span><span class="sxs-lookup"><span data-stu-id="15eaf-137">IID</span></span><br/>                      | <span data-ttu-id="15eaf-138">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="15eaf-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="15eaf-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15eaf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15eaf-140">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="15eaf-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




