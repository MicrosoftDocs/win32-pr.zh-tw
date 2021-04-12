---
description: 指定編碼內容的複雜性設定檔。
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: 'MFPKEY_DECODERCOMPLEXITYPROFILE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848819"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="2e887-103">MFPKEY \_ DECODERCOMPLEXITYPROFILE 屬性</span><span class="sxs-lookup"><span data-stu-id="2e887-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="2e887-104">指定編碼內容的複雜性設定檔。</span><span class="sxs-lookup"><span data-stu-id="2e887-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2e887-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="2e887-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2e887-106">g \_ wszWMVCDecoderComplexityProfile</span><span class="sxs-lookup"><span data-stu-id="2e887-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="2e887-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2e887-107">Data Type</span></span>

<span data-ttu-id="2e887-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2e887-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="2e887-109">備註</span><span class="sxs-lookup"><span data-stu-id="2e887-109">Remarks</span></span>

<span data-ttu-id="2e887-110">只有在編碼完成後，您才可以讀取此值。</span><span class="sxs-lookup"><span data-stu-id="2e887-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="2e887-111">若為音訊，這個屬性會有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2e887-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="2e887-112">值</span><span class="sxs-lookup"><span data-stu-id="2e887-112">Value</span></span> | <span data-ttu-id="2e887-113">描述</span><span class="sxs-lookup"><span data-stu-id="2e887-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e887-114">L1</span><span class="sxs-lookup"><span data-stu-id="2e887-114">"L1"</span></span>  | <span data-ttu-id="2e887-115">取樣率為 44.1 KHz 且最大位元速率為 161 Kbps 的標準編碼。</span><span class="sxs-lookup"><span data-stu-id="2e887-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="2e887-116">L2</span><span class="sxs-lookup"><span data-stu-id="2e887-116">"L2"</span></span>  | <span data-ttu-id="2e887-117">使用取樣率的標準編碼，最高可達 48 KHz，最大位元速率為 161 Kbps。</span><span class="sxs-lookup"><span data-stu-id="2e887-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="2e887-118">L3</span><span class="sxs-lookup"><span data-stu-id="2e887-118">"L3"</span></span>  | <span data-ttu-id="2e887-119">使用取樣率的標準編碼，最高可達 48 KHz，最大位元速率為 385 Kbps。</span><span class="sxs-lookup"><span data-stu-id="2e887-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="2e887-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="2e887-120">"M0a"</span></span> | <span data-ttu-id="2e887-121">使用取樣率的專業編碼，最高可達48到 192 Kbps 之間的 48 KHz 和位元速率。</span><span class="sxs-lookup"><span data-stu-id="2e887-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="2e887-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="2e887-122">"M0b"</span></span> | <span data-ttu-id="2e887-123">具有最高 48 KHz 和最大位元速率為 192 Kbps 之取樣率的專業編碼。</span><span class="sxs-lookup"><span data-stu-id="2e887-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="2e887-124">M1</span><span class="sxs-lookup"><span data-stu-id="2e887-124">"M1"</span></span>  | <span data-ttu-id="2e887-125">具有最高 48 KHz 和最大位元速率為 384 Kbps 之取樣率的專業編碼。</span><span class="sxs-lookup"><span data-stu-id="2e887-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="2e887-126">M2</span><span class="sxs-lookup"><span data-stu-id="2e887-126">"M2"</span></span>  | <span data-ttu-id="2e887-127">具有最高 96 KHz 和最大位元速率為 768 Kbps 之取樣率的專業編碼。</span><span class="sxs-lookup"><span data-stu-id="2e887-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="2e887-128">M3</span><span class="sxs-lookup"><span data-stu-id="2e887-128">"M3"</span></span>  | <span data-ttu-id="2e887-129">具有最高 96 KHz 和最大位元速率為 1.5 Mbps 之取樣率的專業編碼。</span><span class="sxs-lookup"><span data-stu-id="2e887-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="2e887-130">N1</span><span class="sxs-lookup"><span data-stu-id="2e887-130">"N1"</span></span>  | <span data-ttu-id="2e887-131">使用取樣率的無失真編碼，最高可達 48 KHz，最多2個通道。</span><span class="sxs-lookup"><span data-stu-id="2e887-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="2e887-132">N2</span><span class="sxs-lookup"><span data-stu-id="2e887-132">"N2"</span></span>  | <span data-ttu-id="2e887-133">使用取樣率高達 96 KHz 的無失真編碼，以及最多6個通道 (5.1 環繞) 。</span><span class="sxs-lookup"><span data-stu-id="2e887-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="2e887-134">N3</span><span class="sxs-lookup"><span data-stu-id="2e887-134">"N3"</span></span>  | <span data-ttu-id="2e887-135">使用取樣率高達 96 KHz 的無失真編碼，以及最多8個通道 (7.1 環繞) 。</span><span class="sxs-lookup"><span data-stu-id="2e887-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="2e887-136">針對影片，此屬性具有下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2e887-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="2e887-137">值</span><span class="sxs-lookup"><span data-stu-id="2e887-137">Value</span></span> | <span data-ttu-id="2e887-138">描述</span><span class="sxs-lookup"><span data-stu-id="2e887-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2e887-139">AP</span><span class="sxs-lookup"><span data-stu-id="2e887-139">"AP"</span></span>  | <span data-ttu-id="2e887-140">advanced profile (僅適用于 Windows Media 視訊 9 Advanced Profile 編解碼器) </span><span class="sxs-lookup"><span data-stu-id="2e887-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="2e887-141">CP</span><span class="sxs-lookup"><span data-stu-id="2e887-141">"CP"</span></span>  | <span data-ttu-id="2e887-142">不再支援</span><span class="sxs-lookup"><span data-stu-id="2e887-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="2e887-143">多功能</span><span class="sxs-lookup"><span data-stu-id="2e887-143">"MP"</span></span>  | <span data-ttu-id="2e887-144">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="2e887-144">main profile</span></span>                                                                      |
| <span data-ttu-id="2e887-145">SP-1</span><span class="sxs-lookup"><span data-stu-id="2e887-145">"SP"</span></span>  | <span data-ttu-id="2e887-146">簡單設定檔</span><span class="sxs-lookup"><span data-stu-id="2e887-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="2e887-147">針對影片內容，您可以在開始編碼之前，先設定 [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) 來要求設定檔層級。</span><span class="sxs-lookup"><span data-stu-id="2e887-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="2e887-148">編解碼器會嘗試在要求的複雜性層級的參數內進行編碼，但您設定的其他設定將會優先使用。</span><span class="sxs-lookup"><span data-stu-id="2e887-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="2e887-149">在編碼之後，您應該一律檢查實際的複雜性設定檔值，以免無法接受您的要求。</span><span class="sxs-lookup"><span data-stu-id="2e887-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e887-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e887-150">Requirements</span></span>



| <span data-ttu-id="2e887-151">需求</span><span class="sxs-lookup"><span data-stu-id="2e887-151">Requirement</span></span> | <span data-ttu-id="2e887-152">值</span><span class="sxs-lookup"><span data-stu-id="2e887-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e887-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e887-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2e887-154">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e887-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e887-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e887-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2e887-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e887-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e887-157">標頭</span><span class="sxs-lookup"><span data-stu-id="2e887-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e887-158"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e887-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e887-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e887-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e887-160">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="2e887-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




