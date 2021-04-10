---
description: 包含媒體基礎轉換 (MFT) 的分類 GUID。
ms.assetid: 3c0948fc-42ea-4e43-a312-c98038020214
title: 'MFPKEY_CATEGORY 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbb83ab2c824ff9a4510e520b13c49ae5b3a52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849520"
---
# <a name="mfpkey_category-property"></a><span data-ttu-id="e7eba-103">MFPKEY \_ CATEGORY 屬性</span><span class="sxs-lookup"><span data-stu-id="e7eba-103">MFPKEY\_CATEGORY property</span></span>

<span data-ttu-id="e7eba-104">包含媒體基礎轉換 (MFT) 的分類 GUID。</span><span class="sxs-lookup"><span data-stu-id="e7eba-104">Contains the category GUID for a Media Foundation transform (MFT).</span></span>



<span data-ttu-id="e7eba-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e7eba-105">Data type</span></span>

<span data-ttu-id="e7eba-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="e7eba-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e7eba-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="e7eba-107">PROPVARIANT member</span></span>

<span data-ttu-id="e7eba-108"> (**CLSID** \*) 的 GUID</span><span class="sxs-lookup"><span data-stu-id="e7eba-108">**GUID** (**CLSID**\*)</span></span>

<span data-ttu-id="e7eba-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="e7eba-109">VT\_CLSID</span></span>

<span data-ttu-id="e7eba-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="e7eba-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="e7eba-111">備註</span><span class="sxs-lookup"><span data-stu-id="e7eba-111">Remarks</span></span>

<span data-ttu-id="e7eba-112">這個屬性的值是可識別 MFT 類別目錄的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e7eba-112">The value of this property is a GUID that identifies the MFT category.</span></span> <span data-ttu-id="e7eba-113">如需分類清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。</span><span class="sxs-lookup"><span data-stu-id="e7eba-113">For a list of categories, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

<span data-ttu-id="e7eba-114">這個屬性是選擇性的，且僅供參考。</span><span class="sxs-lookup"><span data-stu-id="e7eba-114">This property is optional and is informational only.</span></span> <span data-ttu-id="e7eba-115">MFT 可以使用這個屬性來報告註冊它的類別。</span><span class="sxs-lookup"><span data-stu-id="e7eba-115">An MFT can use this property to report the category under which it is registered.</span></span> <span data-ttu-id="e7eba-116">若要取得此屬性，請查詢 **IPropertyStore** 介面的 MFT。</span><span class="sxs-lookup"><span data-stu-id="e7eba-116">To get this property, query the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="e7eba-117">若要列舉 MFT 類別，請呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數。</span><span class="sxs-lookup"><span data-stu-id="e7eba-117">To enumerate an MFT category, call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function.</span></span> <span data-ttu-id="e7eba-118">**MFTEnum** 函式與這個屬性之間沒有直接連結。</span><span class="sxs-lookup"><span data-stu-id="e7eba-118">There is no direct link between the **MFTEnum** function and this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7eba-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7eba-119">Requirements</span></span>



| <span data-ttu-id="e7eba-120">需求</span><span class="sxs-lookup"><span data-stu-id="e7eba-120">Requirement</span></span> | <span data-ttu-id="e7eba-121">值</span><span class="sxs-lookup"><span data-stu-id="e7eba-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7eba-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7eba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7eba-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7eba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7eba-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7eba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7eba-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7eba-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e7eba-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e7eba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7eba-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7eba-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7eba-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7eba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7eba-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e7eba-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e7eba-130">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="e7eba-130">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




