---
description: SWbemRefreshableItem. IsSet 屬性是布林值，指出 SWbemRefreshableItem 物件是否代表單一物件或物件集。SWbemRefreshableItem 物件代表單一物件或物件集。
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem. IsSet 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998943"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="74f7d-103">SWbemRefreshableItem. IsSet 屬性</span><span class="sxs-lookup"><span data-stu-id="74f7d-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="74f7d-104">**SWbemRefreshableItem. IsSet** 屬性是布林值，指出 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件是否代表單一物件或物件集。</span><span class="sxs-lookup"><span data-stu-id="74f7d-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="74f7d-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="74f7d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="74f7d-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="74f7d-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f7d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f7d-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="74f7d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="74f7d-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="74f7d-109">備註</span><span class="sxs-lookup"><span data-stu-id="74f7d-109">Remarks</span></span>

<span data-ttu-id="74f7d-110">如果 **SWbemRefreshableItem** 為 **TRUE**，則專案代表 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件，且 [**物件**](swbemrefreshableitem-object.md) 屬性將會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74f7d-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="74f7d-111">如果 **為 FALSE**，則表示專案代表 [**SWbemObject**](swbemobject.md) 物件，而 **物件** 屬性為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="74f7d-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f7d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="74f7d-112">Requirements</span></span>



| <span data-ttu-id="74f7d-113">需求</span><span class="sxs-lookup"><span data-stu-id="74f7d-113">Requirement</span></span> | <span data-ttu-id="74f7d-114">值</span><span class="sxs-lookup"><span data-stu-id="74f7d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74f7d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74f7d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="74f7d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74f7d-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74f7d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74f7d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="74f7d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74f7d-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74f7d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="74f7d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f7d-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="74f7d-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74f7d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="74f7d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="74f7d-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74f7d-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74f7d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="74f7d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74f7d-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74f7d-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74f7d-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="74f7d-125">CLSID</span></span><br/>                    | <span data-ttu-id="74f7d-126">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="74f7d-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="74f7d-127">IID</span><span class="sxs-lookup"><span data-stu-id="74f7d-127">IID</span></span><br/>                      | <span data-ttu-id="74f7d-128">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="74f7d-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="74f7d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74f7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f7d-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="74f7d-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="74f7d-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="74f7d-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




