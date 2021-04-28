---
description: MFPKEY_COMPLEXITY 屬性-指定編碼器演算法的複雜度。
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: 'MFPKEY_COMPLEXITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092936"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="1f06e-103">MFPKEY \_ 複雜性屬性</span><span class="sxs-lookup"><span data-stu-id="1f06e-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="1f06e-104">\[[**MFPKEY \_**](mfpkey-complexityexproperty.md)您可以在 [需求] 區段中指定的作業系統使用複雜性。</span><span class="sxs-lookup"><span data-stu-id="1f06e-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1f06e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1f06e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1f06e-106">相反地，請使用 **MFPKEY \_ COMPLEXITYEX**。\]</span><span class="sxs-lookup"><span data-stu-id="1f06e-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="1f06e-107">指定編碼器演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="1f06e-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1f06e-108">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1f06e-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="1f06e-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="1f06e-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="1f06e-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="1f06e-110">Data Type</span></span>

<span data-ttu-id="1f06e-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1f06e-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1f06e-112">預設值</span><span class="sxs-lookup"><span data-stu-id="1f06e-112">Default Value</span></span>

<span data-ttu-id="1f06e-113">預設值取決於影片編碼器的版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="1f06e-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="1f06e-114">編碼器版本</span><span class="sxs-lookup"><span data-stu-id="1f06e-114">Encoder version</span></span>                 | <span data-ttu-id="1f06e-115">預設值</span><span class="sxs-lookup"><span data-stu-id="1f06e-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="1f06e-116">Windows Media 視訊9編碼器</span><span class="sxs-lookup"><span data-stu-id="1f06e-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="1f06e-117">3</span><span class="sxs-lookup"><span data-stu-id="1f06e-117">3</span></span>             |
| <span data-ttu-id="1f06e-118">Windows Media 視訊7/8 編碼器</span><span class="sxs-lookup"><span data-stu-id="1f06e-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="1f06e-119">1</span><span class="sxs-lookup"><span data-stu-id="1f06e-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="1f06e-120">備註</span><span class="sxs-lookup"><span data-stu-id="1f06e-120">Remarks</span></span>

<span data-ttu-id="1f06e-121">這個整數值的範圍是從0到3。</span><span class="sxs-lookup"><span data-stu-id="1f06e-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="1f06e-122">較低的值會使編解碼器使用較不復雜的編碼演算法。</span><span class="sxs-lookup"><span data-stu-id="1f06e-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="1f06e-123">雖然更簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。</span><span class="sxs-lookup"><span data-stu-id="1f06e-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f06e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f06e-124">Requirements</span></span>



| <span data-ttu-id="1f06e-125">需求</span><span class="sxs-lookup"><span data-stu-id="1f06e-125">Requirement</span></span> | <span data-ttu-id="1f06e-126">值</span><span class="sxs-lookup"><span data-stu-id="1f06e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f06e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f06e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1f06e-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f06e-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f06e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f06e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1f06e-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f06e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f06e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1f06e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f06e-132"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f06e-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f06e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f06e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f06e-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1f06e-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




