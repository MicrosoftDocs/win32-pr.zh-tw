---
description: 指定編解碼器在編碼時是否應該使用保守感知優化。
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: 'MFPKEY_PERCEPTUALOPTLEVEL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192248"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="c6e50-103">MFPKEY \_ PERCEPTUALOPTLEVEL 屬性</span><span class="sxs-lookup"><span data-stu-id="c6e50-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="c6e50-104">指定編解碼器在編碼時是否應該使用保守感知優化。</span><span class="sxs-lookup"><span data-stu-id="c6e50-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c6e50-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="c6e50-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c6e50-106">g \_ wszWMVCPerceptualOptLevel</span><span class="sxs-lookup"><span data-stu-id="c6e50-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="c6e50-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c6e50-107">Data Type</span></span>

<span data-ttu-id="c6e50-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c6e50-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c6e50-109">預設值</span><span class="sxs-lookup"><span data-stu-id="c6e50-109">Default Value</span></span>

<span data-ttu-id="c6e50-110">0</span><span class="sxs-lookup"><span data-stu-id="c6e50-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e50-111">備註</span><span class="sxs-lookup"><span data-stu-id="c6e50-111">Remarks</span></span>

<span data-ttu-id="c6e50-112">保守感知優化是編解碼器嘗試在影片框架中識別「重要」和「不重要」區域的程式。</span><span class="sxs-lookup"><span data-stu-id="c6e50-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="c6e50-113">在識別出這些框架區域之後，編解碼器會在重要區域品質的同時提供較高的優先順序，而不重要的區域品質。</span><span class="sxs-lookup"><span data-stu-id="c6e50-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="c6e50-114">感知優化強調讓影像看起來是正確的，而不是工作嚴格的數學精確度。</span><span class="sxs-lookup"><span data-stu-id="c6e50-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="c6e50-115">根據所編碼的影片類型而定，優化的結果會有很大的差別。</span><span class="sxs-lookup"><span data-stu-id="c6e50-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="c6e50-116">這項功能非常適合低位速率和低解析度的編碼 (例如，web 串流) ，但在適用于封存影片品質的情況下，最好避免這樣做。</span><span class="sxs-lookup"><span data-stu-id="c6e50-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e50-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6e50-117">Requirements</span></span>



| <span data-ttu-id="c6e50-118">需求</span><span class="sxs-lookup"><span data-stu-id="c6e50-118">Requirement</span></span> | <span data-ttu-id="c6e50-119">值</span><span class="sxs-lookup"><span data-stu-id="c6e50-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e50-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6e50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e50-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6e50-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6e50-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6e50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e50-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6e50-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6e50-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c6e50-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e50-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e50-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e50-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6e50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e50-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c6e50-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




