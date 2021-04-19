---
description: 指定 (B 框架) 的雙向預測框架數目。
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: 'MFPKEY_NUMBFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980796"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="58d37-103">MFPKEY \_ NUMBFRAMES 屬性</span><span class="sxs-lookup"><span data-stu-id="58d37-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="58d37-104">指定 (B 框架) 的雙向預測框架數目。</span><span class="sxs-lookup"><span data-stu-id="58d37-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="58d37-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="58d37-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="58d37-106">g \_ wszWMVCNumBFrames</span><span class="sxs-lookup"><span data-stu-id="58d37-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="58d37-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="58d37-107">Data Type</span></span>

<span data-ttu-id="58d37-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="58d37-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="58d37-109">預設值</span><span class="sxs-lookup"><span data-stu-id="58d37-109">Default Value</span></span>

<span data-ttu-id="58d37-110">0</span><span class="sxs-lookup"><span data-stu-id="58d37-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="58d37-111">備註</span><span class="sxs-lookup"><span data-stu-id="58d37-111">Remarks</span></span>

<span data-ttu-id="58d37-112">根據預設，Windows Media 視訊9只會使用 intraframes (的畫面格) ，也稱為主要畫面格或錨定框架，其為完整編碼的畫面格，以及 (P 框架) 的預測性框架，其編碼為與上一個 I 框架的差異。</span><span class="sxs-lookup"><span data-stu-id="58d37-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="58d37-113">B 框架與 P 框架不同，因為它們會儲存與上一個框架之間的差異，以及與下列框架之間的差異。</span><span class="sxs-lookup"><span data-stu-id="58d37-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="58d37-114">當您將編解碼器設定為使用 B 型框架時，它會在 I 或 P 類型的每一對畫面格之間使用指定的 B 框架數目。</span><span class="sxs-lookup"><span data-stu-id="58d37-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="58d37-115">例如，如果沒有 B 框架的框架序列是 "IPPPPPPPPI"，則具有兩個 B 框架的相同序列編碼會是 "IBBPBBPBBI"。</span><span class="sxs-lookup"><span data-stu-id="58d37-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="58d37-116">針對大部分的內容，有一或兩個 B 框架是合適的。</span><span class="sxs-lookup"><span data-stu-id="58d37-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="58d37-117">以較高的資料速率而言，通常會有一個 B 框架是最佳選擇。</span><span class="sxs-lookup"><span data-stu-id="58d37-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="58d37-118">三個或更多很少用。</span><span class="sxs-lookup"><span data-stu-id="58d37-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="58d37-119">這個屬性值的有效範圍是0到7。</span><span class="sxs-lookup"><span data-stu-id="58d37-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d37-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="58d37-120">Requirements</span></span>



| <span data-ttu-id="58d37-121">需求</span><span class="sxs-lookup"><span data-stu-id="58d37-121">Requirement</span></span> | <span data-ttu-id="58d37-122">值</span><span class="sxs-lookup"><span data-stu-id="58d37-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58d37-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58d37-123">Minimum supported client</span></span><br/> | <span data-ttu-id="58d37-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58d37-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="58d37-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58d37-125">Minimum supported server</span></span><br/> | <span data-ttu-id="58d37-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58d37-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58d37-127">標頭</span><span class="sxs-lookup"><span data-stu-id="58d37-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="58d37-128"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="58d37-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d37-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58d37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d37-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="58d37-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




