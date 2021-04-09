---
description: SWbemRefreshableItem 物件屬性代表重新整理的單一 SWbemObject 實例。 專案包含在 SWbemRefresher 物件中。重新整理的 SWbemObject 實例。 專案包含在 SWbemRefresher 物件中。
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem 物件屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945640"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="6edba-105">SWbemRefreshableItem 物件屬性</span><span class="sxs-lookup"><span data-stu-id="6edba-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="6edba-106">**SWbemRefreshableItem 物件** 屬性代表重新整理的單一 [**SWbemObject**](swbemobject.md)實例。</span><span class="sxs-lookup"><span data-stu-id="6edba-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="6edba-107">專案包含在 [**SWbemRefresher**](swbemrefresher.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="6edba-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="6edba-108">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="6edba-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6edba-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6edba-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edba-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edba-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="6edba-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="6edba-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="6edba-112">備註</span><span class="sxs-lookup"><span data-stu-id="6edba-112">Remarks</span></span>

<span data-ttu-id="6edba-113">除非 [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md)為 **FALSE**，否則此屬性為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6edba-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edba-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6edba-114">Requirements</span></span>



| <span data-ttu-id="6edba-115">需求</span><span class="sxs-lookup"><span data-stu-id="6edba-115">Requirement</span></span> | <span data-ttu-id="6edba-116">值</span><span class="sxs-lookup"><span data-stu-id="6edba-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6edba-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6edba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6edba-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6edba-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6edba-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6edba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6edba-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6edba-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6edba-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6edba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edba-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6edba-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6edba-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6edba-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6edba-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6edba-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6edba-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6edba-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6edba-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6edba-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6edba-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="6edba-127">CLSID</span></span><br/>                    | <span data-ttu-id="6edba-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="6edba-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="6edba-129">IID</span><span class="sxs-lookup"><span data-stu-id="6edba-129">IID</span></span><br/>                      | <span data-ttu-id="6edba-130">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="6edba-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="6edba-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6edba-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edba-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="6edba-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="6edba-133">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="6edba-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




