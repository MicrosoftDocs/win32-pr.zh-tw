---
description: 指定編解碼器應減少影片有效色彩範圍的程度。
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: 'MFPKEY_RANGEREDUX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988742"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="48877-103">MFPKEY \_ RANGEREDUX 屬性</span><span class="sxs-lookup"><span data-stu-id="48877-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="48877-104">指定編解碼器應減少影片有效色彩範圍的程度。</span><span class="sxs-lookup"><span data-stu-id="48877-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="48877-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="48877-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="48877-106">g \_ wszWMVCRangeRedux</span><span class="sxs-lookup"><span data-stu-id="48877-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="48877-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="48877-107">Data Type</span></span>

<span data-ttu-id="48877-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="48877-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="48877-109">預設值</span><span class="sxs-lookup"><span data-stu-id="48877-109">Default Value</span></span>

<span data-ttu-id="48877-110">0</span><span class="sxs-lookup"><span data-stu-id="48877-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="48877-111">備註</span><span class="sxs-lookup"><span data-stu-id="48877-111">Remarks</span></span>

<span data-ttu-id="48877-112">範圍縮減：指定編解碼器應減少影片 luma 和色度範圍的程度。</span><span class="sxs-lookup"><span data-stu-id="48877-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="48877-113">減少範圍可減少編碼的影片畫面大小，但也會降低影片的色彩細節。</span><span class="sxs-lookup"><span data-stu-id="48877-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="48877-114">縮小範圍的方式包括：編碼期間的縮減，以及解碼期間的擴充。</span><span class="sxs-lookup"><span data-stu-id="48877-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="48877-115">您可以使擴充因素與減少因數不同，但不建議在範圍重新對應很實用的大部分案例中使用。</span><span class="sxs-lookup"><span data-stu-id="48877-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="48877-116">範圍縮減和展開會在 luma 和色度通道上分開執行。</span><span class="sxs-lookup"><span data-stu-id="48877-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="48877-117">減少範圍可能是降低低位速率影片複雜性的有效方法，而不會犧牲影像詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48877-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="48877-118">將全部四個值設定為8，可將 luma 和色度資訊的數量降到一半，讓更多的位被導向以保留影像詳細資料。</span><span class="sxs-lookup"><span data-stu-id="48877-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="48877-119">編解碼器可以選擇在以非常低的位元速率編碼影片時自動使用範圍減少。</span><span class="sxs-lookup"><span data-stu-id="48877-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="48877-120">將全部四個值設定為0，可完全停用範圍減少，即使是低位速率的案例也一樣。</span><span class="sxs-lookup"><span data-stu-id="48877-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="48877-121">減少色彩範圍可減少影片框架的編碼大小，但可以在已解碼的框架中引進 blurriness。</span><span class="sxs-lookup"><span data-stu-id="48877-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="48877-122">如果未設定此屬性，則編解碼器會決定是否要在編碼時間使用範圍減少。</span><span class="sxs-lookup"><span data-stu-id="48877-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="48877-123">此選項通常只會以低位費率由編解碼器選取。</span><span class="sxs-lookup"><span data-stu-id="48877-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="48877-124">這個屬性的值是四個元件的組合（以零分隔），格式為0x0M0m0N0n，其中：</span><span class="sxs-lookup"><span data-stu-id="48877-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="48877-125">M 是 Y 元件的編碼範圍減少因數。</span><span class="sxs-lookup"><span data-stu-id="48877-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="48877-126">m 是 Y 元件的解碼範圍展開因數 (通常與 M) 相同。</span><span class="sxs-lookup"><span data-stu-id="48877-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="48877-127">N 是 UV 元件的編碼範圍減少因數。</span><span class="sxs-lookup"><span data-stu-id="48877-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="48877-128">n 是 UV 元件的解碼範圍展開因數 (通常與 N) 相同。</span><span class="sxs-lookup"><span data-stu-id="48877-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="48877-129">每個因素都是從0到8的數位，其中0不是縮減或展開，而8是最大縮減或擴大。</span><span class="sxs-lookup"><span data-stu-id="48877-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="48877-130">如果您將值設定為0x00000000，則會完全停用範圍減少。</span><span class="sxs-lookup"><span data-stu-id="48877-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="48877-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="48877-131">Requirements</span></span>



| <span data-ttu-id="48877-132">需求</span><span class="sxs-lookup"><span data-stu-id="48877-132">Requirement</span></span> | <span data-ttu-id="48877-133">值</span><span class="sxs-lookup"><span data-stu-id="48877-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48877-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48877-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48877-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48877-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="48877-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48877-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48877-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48877-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="48877-138">標頭</span><span class="sxs-lookup"><span data-stu-id="48877-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="48877-139"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="48877-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48877-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48877-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48877-141">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="48877-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




