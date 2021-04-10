---
description: 指定如何在移動搜尋作業中使用色彩資訊。
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: 'MFPKEY_MOTIONSEARCHLEVEL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026570"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="222cb-103">MFPKEY \_ MOTIONSEARCHLEVEL 屬性</span><span class="sxs-lookup"><span data-stu-id="222cb-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="222cb-104">指定如何在移動搜尋作業中使用色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="222cb-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="222cb-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="222cb-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="222cb-106">g \_ wszWMVCMotionSearchLevel</span><span class="sxs-lookup"><span data-stu-id="222cb-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="222cb-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="222cb-107">Data Type</span></span>

<span data-ttu-id="222cb-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="222cb-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="222cb-109">預設值</span><span class="sxs-lookup"><span data-stu-id="222cb-109">Default Value</span></span>

<span data-ttu-id="222cb-110">0</span><span class="sxs-lookup"><span data-stu-id="222cb-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="222cb-111">備註</span><span class="sxs-lookup"><span data-stu-id="222cb-111">Remarks</span></span>

<span data-ttu-id="222cb-112">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="222cb-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="222cb-113">值</span><span class="sxs-lookup"><span data-stu-id="222cb-113">Value</span></span> | <span data-ttu-id="222cb-114">使用的影片資訊</span><span class="sxs-lookup"><span data-stu-id="222cb-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="222cb-115">0</span><span class="sxs-lookup"><span data-stu-id="222cb-115">0</span></span>     | <span data-ttu-id="222cb-116">僅 Luma。</span><span class="sxs-lookup"><span data-stu-id="222cb-116">Luma only.</span></span>                                       |
| <span data-ttu-id="222cb-117">1</span><span class="sxs-lookup"><span data-stu-id="222cb-117">1</span></span>     | <span data-ttu-id="222cb-118">具有最接近整數色度的 Luma。</span><span class="sxs-lookup"><span data-stu-id="222cb-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="222cb-119">2</span><span class="sxs-lookup"><span data-stu-id="222cb-119">2</span></span>     | <span data-ttu-id="222cb-120">Luma 與真實色度。</span><span class="sxs-lookup"><span data-stu-id="222cb-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="222cb-121">-1</span><span class="sxs-lookup"><span data-stu-id="222cb-121">-1</span></span>    | <span data-ttu-id="222cb-122">巨大區塊-使用 true 色度的彈性。</span><span class="sxs-lookup"><span data-stu-id="222cb-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="222cb-123">-2</span><span class="sxs-lookup"><span data-stu-id="222cb-123">-2</span></span>    | <span data-ttu-id="222cb-124">巨大區塊-具有最接近整數色度的彈性。</span><span class="sxs-lookup"><span data-stu-id="222cb-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="222cb-125">根據預設，編解碼器只會在 luma 頻道中執行動作搜尋。</span><span class="sxs-lookup"><span data-stu-id="222cb-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="222cb-126">在移動估計中包含色度資訊可大幅提升編碼影片的品質。</span><span class="sxs-lookup"><span data-stu-id="222cb-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="222cb-127">使用 luma 和 true 色度的動作搜尋會產生最佳的影片品質，但最高的效能成本。</span><span class="sxs-lookup"><span data-stu-id="222cb-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="222cb-128">這兩個動態模式 (-1 和-2) ，而具有最接近整數色度模式的 luma，將可提供品質與效能之間合理的折衷。</span><span class="sxs-lookup"><span data-stu-id="222cb-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="222cb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="222cb-129">Requirements</span></span>



| <span data-ttu-id="222cb-130">需求</span><span class="sxs-lookup"><span data-stu-id="222cb-130">Requirement</span></span> | <span data-ttu-id="222cb-131">值</span><span class="sxs-lookup"><span data-stu-id="222cb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="222cb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="222cb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="222cb-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="222cb-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="222cb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="222cb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="222cb-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="222cb-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="222cb-136">標頭</span><span class="sxs-lookup"><span data-stu-id="222cb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="222cb-137"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="222cb-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="222cb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="222cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222cb-139">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="222cb-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




