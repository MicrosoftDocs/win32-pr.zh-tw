---
description: 指定音訊解碼器是否應提供高解析度的輸出。
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: 'MFPKEY_WMADEC_HIRESOUTPUT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000100"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a><span data-ttu-id="74700-103">MFPKEY \_ WMADEC \_ HIRESOUTPUT 屬性</span><span class="sxs-lookup"><span data-stu-id="74700-103">MFPKEY\_WMADEC\_HIRESOUTPUT Property</span></span>

<span data-ttu-id="74700-104">指定音訊解碼器是否應提供高解析度的輸出。</span><span class="sxs-lookup"><span data-stu-id="74700-104">Specifies whether the audio decoder should deliver high-resolution output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="74700-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="74700-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="74700-106">g \_ wszWMACHiResOutput</span><span class="sxs-lookup"><span data-stu-id="74700-106">g\_wszWMACHiResOutput</span></span>

## <a name="data-type"></a><span data-ttu-id="74700-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="74700-107">Data Type</span></span>

<span data-ttu-id="74700-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="74700-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="74700-109">預設值</span><span class="sxs-lookup"><span data-stu-id="74700-109">Default Value</span></span>

<span data-ttu-id="74700-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="74700-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="74700-111">備註</span><span class="sxs-lookup"><span data-stu-id="74700-111">Remarks</span></span>

<span data-ttu-id="74700-112">將此屬性設定為 VARIANT \_ TRUE，以將多聲道或24位音訊內容或速率高於 48000 Hz 的音訊內容解碼。</span><span class="sxs-lookup"><span data-stu-id="74700-112">Set this property to VARIANT\_TRUE to decode multichannel or 24-bit audio content, or audio with a sample rate greater than 48,000 Hz.</span></span> <span data-ttu-id="74700-113">如果內容是以高解析度編碼，但這個屬性是 VARIANT \_ FALSE，則適用下列行為：</span><span class="sxs-lookup"><span data-stu-id="74700-113">If the content is encoded in high resolution, but this property is VARIANT\_FALSE, the following behaviors apply:</span></span>

-   <span data-ttu-id="74700-114">SQL-DMO 輸出將限制為16位、48-KHz 身歷聲。</span><span class="sxs-lookup"><span data-stu-id="74700-114">The DMO output will be limited to 16-bit, 48-KHz stereo.</span></span>
-   <span data-ttu-id="74700-115">MFT 會列舉限制為16個位的輸出模式，而不涉及頻道計數或取樣率的變更。</span><span class="sxs-lookup"><span data-stu-id="74700-115">The MFT will enumerate output modes that are limited to 16 bits and do not involve changes in channel count or sampling rate.</span></span>

<span data-ttu-id="74700-116">高解析度音訊的屬性會在 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構中傳遞，而不是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="74700-116">The properties of high-resolution audio are passed in a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure, not [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).</span></span>

<span data-ttu-id="74700-117">只有當解碼器是在 Windows XP 或更新版本上執行時，才能使用高解析度輸出。</span><span class="sxs-lookup"><span data-stu-id="74700-117">High-resolution output is available only if the decoder is running on Windows XP or later.</span></span> <span data-ttu-id="74700-118">無論您的應用程式執行所在的作業系統為何，都可以設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="74700-118">You can set this property regardless of the operating system on which your application is running.</span></span> <span data-ttu-id="74700-119">在 Windows XP 之前的 Windows 版本上，此解碼器會忽略此設定並傳遞標準輸出。</span><span class="sxs-lookup"><span data-stu-id="74700-119">On versions of Windows earlier than Windows XP, the decoder will ignore this setting and deliver standard output.</span></span>

<span data-ttu-id="74700-120">許多玩家 (包括 Windows Media Player 9 系列和更新版本，) 為所有內容設定這個值。</span><span class="sxs-lookup"><span data-stu-id="74700-120">Many players (including Windows Media Player 9 Series and later) set this value for all content.</span></span>

## <a name="requirements"></a><span data-ttu-id="74700-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="74700-121">Requirements</span></span>



| <span data-ttu-id="74700-122">需求</span><span class="sxs-lookup"><span data-stu-id="74700-122">Requirement</span></span> | <span data-ttu-id="74700-123">值</span><span class="sxs-lookup"><span data-stu-id="74700-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74700-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74700-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74700-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74700-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74700-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74700-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74700-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74700-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74700-128">標頭</span><span class="sxs-lookup"><span data-stu-id="74700-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="74700-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="74700-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74700-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74700-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74700-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="74700-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
