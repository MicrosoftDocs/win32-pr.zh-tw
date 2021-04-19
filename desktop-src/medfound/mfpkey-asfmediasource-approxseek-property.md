---
description: 指定 ASF 媒體來源是否使用近似搜尋。
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: 'MFPKEY_ASFMediaSource_ApproxSeek 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989123"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a><span data-ttu-id="946e8-103">MFPKEY \_ ASFMediaSource \_ ApproxSeek 屬性</span><span class="sxs-lookup"><span data-stu-id="946e8-103">MFPKEY\_ASFMediaSource\_ApproxSeek property</span></span>

<span data-ttu-id="946e8-104">指定 ASF 媒體來源是否使用近似搜尋。</span><span class="sxs-lookup"><span data-stu-id="946e8-104">Specifies whether the ASF media source uses approximate seeking.</span></span>



<span data-ttu-id="946e8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="946e8-105">Data type</span></span>

<span data-ttu-id="946e8-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="946e8-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="946e8-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="946e8-107">PROPVARIANT member</span></span>

<span data-ttu-id="946e8-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="946e8-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="946e8-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="946e8-109">VT\_BOOL</span></span>

<span data-ttu-id="946e8-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="946e8-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="946e8-111">備註</span><span class="sxs-lookup"><span data-stu-id="946e8-111">Remarks</span></span>

<span data-ttu-id="946e8-112">應用程式可以使用這個屬性來設定 ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="946e8-112">Applications can use this property to configure the ASF media source.</span></span> <span data-ttu-id="946e8-113">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="946e8-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="946e8-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="946e8-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="946e8-115">ASF 媒體來源處理搜尋的方式如下：</span><span class="sxs-lookup"><span data-stu-id="946e8-115">The ASF media source handles seeking as follows:</span></span>

-   <span data-ttu-id="946e8-116">如果這個屬性的值為 **VARIANT \_ TRUE**，則媒體來源會使用近似的搜尋，其精確度較低，但比確切搜尋更快。</span><span class="sxs-lookup"><span data-stu-id="946e8-116">If the value of this property is **VARIANT\_TRUE**, the media source uses approximate seeking, which is less accurate but faster than exact seeking.</span></span>
-   <span data-ttu-id="946e8-117">如果此值為 **VARIANT \_ FALSE** ，且 ASF 檔案有索引，則媒體來源會使用精確的搜尋。</span><span class="sxs-lookup"><span data-stu-id="946e8-117">If the value is **VARIANT\_FALSE** and the ASF file has an index, the media source uses exact seeking.</span></span>
-   <span data-ttu-id="946e8-118">如果 ASF 檔案不包含索引，除非 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) 屬性設定為 **VARIANT \_ TRUE**，否則媒體來源會使用 approxmate 搜尋。</span><span class="sxs-lookup"><span data-stu-id="946e8-118">If the ASF file does not contain an index, the media source uses approxmate seeking unless the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is set to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="946e8-119">如果 ASF 檔案未包含索引，且 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) 屬性為 **VARIANT \_ TRUE**，則媒體來源會使用反復搜尋。</span><span class="sxs-lookup"><span data-stu-id="946e8-119">If the ASF file does not contain an index and the [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) property is **VARIANT\_TRUE**, the media source uses iterative seeking.</span></span> <span data-ttu-id="946e8-120">反復搜尋的精確度較高，但比近似搜尋 (更慢，但通常不如搜尋) 精確。</span><span class="sxs-lookup"><span data-stu-id="946e8-120">Iterative seeking is more accurate but slower than approximate seeking (but generally less accurate than exact seeking).</span></span>
    > [!Note]  
    > <span data-ttu-id="946e8-121">需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="946e8-121">Requires Windows 7.</span></span>

     

<span data-ttu-id="946e8-122">這個屬性的預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="946e8-122">The default value of this property is **VARIANT\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="946e8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="946e8-123">Requirements</span></span>



| <span data-ttu-id="946e8-124">需求</span><span class="sxs-lookup"><span data-stu-id="946e8-124">Requirement</span></span> | <span data-ttu-id="946e8-125">值</span><span class="sxs-lookup"><span data-stu-id="946e8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="946e8-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="946e8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="946e8-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="946e8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="946e8-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="946e8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="946e8-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="946e8-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="946e8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="946e8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="946e8-131"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="946e8-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946e8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="946e8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946e8-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="946e8-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




