---
description: SWbemRefreshableItem. ObjectSet 屬性代表要重新整理的物件集。
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem. ObjectSet 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321531"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="90037-103">SWbemRefreshableItem. ObjectSet 屬性</span><span class="sxs-lookup"><span data-stu-id="90037-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="90037-104">**SWbemRefreshableItem. ObjectSet** 屬性代表要重新整理的物件集。</span><span class="sxs-lookup"><span data-stu-id="90037-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="90037-105">**ObjectSet** 屬性是包含在 [**SWbemRefresher**](swbemrefresher.md)物件中的列舉值或收集項。</span><span class="sxs-lookup"><span data-stu-id="90037-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="90037-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="90037-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="90037-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="90037-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="90037-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="90037-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="90037-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="90037-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="90037-110">備註</span><span class="sxs-lookup"><span data-stu-id="90037-110">Remarks</span></span>

<span data-ttu-id="90037-111">除非 [**SWbemRefreshableItem**](swbemrefreshableitem-isset.md)為 **TRUE**，否則此屬性為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="90037-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="90037-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="90037-112">Requirements</span></span>



| <span data-ttu-id="90037-113">需求</span><span class="sxs-lookup"><span data-stu-id="90037-113">Requirement</span></span> | <span data-ttu-id="90037-114">值</span><span class="sxs-lookup"><span data-stu-id="90037-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90037-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90037-115">Minimum supported client</span></span><br/> | <span data-ttu-id="90037-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90037-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90037-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90037-117">Minimum supported server</span></span><br/> | <span data-ttu-id="90037-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90037-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90037-119">標頭</span><span class="sxs-lookup"><span data-stu-id="90037-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90037-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="90037-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="90037-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="90037-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="90037-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="90037-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="90037-123">DLL</span><span class="sxs-lookup"><span data-stu-id="90037-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90037-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90037-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="90037-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="90037-125">CLSID</span></span><br/>                    | <span data-ttu-id="90037-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="90037-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="90037-127">IID</span><span class="sxs-lookup"><span data-stu-id="90037-127">IID</span></span><br/>                      | <span data-ttu-id="90037-128">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="90037-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="90037-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90037-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90037-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="90037-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="90037-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="90037-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




