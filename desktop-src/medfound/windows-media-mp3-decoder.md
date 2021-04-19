---
description: Windows Media MP3 解碼會將編碼為下列格式的音訊檔案解碼。
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: 'Windows Media MP3 解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993233"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="88a3f-103">Windows Media MP3 解碼</span><span class="sxs-lookup"><span data-stu-id="88a3f-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="88a3f-104">Windows Media MP3 解碼會將編碼為下列格式的音訊檔案解碼。</span><span class="sxs-lookup"><span data-stu-id="88a3f-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="88a3f-105">ISO/IEC 11172-3 (MPEG 1 音訊) 第3層</span><span class="sxs-lookup"><span data-stu-id="88a3f-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="88a3f-106">ISO/IEC 13818-3 (MPEG-2 音訊) 第3層，低取樣頻率延伸</span><span class="sxs-lookup"><span data-stu-id="88a3f-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="88a3f-107">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="88a3f-107">Class Identifier</span></span>

<span data-ttu-id="88a3f-108">Windows Media MP3 解碼 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMP3DecMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="88a3f-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="88a3f-109">您可以藉由呼叫 **CoCreateInstance** 來建立 MP3 解碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="88a3f-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="88a3f-110">介面</span><span class="sxs-lookup"><span data-stu-id="88a3f-110">Interfaces</span></span>

<span data-ttu-id="88a3f-111">MP3 解碼器物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="88a3f-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="88a3f-112">Windows Media MP3 解碼器的運作方式，視您取得的介面和正在執行的 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="88a3f-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="88a3f-113">下表顯示 Windows Media MP3 解碼器以 SQL-DMO 或 MFT 行為的條件。</span><span class="sxs-lookup"><span data-stu-id="88a3f-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="88a3f-114">作業系統</span><span class="sxs-lookup"><span data-stu-id="88a3f-114">Operating system</span></span> | <span data-ttu-id="88a3f-115">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="88a3f-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a3f-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="88a3f-116">Windows XP</span></span>       | <span data-ttu-id="88a3f-117">Windows Media MP3 解碼一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="88a3f-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="88a3f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88a3f-118">Windows Vista</span></span>    | <span data-ttu-id="88a3f-119">Windows Media MP3 解碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="88a3f-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="88a3f-120">如果您在 Windows Media MP3 解碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="88a3f-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="88a3f-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88a3f-121">Windows 7</span></span>        | <span data-ttu-id="88a3f-122">Windows Media MP3 解碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="88a3f-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="88a3f-123">如果您在 Windows Media MP3 解碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="88a3f-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="88a3f-124">輸入格式</span><span class="sxs-lookup"><span data-stu-id="88a3f-124">Input Formats</span></span>

<span data-ttu-id="88a3f-125">下表顯示的音訊格式標記代表 Windows Media MP3 解碼所支援的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="88a3f-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="88a3f-126">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="88a3f-126">Format tag constant</span></span>      | <span data-ttu-id="88a3f-127">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="88a3f-127">Format tag value</span></span> | <span data-ttu-id="88a3f-128">音訊格式</span><span class="sxs-lookup"><span data-stu-id="88a3f-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="88a3f-129">WAVE \_ 格式 \_ MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="88a3f-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="88a3f-130">0x55</span><span class="sxs-lookup"><span data-stu-id="88a3f-130">0x55</span></span>             | <span data-ttu-id="88a3f-131">ISO MPEG 第3層</span><span class="sxs-lookup"><span data-stu-id="88a3f-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="88a3f-132">輸出格式</span><span class="sxs-lookup"><span data-stu-id="88a3f-132">Output Formats</span></span>

<span data-ttu-id="88a3f-133">下表顯示的音訊格式標記代表 Windows Media MP3 解碼所支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="88a3f-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="88a3f-134">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="88a3f-134">Format tag constant</span></span>       | <span data-ttu-id="88a3f-135">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="88a3f-135">Format tag value</span></span> | <span data-ttu-id="88a3f-136">音訊格式</span><span class="sxs-lookup"><span data-stu-id="88a3f-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="88a3f-137">WAVE \_ 格式 \_ PCM</span><span class="sxs-lookup"><span data-stu-id="88a3f-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="88a3f-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="88a3f-138">0x0001</span></span>           | <span data-ttu-id="88a3f-139">用來作為一或 (的 PCM 格式) </span><span class="sxs-lookup"><span data-stu-id="88a3f-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="88a3f-140">WAVE \_ 格式 \_ IEEE \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="88a3f-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="88a3f-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="88a3f-141">0x0003</span></span>           | <span data-ttu-id="88a3f-142">作為 MFT 使用的 IEEE 浮點數 () </span><span class="sxs-lookup"><span data-stu-id="88a3f-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="88a3f-143">WAVE \_ 格式 \_ 可擴充</span><span class="sxs-lookup"><span data-stu-id="88a3f-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="88a3f-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="88a3f-144">0xFFFE</span></span>           | <span data-ttu-id="88a3f-145">使用 **WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式做為 MFT 時 () </span><span class="sxs-lookup"><span data-stu-id="88a3f-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="88a3f-146">Windows Media MP3 解碼支援和列舉下列輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88a3f-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="88a3f-147">輸出類型，具有與輸入類型相同的取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="88a3f-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="88a3f-148">身歷聲輸入的 Mono 輸出。</span><span class="sxs-lookup"><span data-stu-id="88a3f-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="88a3f-149">位深度為8和16的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="88a3f-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="88a3f-150">浮點數輸出（如果解碼器的行為是 MFT）。</span><span class="sxs-lookup"><span data-stu-id="88a3f-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="88a3f-151">Windows Media MP3 解碼支援但不會列舉下列輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="88a3f-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="88a3f-152">輸出類型，具有輸入類型的一半取樣率。</span><span class="sxs-lookup"><span data-stu-id="88a3f-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="88a3f-153">輸出類型，具有輸入類型的第四個取樣率。</span><span class="sxs-lookup"><span data-stu-id="88a3f-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a3f-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="88a3f-154">Requirements</span></span>



| <span data-ttu-id="88a3f-155">需求</span><span class="sxs-lookup"><span data-stu-id="88a3f-155">Requirement</span></span> | <span data-ttu-id="88a3f-156">值</span><span class="sxs-lookup"><span data-stu-id="88a3f-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88a3f-157">用戶端</span><span class="sxs-lookup"><span data-stu-id="88a3f-157">Client</span></span><br/> | <span data-ttu-id="88a3f-158">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="88a3f-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="88a3f-159">標頭</span><span class="sxs-lookup"><span data-stu-id="88a3f-159">Header</span></span><br/> | <dl> <span data-ttu-id="88a3f-160"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="88a3f-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="88a3f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="88a3f-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="88a3f-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88a3f-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="88a3f-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88a3f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a3f-164">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="88a3f-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="88a3f-165">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="88a3f-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




