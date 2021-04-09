---
description: 您可以使用 SWbemNamedValueSet 物件的 Count 屬性來判斷集合中有多少個專案。 這是唯讀的屬性。
ms.assetid: 4086cf91-69cd-4bce-a6e0-f223b18cd18d
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet： Count 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Count
- ISWbemNamedValueSet.Count
- ISWbemNamedValueSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a32602ebcc279685ff1d1e2e6c837d1a39b7a8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848625"
---
# <a name="swbemnamedvaluesetcount-property"></a><span data-ttu-id="a622d-104">SWbemNamedValueSet Count 屬性</span><span class="sxs-lookup"><span data-stu-id="a622d-104">SWbemNamedValueSet.Count property</span></span>

<span data-ttu-id="a622d-105">您可以使用 [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **Count** 屬性來判斷集合中有多少個專案。</span><span class="sxs-lookup"><span data-stu-id="a622d-105">Use the **Count** property of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object to determine how many items are in the collection.</span></span> <span data-ttu-id="a622d-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="a622d-106">This property is read-only.</span></span>

<span data-ttu-id="a622d-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="a622d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a622d-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a622d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a622d-109">語法</span><span class="sxs-lookup"><span data-stu-id="a622d-109">Syntax</span></span>


```VB
SWbemNamedValueSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="a622d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a622d-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a622d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a622d-111">Requirements</span></span>



| <span data-ttu-id="a622d-112">需求</span><span class="sxs-lookup"><span data-stu-id="a622d-112">Requirement</span></span> | <span data-ttu-id="a622d-113">值</span><span class="sxs-lookup"><span data-stu-id="a622d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a622d-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a622d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a622d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a622d-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a622d-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a622d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a622d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a622d-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a622d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a622d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a622d-119"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="a622d-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a622d-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a622d-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="a622d-121"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a622d-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a622d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a622d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a622d-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a622d-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a622d-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="a622d-124">CLSID</span></span><br/>                    | <span data-ttu-id="a622d-125">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="a622d-125">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="a622d-126">IID</span><span class="sxs-lookup"><span data-stu-id="a622d-126">IID</span></span><br/>                      | <span data-ttu-id="a622d-127">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="a622d-127">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="a622d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a622d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a622d-129">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="a622d-129">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




