---
description: 指定要使用語音編解碼器將內容編碼為音樂的部分內容。
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: 'MFPKEY_WMAVOICE_ENC_EDL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692331"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a><span data-ttu-id="4e00e-103">MFPKEY \_ WMAVOICE \_ ENC \_ EDL 屬性</span><span class="sxs-lookup"><span data-stu-id="4e00e-103">MFPKEY\_WMAVOICE\_ENC\_EDL Property</span></span>

<span data-ttu-id="4e00e-104">指定要使用語音編解碼器將內容編碼為音樂的部分內容。</span><span class="sxs-lookup"><span data-stu-id="4e00e-104">Specifies the portions of content to be encoded as music by the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4e00e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="4e00e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4e00e-106">g \_ wszWMACVoiceBuffer</span><span class="sxs-lookup"><span data-stu-id="4e00e-106">g\_wszWMACVoiceBuffer</span></span>

## <a name="data-type"></a><span data-ttu-id="4e00e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4e00e-107">Data Type</span></span>

<span data-ttu-id="4e00e-108">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="4e00e-108">VT\_BSTR</span></span>

## <a name="default-value"></a><span data-ttu-id="4e00e-109">預設值</span><span class="sxs-lookup"><span data-stu-id="4e00e-109">Default Value</span></span>

<span data-ttu-id="4e00e-110">無預設值。</span><span class="sxs-lookup"><span data-stu-id="4e00e-110">No default value.</span></span> <span data-ttu-id="4e00e-111">如果未設定此屬性，編解碼器將會使用 [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) 屬性的值來判斷如何編碼內容。</span><span class="sxs-lookup"><span data-stu-id="4e00e-111">If this property is not set, the codec will use the value of the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to determine how to encode the content.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e00e-112">備註</span><span class="sxs-lookup"><span data-stu-id="4e00e-112">Remarks</span></span>

<span data-ttu-id="4e00e-113">如果編解碼器的自動模式未提供滿意的結果，您可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="4e00e-113">You can use this property if the automatic mode of the codec is not giving satisfactory results.</span></span>

<span data-ttu-id="4e00e-114">此值是以逗號分隔的字串，其中至少包含四個整數。</span><span class="sxs-lookup"><span data-stu-id="4e00e-114">This value is a comma-delimited string containing at least four integers.</span></span> <span data-ttu-id="4e00e-115">第一個整數是版本號碼;此值一律使用1。</span><span class="sxs-lookup"><span data-stu-id="4e00e-115">The first integer is the version number; always use 1 for this value.</span></span> <span data-ttu-id="4e00e-116">第二個整數是需要編碼為音樂的區段數目。</span><span class="sxs-lookup"><span data-stu-id="4e00e-116">The second integer is the number of sections that need to be encoded as music.</span></span> <span data-ttu-id="4e00e-117">在第二個整數之後，會有數個代表範圍的值（以毫秒為單位），每個內容區段的一對需要編碼為音樂。</span><span class="sxs-lookup"><span data-stu-id="4e00e-117">Following the second integer are a number of pairs of values representing ranges in milliseconds, one pair for each section of content that needs to be encoded as music.</span></span>

<span data-ttu-id="4e00e-118">例如，"1，2100200500600" 會通知編碼器使用第1版的音樂。</span><span class="sxs-lookup"><span data-stu-id="4e00e-118">For example, "1,2,100,200,500,600" informs the encoder to use version 1 with 2 sections of music.</span></span> <span data-ttu-id="4e00e-119">第一個 [音樂] 區段的開頭為100毫秒，結束于200毫秒。</span><span class="sxs-lookup"><span data-stu-id="4e00e-119">The first music section starts at 100 ms and ends at 200 ms.</span></span> <span data-ttu-id="4e00e-120">第二個音樂區段會從500毫秒開始，並于600毫秒結束。</span><span class="sxs-lookup"><span data-stu-id="4e00e-120">The second music section starts at 500 ms and ends at 600 ms.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e00e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e00e-121">Requirements</span></span>



| <span data-ttu-id="4e00e-122">需求</span><span class="sxs-lookup"><span data-stu-id="4e00e-122">Requirement</span></span> | <span data-ttu-id="4e00e-123">值</span><span class="sxs-lookup"><span data-stu-id="4e00e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e00e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e00e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4e00e-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e00e-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e00e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e00e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4e00e-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e00e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e00e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4e00e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e00e-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e00e-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e00e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e00e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e00e-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="4e00e-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




