---
description: MFPKEY_COMPLEXITYEX 屬性-指定編碼器演算法的複雜度。
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: 'MFPKEY_COMPLEXITYEX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087606"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="664a3-103">MFPKEY \_ COMPLEXITYEX 屬性</span><span class="sxs-lookup"><span data-stu-id="664a3-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="664a3-104">指定編碼器演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="664a3-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="664a3-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="664a3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="664a3-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="664a3-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="664a3-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="664a3-107">Data Type</span></span>

<span data-ttu-id="664a3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="664a3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="664a3-109">預設值</span><span class="sxs-lookup"><span data-stu-id="664a3-109">Default Value</span></span>

<span data-ttu-id="664a3-110">預設值取決於影片編碼器的版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="664a3-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="664a3-111">編碼器版本</span><span class="sxs-lookup"><span data-stu-id="664a3-111">Encoder version</span></span>                 | <span data-ttu-id="664a3-112">預設值</span><span class="sxs-lookup"><span data-stu-id="664a3-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="664a3-113">Windows Media 視訊9編碼器</span><span class="sxs-lookup"><span data-stu-id="664a3-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="664a3-114">3</span><span class="sxs-lookup"><span data-stu-id="664a3-114">3</span></span>             |
| <span data-ttu-id="664a3-115">Windows Media 視訊7/8 編碼器</span><span class="sxs-lookup"><span data-stu-id="664a3-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="664a3-116">1</span><span class="sxs-lookup"><span data-stu-id="664a3-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="664a3-117">可能的值</span><span class="sxs-lookup"><span data-stu-id="664a3-117">Possible Values</span></span>

<span data-ttu-id="664a3-118">可能的值取決於影片編碼器的版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="664a3-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="664a3-119">編碼器版本</span><span class="sxs-lookup"><span data-stu-id="664a3-119">Encoder version</span></span>                 | <span data-ttu-id="664a3-120">可能值</span><span class="sxs-lookup"><span data-stu-id="664a3-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="664a3-121">Windows Media 視訊9編碼器</span><span class="sxs-lookup"><span data-stu-id="664a3-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="664a3-122">0、1、2、3、4、5</span><span class="sxs-lookup"><span data-stu-id="664a3-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="664a3-123">Windows Media 視訊7/8 編碼器</span><span class="sxs-lookup"><span data-stu-id="664a3-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="664a3-124">0、1</span><span class="sxs-lookup"><span data-stu-id="664a3-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="664a3-125">備註</span><span class="sxs-lookup"><span data-stu-id="664a3-125">Remarks</span></span>

<span data-ttu-id="664a3-126">較低的值會使編解碼器使用較不復雜的編碼演算法。</span><span class="sxs-lookup"><span data-stu-id="664a3-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="664a3-127">雖然更簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。</span><span class="sxs-lookup"><span data-stu-id="664a3-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="664a3-128">從即時來源編碼內容時，這可能很重要，因為編碼器必須快速處理輸入，才能跟上來源的高度。</span><span class="sxs-lookup"><span data-stu-id="664a3-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="664a3-129">如果 [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) 屬性設定為1，則會忽略任何指派給這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="664a3-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="664a3-130">在此情況下，MFPKEY \_ COMPLEXITYEX 會自動設為3。</span><span class="sxs-lookup"><span data-stu-id="664a3-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="664a3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="664a3-131">Requirements</span></span>



| <span data-ttu-id="664a3-132">需求</span><span class="sxs-lookup"><span data-stu-id="664a3-132">Requirement</span></span> | <span data-ttu-id="664a3-133">值</span><span class="sxs-lookup"><span data-stu-id="664a3-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="664a3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="664a3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="664a3-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664a3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="664a3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="664a3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="664a3-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="664a3-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="664a3-138">標頭</span><span class="sxs-lookup"><span data-stu-id="664a3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="664a3-139"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="664a3-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="664a3-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="664a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664a3-141">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="664a3-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




