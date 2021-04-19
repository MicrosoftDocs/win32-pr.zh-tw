---
description: Windows Media 音訊聲音編碼程式已針對以高壓縮率編碼人類聲音進行優化。 這是最適合串流的編碼程式，大部分是由說出的單字所組成。
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: 'Windows Media 音訊語音編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001172"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="4c5ff-104">Windows Media 音訊語音編碼器</span><span class="sxs-lookup"><span data-stu-id="4c5ff-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="4c5ff-105">Windows Media 音訊聲音編碼程式已針對以高壓縮率編碼人類聲音進行優化。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="4c5ff-106">這是最適合串流的編碼程式，大部分是由說出的單字所組成。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4c5ff-107">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="4c5ff-107">Class Identifier</span></span>

<span data-ttu-id="4c5ff-108">Windows Media 音訊聲音編碼器 (CLSID) 的類別識別碼會以常數 **CLSID \_ CWMSPEncMediaObject2** 表示。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="4c5ff-109">您可以藉由呼叫 **CoCreateInstance** 來建立語音編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="4c5ff-110">輸出格式</span><span class="sxs-lookup"><span data-stu-id="4c5ff-110">Output Formats</span></span>

<span data-ttu-id="4c5ff-111">Windows Media 音訊的語音編碼內容是以格式標記0x00A 來識別。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="4c5ff-112">編碼器屬性</span><span class="sxs-lookup"><span data-stu-id="4c5ff-112">Encoder Properties</span></span>

<span data-ttu-id="4c5ff-113">Windows Media 音訊語音編碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4c5ff-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4c5ff-114">Property</span></span></th>
<th><span data-ttu-id="4c5ff-115">描述</span><span class="sxs-lookup"><span data-stu-id="4c5ff-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c5ff-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="4c5ff-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="4c5ff-117">指定用於語音編解碼器的緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="4c5ff-118">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-118">Windows XP and later.</span></span><br />
<span data-ttu-id="4c5ff-119">唯寫。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5ff-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="4c5ff-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="4c5ff-121">指定包單位中的編碼器延遲。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="4c5ff-122">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-122">Windows XP and later.</span></span><br />
<span data-ttu-id="4c5ff-123">唯寫。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5ff-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="4c5ff-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="4c5ff-125">指定要使用語音編解碼器將內容編碼為音樂的部分內容。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="4c5ff-126">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-126">Windows XP and later.</span></span><br />
<span data-ttu-id="4c5ff-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4c5ff-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5ff-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="4c5ff-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="4c5ff-129">指定語音編解碼器的模式。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="4c5ff-130">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4c5ff-130">Windows XP and later.</span></span><br />
<span data-ttu-id="4c5ff-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4c5ff-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="4c5ff-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c5ff-132">Requirements</span></span>



| <span data-ttu-id="4c5ff-133">需求</span><span class="sxs-lookup"><span data-stu-id="4c5ff-133">Requirement</span></span> | <span data-ttu-id="4c5ff-134">值</span><span class="sxs-lookup"><span data-stu-id="4c5ff-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5ff-135">用戶端</span><span class="sxs-lookup"><span data-stu-id="4c5ff-135">Client</span></span><br/> | <span data-ttu-id="4c5ff-136">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c5ff-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="4c5ff-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4c5ff-137">Header</span></span><br/> | <dl> <span data-ttu-id="4c5ff-138"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c5ff-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4c5ff-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5ff-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="4c5ff-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5ff-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5ff-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c5ff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5ff-142">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="4c5ff-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="4c5ff-143">使用 Windows Media 音訊語音編解碼器</span><span class="sxs-lookup"><span data-stu-id="4c5ff-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




