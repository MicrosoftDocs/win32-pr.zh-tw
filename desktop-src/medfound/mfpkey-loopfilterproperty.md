---
description: 指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: 'MFPKEY_LOOPFILTER 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988743"
---
# <a name="mfpkey_loopfilter-property"></a><span data-ttu-id="ee8ea-103">MFPKEY \_ LOOPFILTER 屬性</span><span class="sxs-lookup"><span data-stu-id="ee8ea-103">MFPKEY\_LOOPFILTER Property</span></span>

<span data-ttu-id="ee8ea-104">指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-104">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ee8ea-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ee8ea-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ee8ea-106">g \_ wszWMVCLoopFilter</span><span class="sxs-lookup"><span data-stu-id="ee8ea-106">g\_wszWMVCLoopFilter</span></span>

## <a name="data-type"></a><span data-ttu-id="ee8ea-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ee8ea-107">Data Type</span></span>

<span data-ttu-id="ee8ea-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ee8ea-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="ee8ea-109">備註</span><span class="sxs-lookup"><span data-stu-id="ee8ea-109">Remarks</span></span>

<span data-ttu-id="ee8ea-110">「迴圈中」篩選器是一種在編碼和解碼期間套用的 deblocking 方法，可在編碼時間減少封鎖成品 ( 「在迴圈中」 ) ，讓未來的 P 框架和 B 框架不會將這些專案向前推進。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-110">The in-loop filter is a deblocking method that is applied during both encoding and decoding, to reduce blocking artifacts at encoding time ("in the loop") so that future P-frames and B-frames don't carry them forward.</span></span>

<span data-ttu-id="ee8ea-111">套用「迴圈」篩選的效果，是輸出影片畫面格中宏區塊的邊緣比較不明顯。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-111">The effect of applying the in-loop filter is that the edges of the macro-blocks in the output video frames are less noticeable.</span></span> <span data-ttu-id="ee8ea-112">在此同時，影像在外觀上可能會變柔和。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-112">At the same time the image can become softer in appearance.</span></span>

<span data-ttu-id="ee8ea-113">雖然「迴圈中」篩選可能會導致某些框架中的影像詳細資料減少，但整體的影片品質將會明顯受益。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-113">Although the in-loop filter can lead to reduced image detail in some frames, the overall video quality will benefit noticeably.</span></span> <span data-ttu-id="ee8ea-114">使用迴圈中篩選的最大缺點是額外的解碼效能成本。</span><span class="sxs-lookup"><span data-stu-id="ee8ea-114">The biggest disadvantage to using in-loop filtering is the additional decoding performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8ea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee8ea-115">Requirements</span></span>



| <span data-ttu-id="ee8ea-116">需求</span><span class="sxs-lookup"><span data-stu-id="ee8ea-116">Requirement</span></span> | <span data-ttu-id="ee8ea-117">值</span><span class="sxs-lookup"><span data-stu-id="ee8ea-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8ea-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee8ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8ea-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee8ea-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee8ea-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee8ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8ea-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee8ea-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee8ea-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ee8ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee8ea-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8ea-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8ea-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee8ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8ea-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ee8ea-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




