---
description: 隨著需要壓縮音訊格式的媒體存放裝置增加，應用程式必須識別、描述和使用各種新編碼的音訊內容，以將內容從電腦傳輸至裝置，例如 HDMI 或 DisplayPort 接收者。
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: 表示 IEC 61937 傳輸的格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a607770a388a11978d0e4666b5046506b6698c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549293"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a><span data-ttu-id="a9953-103">表示 IEC 61937 傳輸的格式</span><span class="sxs-lookup"><span data-stu-id="a9953-103">Representing Formats for IEC 61937 Transmissions</span></span>

<span data-ttu-id="a9953-104">隨著需要壓縮音訊格式的媒體存放裝置增加，應用程式必須識別、描述和使用各種新編碼的音訊內容，以將內容從電腦傳輸至裝置，例如 HDMI 或 DisplayPort 接收者。</span><span class="sxs-lookup"><span data-stu-id="a9953-104">With the increase in media storage devices that require compressed audio formats, applications must identify, describe, and use a variety of new encoded audio content for transmitting content from PCs to devices such as HDMI or DisplayPort receiver.</span></span>

<span data-ttu-id="a9953-105">若要代表要透過 IEC 61937 相容介面傳輸的編碼音訊串流，應用程式必須提供：</span><span class="sxs-lookup"><span data-stu-id="a9953-105">To represent an encoded audio stream to be transmitted over an IEC 61937-compatible interface, an application must provide:</span></span>

-   <span data-ttu-id="a9953-106">要傳輸的編碼音訊資料流程特性。</span><span class="sxs-lookup"><span data-stu-id="a9953-106">The characteristics of an encoded audio stream to be transmitted.</span></span>

-   <span data-ttu-id="a9953-107">目標裝置上已解碼音訊串流的特性。</span><span class="sxs-lookup"><span data-stu-id="a9953-107">The characteristics of a decoded audio stream on the target device.</span></span>

<span data-ttu-id="a9953-108">在 Windows Vista 和舊版 Windows 作業系統中，應用程式可以從頻道數目、取樣大小，以及使用此格式之音訊串流的資料速率，推斷音訊格式的品質等級。</span><span class="sxs-lookup"><span data-stu-id="a9953-108">In Windows Vista and earlier Windows operating systems, an application can infer the quality level of an audio format from the number of channels, the sample size, and the data rate of an audio stream that uses the format.</span></span> <span data-ttu-id="a9953-109">針對 PCM 格式，可從指定格式的 **WAVEFORMATEX** 結構的 **nChannels**、 **nSamplesPerSec** 和 **nAvgBytesPerSec** 成員取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="a9953-109">For a PCM format, this information is available from the **nChannels**, **nSamplesPerSec**, and **nAvgBytesPerSec** members of the **WAVEFORMATEX** structure that specifies the format.</span></span> <span data-ttu-id="a9953-110">針對非 PCM 格式，已 commandeered 這三個成員，以將壓縮資料的相關資訊儲存在音訊資料流程中。</span><span class="sxs-lookup"><span data-stu-id="a9953-110">For a non-PCM format, these three members have been commandeered to store information about the compressed data in the audio stream.</span></span> <span data-ttu-id="a9953-111">因此， **WAVEFORMATEX** 結構在解壓縮並播放串流之後，缺乏非 PCM 音訊串流的有效通道、取樣大小和資料速率的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9953-111">Thus, the **WAVEFORMATEX** structure lacks information about the effective number of channels, sample size, and data rate of the non-PCM audio stream after the stream is decompressed and played.</span></span> <span data-ttu-id="a9953-112">根據此結構中的資訊，使用者或應用程式可能難以推斷非 PCM 串流的品質等級。</span><span class="sxs-lookup"><span data-stu-id="a9953-112">Based on the information in this structure, a user or an application might have difficulty inferring the quality level of the non-PCM stream.</span></span>

<span data-ttu-id="a9953-113">**WAVEFORMATEX** 已延伸至 **WAVEFORMATEXTENSIBLE** 結構，以提供額外的資料流程特性。</span><span class="sxs-lookup"><span data-stu-id="a9953-113">The **WAVEFORMATEX** was extended to the **WAVEFORMATEXTENSIBLE** structure to provide the extra stream characteristics.</span></span> <span data-ttu-id="a9953-114">不過，此結構也不適合用來描述 IEC 61937 傳輸的資料流程，因為它的目的是要代表一組特性，並且用於未壓縮的多重通道 PCM 資料。</span><span class="sxs-lookup"><span data-stu-id="a9953-114">However, this structure is also not adequate in describing the stream for IEC 61937 transmissions because it was intended to represent a single set of characteristics and used for uncompressed, multi-channel PCM data.</span></span>

<span data-ttu-id="a9953-115">在 Windows 7 中，作業系統會提供新結構 **WAVEFORMATEXTENSIBLE \_ IEC61937** 的支援，以擴充 **WAVEFORMATEXTENSIBLE** 結構來儲存兩組音訊資料流程特性，藉此解決這個問題：編碼的音訊格式在音訊串流解碼後的傳輸和特性。</span><span class="sxs-lookup"><span data-stu-id="a9953-115">In Windows 7, the operating system addresses this problem by providing support for a new structure, **WAVEFORMATEXTENSIBLE\_IEC61937** which extends **WAVEFORMATEXTENSIBLE** structure to store two sets of audio stream characteristics: the encoded audio format before transmission and characteristics of the audio stream after it has been decoded.</span></span> <span data-ttu-id="a9953-116">新的結構會明確指定非 PCM 格式的通道、樣本大小和資料速率的有效數目。</span><span class="sxs-lookup"><span data-stu-id="a9953-116">The new structure explicitly specifies the effective number of channels, sample size, and data rate of a non-PCM format.</span></span> <span data-ttu-id="a9953-117">利用這項資訊，應用程式可以在解壓縮並播放非 PCM 串流之後，推斷其品質層級。</span><span class="sxs-lookup"><span data-stu-id="a9953-117">With this information, an application can infer the quality level of the non-PCM stream after it is decompressed and played.</span></span>

<span data-ttu-id="a9953-118">**WAVEFORMATEXTENSIBLE \_ IEC61937** 結構是在 Windows 7 SDK 隨附的 KsMedia. h 標頭中宣告的。</span><span class="sxs-lookup"><span data-stu-id="a9953-118">The **WAVEFORMATEXTENSIBLE\_IEC61937** structure is declared in the KsMedia.h header included with the Windows 7 SDK.</span></span> <span data-ttu-id="a9953-119">**FormatExt** 成員是 **WAVEFORMATEXTENSIBLE** 結構，可儲存要傳送之資料流程的特性。</span><span class="sxs-lookup"><span data-stu-id="a9953-119">The **FormatExt** member is the **WAVEFORMATEXTENSIBLE** structure that stores the characteristics of the stream to be transmitted.</span></span> <span data-ttu-id="a9953-120">**WAVEFORMATEXTENSIBLE** 結構的 **格式** 成員是 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="a9953-120">The **Format** member of the **WAVEFORMATEXTENSIBLE** structure is the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="a9953-121">這個 **WAVEFORMATEX** 和 **WAVEFORMATEXTENSIBLE** 的內容會向應用程式指出結構是否可解釋為 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構。</span><span class="sxs-lookup"><span data-stu-id="a9953-121">The contents of this **WAVEFORMATEX** and **WAVEFORMATEXTENSIBLE** indicate to an application whether the structure can be interpreted as a **WAVEFORMATEXTENSIBLE\_IEC61937** structure.</span></span> <span data-ttu-id="a9953-122">針對 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構：</span><span class="sxs-lookup"><span data-stu-id="a9953-122">For a **WAVEFORMATEXTENSIBLE\_IEC61937** structure:</span></span>

-   <span data-ttu-id="a9953-123">**WAVEFORMATEX** 的 **wFormatTag** 成員必須包含可延伸 \_ () 的 WAVE 格式 \_ `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` 。</span><span class="sxs-lookup"><span data-stu-id="a9953-123">The **wFormatTag** member of **WAVEFORMATEX** must contain WAVE\_FORMAT\_EXTENSIBLE (`FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE`).</span></span>

-   <span data-ttu-id="a9953-124">**WAVEFORMATEXTENSIBLE** 結構的 **SubFormat** 成員會指定要傳送之編碼格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a9953-124">The **SubFormat** member of the **WAVEFORMATEXTENSIBLE** structure specifies the GUID of the encoded format to be transmitted.</span></span> <span data-ttu-id="a9953-125">例如， `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` 表示杜比數位加上的格式。</span><span class="sxs-lookup"><span data-stu-id="a9953-125">For example, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indicates the Dolby Digital Plus format.</span></span> <span data-ttu-id="a9953-126">如需支援的 Guid，請參閱 SubFormat Guid。</span><span class="sxs-lookup"><span data-stu-id="a9953-126">For the supported GUIDs, see SubFormat GUIDs.</span></span>

-   <span data-ttu-id="a9953-127">WAVEFORMATEX 的 **cbSize** 成員所指定的大小為34個位元組。</span><span class="sxs-lookup"><span data-stu-id="a9953-127">The size indicated by **cbSize** member of the WAVEFORMATEX is 34 bytes.</span></span> <span data-ttu-id="a9953-128">(`FormatExt.Format.cbSize = 34`).</span><span class="sxs-lookup"><span data-stu-id="a9953-128">(`FormatExt.Format.cbSize = 34`).</span></span> <span data-ttu-id="a9953-129">**WAVEFORMATEXTENSIBLE \_ IEC61937** 的總大小為52個位元組。</span><span class="sxs-lookup"><span data-stu-id="a9953-129">The total size of **WAVEFORMATEXTENSIBLE\_IEC61937** is 52 bytes.</span></span>

<span data-ttu-id="a9953-130">**WAVEFORMATEXTENSIBLE \_ IEC61937** 的 **DwEncodedSamplesPerSec**、 **dwEncodedChannelCount** 和 **dwAverageBytesPerSec** 成員會描述取樣率、通道數目，以及音訊串流在解碼後的位元組位元速率（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a9953-130">The **dwEncodedSamplesPerSec**, **dwEncodedChannelCount**, and **dwAverageBytesPerSec** members of **WAVEFORMATEXTENSIBLE\_IEC61937** describe the sampling rate, number of channels, and bit rate in bytes of the stream of the audio stream after it has been decoded.</span></span>

## <a name="subformat-guids"></a><span data-ttu-id="a9953-131">SubFormat Guid</span><span class="sxs-lookup"><span data-stu-id="a9953-131">SubFormat GUIDs</span></span>

<span data-ttu-id="a9953-132">在 Windows 7 中，KsMedia 標頭包含 CEA-861-D 所定義之壓縮音訊格式的 SubFormat Guid 定義。</span><span class="sxs-lookup"><span data-stu-id="a9953-132">In Windows 7, the KsMedia.h header contains definitions for the SubFormat GUIDs for the compressed audio formats defined by CEA-861-D.</span></span> <span data-ttu-id="a9953-133">Guid 是在 **WAVEFORMATEXTENSIBLE** 的 SubFormat 成員中指定，在 **WAVEFORMATEXTENSIBLE \_ IEC61937** 結構的 **FormatExt** 成員中指定 (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`) 。</span><span class="sxs-lookup"><span data-stu-id="a9953-133">The GUIDs are specified in the SubFormat member of the **WAVEFORMATEXTENSIBLE**, specified in the **FormatExt** member of the **WAVEFORMATEXTENSIBLE\_IEC61937** structure (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`).</span></span>

<span data-ttu-id="a9953-134">下表列出以標準 IEC 61937 編碼音訊格式提供之壓縮音訊格式的 Guid。</span><span class="sxs-lookup"><span data-stu-id="a9953-134">The GUIDs for the compressed audio formats that are available as standard IEC 61937 encoded audio formats are listed in the following table.</span></span> <span data-ttu-id="a9953-135">這些格式類似于現有的現用程式碼 3 (AC-3) 和數位劇院音效 (DTS) 格式的標記法在 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="a9953-135">These formats are similar to the existing Active Coding 3 (AC-3) and Digital Theater Sound (DTS) formats representations in Windows.</span></span>



| <span data-ttu-id="a9953-136">CEA 861 類型</span><span class="sxs-lookup"><span data-stu-id="a9953-136">CEA 861 Type</span></span> | <span data-ttu-id="a9953-137">SubFormat GUID</span><span class="sxs-lookup"><span data-stu-id="a9953-137">SubFormat GUID</span></span>                                                                                                          | <span data-ttu-id="a9953-138">Description</span><span class="sxs-lookup"><span data-stu-id="a9953-138">Description</span></span>                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="a9953-139">0x00</span><span class="sxs-lookup"><span data-stu-id="a9953-139">0x00</span></span>         |                                                                                                                         | <span data-ttu-id="a9953-140">請參閱資料流程。</span><span class="sxs-lookup"><span data-stu-id="a9953-140">Refer to the stream.</span></span>                         |
| <span data-ttu-id="a9953-141">0x01</span><span class="sxs-lookup"><span data-stu-id="a9953-141">0x01</span></span>         | <span data-ttu-id="a9953-142">00000000-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-142">00000000-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-143">KSDATAFORMAT \_ 子類型 \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="a9953-143">KSDATAFORMAT\_SUBTYPE\_WAVEFORMATEX</span></span><br/>                          | <span data-ttu-id="a9953-144">IEC 60958 PCM</span><span class="sxs-lookup"><span data-stu-id="a9953-144">IEC 60958 PCM</span></span>                                |
| <span data-ttu-id="a9953-145">0x02</span><span class="sxs-lookup"><span data-stu-id="a9953-145">0x02</span></span>         | <span data-ttu-id="a9953-146">00000092-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-146">00000092-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-147">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位</span><span class="sxs-lookup"><span data-stu-id="a9953-147">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL</span></span><br/>              | <span data-ttu-id="a9953-148">AC-3</span><span class="sxs-lookup"><span data-stu-id="a9953-148">AC-3</span></span>                                         |
| <span data-ttu-id="a9953-149">0x03</span><span class="sxs-lookup"><span data-stu-id="a9953-149">0x03</span></span>         | <span data-ttu-id="a9953-150">00000003-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-150">00000003-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-151">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG1</span><span class="sxs-lookup"><span data-stu-id="a9953-151">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG1</span></span><br/>                       | <span data-ttu-id="a9953-152">MPEG-2 (第1層 & 2) </span><span class="sxs-lookup"><span data-stu-id="a9953-152">MPEG-1 (Layer 1 & 2)</span></span>                         |
| <span data-ttu-id="a9953-153">0x04</span><span class="sxs-lookup"><span data-stu-id="a9953-153">0x04</span></span>         | <span data-ttu-id="a9953-154">00000004-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-154">00000004-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-155">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG3</span><span class="sxs-lookup"><span data-stu-id="a9953-155">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG3</span></span><br/>                       | <span data-ttu-id="a9953-156">MPEG-2 (第3層) </span><span class="sxs-lookup"><span data-stu-id="a9953-156">MPEG-3 (Layer 3)</span></span>                             |
| <span data-ttu-id="a9953-157">0x05</span><span class="sxs-lookup"><span data-stu-id="a9953-157">0x05</span></span>         | <span data-ttu-id="a9953-158">00000005-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-158">00000005-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-159">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="a9953-159">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG2</span></span> <br/>                      | <span data-ttu-id="a9953-160">MPEG-2 (多重通道) </span><span class="sxs-lookup"><span data-stu-id="a9953-160">MPEG-2(multichannel)</span></span>                         |
| <span data-ttu-id="a9953-161">0x06</span><span class="sxs-lookup"><span data-stu-id="a9953-161">0x06</span></span>         | <span data-ttu-id="a9953-162">00000006-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-162">00000006-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-163">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ AAC</span><span class="sxs-lookup"><span data-stu-id="a9953-163">KSDATAFORMAT\_SUBTYPE\_IEC61937\_AAC</span></span><br/>                         | <span data-ttu-id="a9953-164">Advanced Audio 編碼 (ADTS) 中的 MPEG-2/4 AAC</span><span class="sxs-lookup"><span data-stu-id="a9953-164">Advanced Audio Coding (MPEG-2/4 AAC in ADTS)</span></span> |
| <span data-ttu-id="a9953-165">0x07</span><span class="sxs-lookup"><span data-stu-id="a9953-165">0x07</span></span>         | <span data-ttu-id="a9953-166">00000008-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-166">00000008-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-167">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS</span><span class="sxs-lookup"><span data-stu-id="a9953-167">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS</span></span><br/>                         | <span data-ttu-id="a9953-168">DTS</span><span class="sxs-lookup"><span data-stu-id="a9953-168">DTS</span></span>                                          |
| <span data-ttu-id="a9953-169">0x0a</span><span class="sxs-lookup"><span data-stu-id="a9953-169">0x0a</span></span>         | <span data-ttu-id="a9953-170">0000000a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-170">0000000a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-171">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號</span><span class="sxs-lookup"><span data-stu-id="a9953-171">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS</span></span><br/>        | <span data-ttu-id="a9953-172">杜比數位加號</span><span class="sxs-lookup"><span data-stu-id="a9953-172">Dolby Digital Plus</span></span>                           |
| <span data-ttu-id="a9953-173">0x0a</span><span class="sxs-lookup"><span data-stu-id="a9953-173">0x0a</span></span>         | <span data-ttu-id="a9953-174">0000010a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-174">0000010a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-175">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ PLUS \_ ATMOS</span><span class="sxs-lookup"><span data-stu-id="a9953-175">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS\_ATMOS</span></span><br/> | <span data-ttu-id="a9953-176">以杜比數位加號編碼的杜比 Atmos</span><span class="sxs-lookup"><span data-stu-id="a9953-176">Dolby Atmos encoded with Dolby Digital Plus</span></span>  |
| <span data-ttu-id="a9953-177">0x0b</span><span class="sxs-lookup"><span data-stu-id="a9953-177">0x0b</span></span>         | <span data-ttu-id="a9953-178">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-178">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-179">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="a9953-179">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/> | <span data-ttu-id="a9953-180">DTS HD</span><span class="sxs-lookup"><span data-stu-id="a9953-180">DTS HD</span></span>  |
| <span data-ttu-id="a9953-181">0x0b</span><span class="sxs-lookup"><span data-stu-id="a9953-181">0x0b</span></span>         | <span data-ttu-id="a9953-182">0000010b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-182">0000010b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-183">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ .dtsx \_ E1</span><span class="sxs-lookup"><span data-stu-id="a9953-183">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTSX\_E1</span></span><br/> | <span data-ttu-id="a9953-184">DTS： X E1</span><span class="sxs-lookup"><span data-stu-id="a9953-184">DTS:X E1</span></span>  |
| <span data-ttu-id="a9953-185">0x0b</span><span class="sxs-lookup"><span data-stu-id="a9953-185">0x0b</span></span>         | <span data-ttu-id="a9953-186">0000030b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-186">0000030b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-187">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ .dtsx \_ E2</span><span class="sxs-lookup"><span data-stu-id="a9953-187">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTSX\_E2</span></span><br/> | <span data-ttu-id="a9953-188">DTS： X E2</span><span class="sxs-lookup"><span data-stu-id="a9953-188">DTS:X E2</span></span>  |
| <span data-ttu-id="a9953-189">0x0f</span><span class="sxs-lookup"><span data-stu-id="a9953-189">0x0f</span></span>         |                                                                                                                         | <span data-ttu-id="a9953-190">未使用的保留</span><span class="sxs-lookup"><span data-stu-id="a9953-190">Unused Reserved</span></span>                              |



 

<span data-ttu-id="a9953-191">下表列出以高位速率音訊範例封包傳輸的壓縮音訊格式 Guid。</span><span class="sxs-lookup"><span data-stu-id="a9953-191">The GUIDs for the compressed audio formats that are transmitted in high bit-rate audio sample packets are listed in the following table.</span></span>



| <span data-ttu-id="a9953-192">CEA 861 類型</span><span class="sxs-lookup"><span data-stu-id="a9953-192">CEA 861 Type</span></span> | <span data-ttu-id="a9953-193">SubFormat GUID</span><span class="sxs-lookup"><span data-stu-id="a9953-193">SubFormat GUID</span></span>                                                                                           | <span data-ttu-id="a9953-194">Description</span><span class="sxs-lookup"><span data-stu-id="a9953-194">Description</span></span>                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9953-195">0x0b</span><span class="sxs-lookup"><span data-stu-id="a9953-195">0x0b</span></span>         | <span data-ttu-id="a9953-196">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-196">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-197">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="a9953-197">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/>      | <span data-ttu-id="a9953-198">DTS-HD (24 位、96Khz) </span><span class="sxs-lookup"><span data-stu-id="a9953-198">DTS-HD (24-bit, 96Khz)</span></span>                                                                                                          |
| <span data-ttu-id="a9953-199">0x0c</span><span class="sxs-lookup"><span data-stu-id="a9953-199">0x0c</span></span>         | <span data-ttu-id="a9953-200">0000000c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-200">0000000c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-201">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MLP</span><span class="sxs-lookup"><span data-stu-id="a9953-201">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MLP</span></span><br/>   | <span data-ttu-id="a9953-202">杜比1.0：</span><span class="sxs-lookup"><span data-stu-id="a9953-202">Dolby MAT 1.0:</span></span><br/> <span data-ttu-id="a9953-203">杜比 TrueHD (MLP –經線無失真封裝) –24位 192KHz/高達 18 Mbps、8個通道) </span><span class="sxs-lookup"><span data-stu-id="a9953-203">Dolby TrueHD (MLP – Meridian Lossless Packing) – 24-bit 192KHz/up to 18 Mbps, 8 channels)</span></span> <br/> |
| <span data-ttu-id="a9953-204">0x0c</span><span class="sxs-lookup"><span data-stu-id="a9953-204">0x0c</span></span>         | <span data-ttu-id="a9953-205">0000010c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-205">0000010c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-206">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MAT20</span><span class="sxs-lookup"><span data-stu-id="a9953-206">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT20</span></span><br/> | <span data-ttu-id="a9953-207">杜比2.0：</span><span class="sxs-lookup"><span data-stu-id="a9953-207">Dolby MAT 2.0:</span></span> <br/> <span data-ttu-id="a9953-208">杜比 TrueHD –24位 192KHz/最高可達 18 Mbps、8個通道或 LPCM，最高可達 24 Mbps。</span><span class="sxs-lookup"><span data-stu-id="a9953-208">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="a9953-209">0x0c</span><span class="sxs-lookup"><span data-stu-id="a9953-209">0x0c</span></span>         | <span data-ttu-id="a9953-210">0000030c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-210">0000030c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-211">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ MAT21</span><span class="sxs-lookup"><span data-stu-id="a9953-211">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT21</span></span><br/> | <span data-ttu-id="a9953-212">杜比2.1：</span><span class="sxs-lookup"><span data-stu-id="a9953-212">Dolby MAT 2.1:</span></span> <br/> <span data-ttu-id="a9953-213">杜比 TrueHD –24位 192KHz/最高可達 18 Mbps、8個通道或 LPCM，最高可達 24 Mbps。</span><span class="sxs-lookup"><span data-stu-id="a9953-213">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="a9953-214">0x0e</span><span class="sxs-lookup"><span data-stu-id="a9953-214">0x0e</span></span>         | <span data-ttu-id="a9953-215">00000164-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-215">00000164-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-216">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ WMA \_ PRO</span><span class="sxs-lookup"><span data-stu-id="a9953-216">KSDATAFORMAT\_SUBTYPE\_IEC61937\_WMA\_PRO</span></span><br/>     | <span data-ttu-id="a9953-217">Windows Media 音訊 (WMA) Pro</span><span class="sxs-lookup"><span data-stu-id="a9953-217">Windows Media Audio (WMA) Pro</span></span>                                                                                                   |



 

<span data-ttu-id="a9953-218">Microsoft 提供的 HD 音訊類別驅動程式支援 PCM、AC3、DTS、AAC、杜比數位 Plus、WMA Pro、 (MLP) 格式。</span><span class="sxs-lookup"><span data-stu-id="a9953-218">Microsoft-provided HD Audio class driver supports PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP) formats.</span></span> <span data-ttu-id="a9953-219">HD 音訊類別驅動程式不支援且可由協力廠商解決方案執行的壓縮音訊格式 Guid，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="a9953-219">The GUIDs for the compressed audio formats that are not supported by the HD audio class driver and can be implemented by third-party solutions are listed in the following table.</span></span>



| <span data-ttu-id="a9953-220">CEA 861 類型</span><span class="sxs-lookup"><span data-stu-id="a9953-220">CEA 861 Type</span></span> | <span data-ttu-id="a9953-221">SubFormat GUID</span><span class="sxs-lookup"><span data-stu-id="a9953-221">SubFormat GUID</span></span>                                                                                              | <span data-ttu-id="a9953-222">Description</span><span class="sxs-lookup"><span data-stu-id="a9953-222">Description</span></span>                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a9953-223">0x08</span><span class="sxs-lookup"><span data-stu-id="a9953-223">0x08</span></span>         | <span data-ttu-id="a9953-224">00000008-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-224">00000008-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-225">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ ATRAC</span><span class="sxs-lookup"><span data-stu-id="a9953-225">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ATRAC</span></span><br/>           | <span data-ttu-id="a9953-226">適應性轉換聲場編碼 (ATRAC) </span><span class="sxs-lookup"><span data-stu-id="a9953-226">Adaptive Transform Acoustic Coding (ATRAC)</span></span>                                     |
| <span data-ttu-id="a9953-227">0x09</span><span class="sxs-lookup"><span data-stu-id="a9953-227">0x09</span></span>         | <span data-ttu-id="a9953-228">00000009-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-228">00000009-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-229">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 一個 \_ 位 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="a9953-229">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ONE\_BIT\_AUDIO</span></span><br/> | <span data-ttu-id="a9953-230">One-Bit 音訊</span><span class="sxs-lookup"><span data-stu-id="a9953-230">One-Bit Audio</span></span>                                                                  |
| <span data-ttu-id="a9953-231">0x0d</span><span class="sxs-lookup"><span data-stu-id="a9953-231">0x0d</span></span>         | <span data-ttu-id="a9953-232">0000000d-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="a9953-232">0000000d-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="a9953-233">KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DST</span><span class="sxs-lookup"><span data-stu-id="a9953-233">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DST</span></span><br/>             | <span data-ttu-id="a9953-234">直接串流傳輸 (DST) —無失真壓縮的 DSD (直接串流數位) 。</span><span class="sxs-lookup"><span data-stu-id="a9953-234">Direct Stream Transport (DST)—lossless compressed DSD (Direct Stream Digital).</span></span> |



 

## <a name="dolby-digital-plus-format"></a><span data-ttu-id="a9953-235">杜比數位加號格式</span><span class="sxs-lookup"><span data-stu-id="a9953-235">Dolby Digital Plus Format</span></span>

<span data-ttu-id="a9953-236">當杜比數位 Plus 內容透過 IEC 60958 傳輸時，連結取樣率必須是內容取樣率的四倍。</span><span class="sxs-lookup"><span data-stu-id="a9953-236">When Dolby Digital Plus content is transmitted over IEC 60958, the link-sampling rate must be four times the sampling rate of the content.</span></span> <span data-ttu-id="a9953-237">杜比數位加號支援 32 KHz、44.1 KHz 和 48 KHz 的內容取樣率。</span><span class="sxs-lookup"><span data-stu-id="a9953-237">Dolby Digital Plus supports content sample rates of 32 KHz, 44.1 KHz, and 48 KHz.</span></span> <span data-ttu-id="a9953-238">HDMI 等介面不支援 128 KHz (32 KHz x 4) ，因此只能支援44.1 和 48 KHz 內容範例速率。</span><span class="sxs-lookup"><span data-stu-id="a9953-238">Interfaces such as HDMI do not support 128 KHz (32 KHz x 4), so only 44.1 and 48 KHz content sample rates can be supported.</span></span>

<span data-ttu-id="a9953-239">下列範例顯示以 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以代表內容取樣率 48 KHz 的杜比數位格式。</span><span class="sxs-lookup"><span data-stu-id="a9953-239">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby Digital Plus format at a content sample rate of 48 KHz are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a><span data-ttu-id="a9953-240">TrueHD () 的杜比</span><span class="sxs-lookup"><span data-stu-id="a9953-240">Dolby TrueHD (MAT)</span></span>

<span data-ttu-id="a9953-241">杜比 TrueHD 內容會透過 IEC 60958 在 176.4 kHz/8 通道上傳輸， (要求 60958 44.1、88.2 和 176.4 kHz 之 705.6 kHz 的) 畫面播放速率，以及 192 kHz/8 通道 (需要適用于60958、768和 48 kHz 之內容取樣速率的 IEC 96 幀) 速率。</span><span class="sxs-lookup"><span data-stu-id="a9953-241">Dolby TrueHD content is transmitted over IEC 60958 at 176.4 kHz / 8 channels (requiring an IEC 60958 frame rate of 705.6 kHz) for content sample rates of 44.1, 88.2 and 176.4 kHz, and 192 kHz / 8 channels (requiring an IEC 60958 frame rate of 768 kHz) for content sample rates of 48, 96 and 192 kHz.</span></span>

<span data-ttu-id="a9953-242">下列範例顯示 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以代表內容取樣率為 96 KHz 的杜比 TrueHD。</span><span class="sxs-lookup"><span data-stu-id="a9953-242">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby TrueHD at a content sample rate of 96 KHz are shown in the following examples.</span></span>

<span data-ttu-id="a9953-243">杜比1。0</span><span class="sxs-lookup"><span data-stu-id="a9953-243">Dolby MAT 1.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="a9953-244">杜比2。0</span><span class="sxs-lookup"><span data-stu-id="a9953-244">Dolby MAT 2.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="a9953-245">杜比2。1</span><span class="sxs-lookup"><span data-stu-id="a9953-245">Dolby MAT 2.1</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> <span data-ttu-id="a9953-246">支援某個版本的杜比，不表示支援較低版本號碼的杜比。</span><span class="sxs-lookup"><span data-stu-id="a9953-246">Support for one version of Dolby MAT does not imply support for Dolby MAT with a lower version number.</span></span> <span data-ttu-id="a9953-247">由於杜比2.1 可回溯相容于舊版的杜比，因此指出支援杜比的類別驅動程式通常也會指出針對每個版本使用不同的 WAVEFORMATEXTENSIBLE IEC61937 結構，以2.0 支援杜比、2.1 和1.0。 \_</span><span class="sxs-lookup"><span data-stu-id="a9953-247">Since Dolby MAT 2.1 is backwards compatible with previous versions of Dolby MAT, a class driver that indicates support for Dolby MAT 2.1 will typically also indicate support for Dolby MAT 2.0 and Dolby MAT 1.0, using a separate WAVEFORMATEXTENSIBLE\_IEC61937 structure for each version.</span></span>

 

## <a name="wma-pro"></a><span data-ttu-id="a9953-248">WMA Pro</span><span class="sxs-lookup"><span data-stu-id="a9953-248">WMA Pro</span></span>

<span data-ttu-id="a9953-249">您可以在下表所列的四個設定檔中的其中一個來編碼 WMA Pro 音訊內容。</span><span class="sxs-lookup"><span data-stu-id="a9953-249">WMA Pro audio content can be encoded in one of the four profiles listed in the following table.</span></span>



| <span data-ttu-id="a9953-250">設定檔</span><span class="sxs-lookup"><span data-stu-id="a9953-250">Profile</span></span> | <span data-ttu-id="a9953-251">屬性-值</span><span class="sxs-lookup"><span data-stu-id="a9953-251">Property - Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="a9953-252">Description</span><span class="sxs-lookup"><span data-stu-id="a9953-252">Description</span></span>                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9953-253">M0</span><span class="sxs-lookup"><span data-stu-id="a9953-253">M0</span></span>      | <span data-ttu-id="a9953-254">最大位元速率– 192000 bps</span><span class="sxs-lookup"><span data-stu-id="a9953-254">Maximum bit rate – 192000 bps</span></span> <br/> <span data-ttu-id="a9953-255">最大取樣率– 48 KHz</span><span class="sxs-lookup"><span data-stu-id="a9953-255">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="a9953-256">最大頻道計數-2</span><span class="sxs-lookup"><span data-stu-id="a9953-256">Maximum channel count – 2</span></span> <br/> <span data-ttu-id="a9953-257">緩衝區大小上限– 600 \* 1024 位</span><span class="sxs-lookup"><span data-stu-id="a9953-257">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="a9953-258">每一框架的樣本數上限-2048</span><span class="sxs-lookup"><span data-stu-id="a9953-258">Maximum samples per frame – 2048</span></span> <br/> <span data-ttu-id="a9953-259">每一框架的最大位數-655536</span><span class="sxs-lookup"><span data-stu-id="a9953-259">Maximum bits per frame - 655536</span></span><br/>   | <span data-ttu-id="a9953-260">建議使用無線音樂和串流。</span><span class="sxs-lookup"><span data-stu-id="a9953-260">Recommended for over-the-air music and streaming.</span></span><br/> <span data-ttu-id="a9953-261">音訊框架中的最大位元速率為 1536000 bps。</span><span class="sxs-lookup"><span data-stu-id="a9953-261">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/>          |
| <span data-ttu-id="a9953-262">M1</span><span class="sxs-lookup"><span data-stu-id="a9953-262">M1</span></span>      | <span data-ttu-id="a9953-263">最大位元速率– 385000 bps</span><span class="sxs-lookup"><span data-stu-id="a9953-263">Maximum bit rate – 385000 bps</span></span> <br/> <span data-ttu-id="a9953-264">最大取樣率– 48 KHz</span><span class="sxs-lookup"><span data-stu-id="a9953-264">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="a9953-265">最大頻道計數–6</span><span class="sxs-lookup"><span data-stu-id="a9953-265">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="a9953-266">緩衝區大小上限– 600 \* 1024 位</span><span class="sxs-lookup"><span data-stu-id="a9953-266">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="a9953-267">每一框架的樣本數上限-4096</span><span class="sxs-lookup"><span data-stu-id="a9953-267">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="a9953-268">每一框架的最大位數-131072</span><span class="sxs-lookup"><span data-stu-id="a9953-268">Maximum bits per frame - 131072</span></span><br/>   | <span data-ttu-id="a9953-269">建議用於環繞音效標準定義影片。</span><span class="sxs-lookup"><span data-stu-id="a9953-269">Recommended for surround-sound standard definition movies.</span></span><br/> <span data-ttu-id="a9953-270">音訊框架中的最大位元速率為 1536000 bps。</span><span class="sxs-lookup"><span data-stu-id="a9953-270">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/> |
| <span data-ttu-id="a9953-271">M2</span><span class="sxs-lookup"><span data-stu-id="a9953-271">M2</span></span>      | <span data-ttu-id="a9953-272">最大位元速率– 769000 bps</span><span class="sxs-lookup"><span data-stu-id="a9953-272">Maximum bit rate – 769000 bps</span></span> <br/> <span data-ttu-id="a9953-273">最大取樣率– 96 KHz</span><span class="sxs-lookup"><span data-stu-id="a9953-273">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="a9953-274">最大頻道計數–6</span><span class="sxs-lookup"><span data-stu-id="a9953-274">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="a9953-275">緩衝區大小上限– 1200 \* 1024 位</span><span class="sxs-lookup"><span data-stu-id="a9953-275">Maximum buffer size – 1200\*1024 bits</span></span> <br/> <span data-ttu-id="a9953-276">每一框架的樣本數上限-4096</span><span class="sxs-lookup"><span data-stu-id="a9953-276">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="a9953-277">每一框架的最大位數-131072</span><span class="sxs-lookup"><span data-stu-id="a9953-277">Maximum bits per frame - 131072</span></span><br/>  | <span data-ttu-id="a9953-278">適用于環繞音效高定義電影的建議。</span><span class="sxs-lookup"><span data-stu-id="a9953-278">Recommended for surround-sound high definition movies.</span></span><br/> <span data-ttu-id="a9953-279">音訊框架中的最大速率是 3072000 bps。</span><span class="sxs-lookup"><span data-stu-id="a9953-279">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>         |
| <span data-ttu-id="a9953-280">M3</span><span class="sxs-lookup"><span data-stu-id="a9953-280">M3</span></span>      | <span data-ttu-id="a9953-281">最大位元速率– 3000000 bps</span><span class="sxs-lookup"><span data-stu-id="a9953-281">Maximum bit rate – 3000000 bps</span></span> <br/> <span data-ttu-id="a9953-282">最大取樣率– 96 KHz</span><span class="sxs-lookup"><span data-stu-id="a9953-282">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="a9953-283">最大頻道計數–8</span><span class="sxs-lookup"><span data-stu-id="a9953-283">Maximum channel count – 8</span></span> <br/> <span data-ttu-id="a9953-284">緩衝區大小上限– 2400 \* 1024 位</span><span class="sxs-lookup"><span data-stu-id="a9953-284">Maximum buffer size – 2400\*1024 bits</span></span> <br/> <span data-ttu-id="a9953-285">每一框架的樣本數上限-4096</span><span class="sxs-lookup"><span data-stu-id="a9953-285">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="a9953-286">每一框架的最大位數-131072</span><span class="sxs-lookup"><span data-stu-id="a9953-286">Maximum bits per frame - 131072</span></span><br/> | <span data-ttu-id="a9953-287">適用于數位劇院的建議。</span><span class="sxs-lookup"><span data-stu-id="a9953-287">Recommended for digital theater.</span></span><br/> <span data-ttu-id="a9953-288">音訊框架中的最大速率是 3072000 bps。</span><span class="sxs-lookup"><span data-stu-id="a9953-288">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>                               |



 

<span data-ttu-id="a9953-289">M0 和 M1 設定檔適用于 48 KHz/16 位/身歷聲 (1536000 bps) IEC 60958 串流。</span><span class="sxs-lookup"><span data-stu-id="a9953-289">The M0 and M1 profiles fit into a 48 KHz/16 bit/Stereo (1536000 bps) IEC 60958 stream.</span></span> <span data-ttu-id="a9953-290">M2 和 M3 設定檔適用于 96 KHz/16 位/身歷聲 (3072000 bps) IEC 60958 串流。</span><span class="sxs-lookup"><span data-stu-id="a9953-290">The M2 and M3 profiles fit into a 96 KHz/16 bit/Stereo (3072000 bps) IEC 60958 stream.</span></span>

<span data-ttu-id="a9953-291">下列範例顯示 WAVEFORMATEXTENSIBLE IEC61937 結構中的應用程式所設定的值 \_ ，以將 WMA Pro 表示為 M2 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9953-291">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent WMA Pro as an M2 profile are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a><span data-ttu-id="a9953-292">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9953-292">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9953-293">裝置格式</span><span class="sxs-lookup"><span data-stu-id="a9953-293">Device Formats</span></span>](device-formats.md)
</dt> </dl>

 

 




