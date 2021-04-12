---
description: 指定描述輸入音訊內容的 WAVEFORMATEX 結構。
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: 'MFPKEY_WMAENC_ORIGWAVEFORMAT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192165"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="aa805-103">MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT 屬性</span><span class="sxs-lookup"><span data-stu-id="aa805-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="aa805-104">指定描述輸入音訊內容的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="aa805-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="aa805-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="aa805-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="aa805-106">g \_ wszWMACOriginalWaveFormat</span><span class="sxs-lookup"><span data-stu-id="aa805-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="aa805-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="aa805-107">Data Type</span></span>

<span data-ttu-id="aa805-108">VT \_ array \| vt \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 為位元組陣列) </span><span class="sxs-lookup"><span data-stu-id="aa805-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="aa805-109">備註</span><span class="sxs-lookup"><span data-stu-id="aa805-109">Remarks</span></span>

<span data-ttu-id="aa805-110">將以 Windows Media 音訊為基礎的內容轉換成較低的位元速率時，您可以將內容的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構傳遞給編解碼器，讓編解碼器能夠優化其演算法。</span><span class="sxs-lookup"><span data-stu-id="aa805-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="aa805-111">這項功能稱為 smart recompression，可提供比解壓縮內容更好的結果，然後透過編解碼器將重新產生的 PCM 範例饋送回來。</span><span class="sxs-lookup"><span data-stu-id="aa805-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="aa805-112">傳遞 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構時，請在 **WAVEFORMATEX cbSize** 所指定之結構的結尾包含任何額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="aa805-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="aa805-113">音訊編碼器只接受通道數目、每個樣本位數和樣本速率相同的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="aa805-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="aa805-114">您只能將內容轉碼至這些參數中的較低位元速率。</span><span class="sxs-lookup"><span data-stu-id="aa805-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="aa805-115">在任何情況下，您都必須將內容解碼，並將未壓縮的範例作為輸入傳遞至編碼器。</span><span class="sxs-lookup"><span data-stu-id="aa805-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="aa805-116">設定此屬性可為編碼器提供有關已在內容上執行之處理的一些資訊。</span><span class="sxs-lookup"><span data-stu-id="aa805-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa805-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa805-117">Requirements</span></span>



| <span data-ttu-id="aa805-118">需求</span><span class="sxs-lookup"><span data-stu-id="aa805-118">Requirement</span></span> | <span data-ttu-id="aa805-119">值</span><span class="sxs-lookup"><span data-stu-id="aa805-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa805-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa805-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa805-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa805-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aa805-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa805-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa805-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa805-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa805-124">標頭</span><span class="sxs-lookup"><span data-stu-id="aa805-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa805-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa805-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa805-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa805-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa805-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="aa805-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
