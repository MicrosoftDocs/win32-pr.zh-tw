---
description: Windows Media 音訊的語音編碼器會將 Windows Media 音訊語音編碼器編碼的資料流程解碼。
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: 'Windows Media 音訊語音解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001814"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="252c2-103">Windows Media 音訊語音解碼器</span><span class="sxs-lookup"><span data-stu-id="252c2-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="252c2-104">Windows Media 音訊的語音編碼器會將 [**Windows Media 音訊語音編碼器**](windowsmediaaudiovoiceencoder.md)編碼的資料流程解碼。</span><span class="sxs-lookup"><span data-stu-id="252c2-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="252c2-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="252c2-105">Class Identifier</span></span>

<span data-ttu-id="252c2-106">Windows Media 音訊語音解碼 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMSPDecMediaObject** 表示。</span><span class="sxs-lookup"><span data-stu-id="252c2-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="252c2-107">您可以藉由呼叫 **CoCreateInstance** 來建立語音解碼的實例。</span><span class="sxs-lookup"><span data-stu-id="252c2-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="252c2-108">輸入格式</span><span class="sxs-lookup"><span data-stu-id="252c2-108">Input Formats</span></span>

<span data-ttu-id="252c2-109">Windows Media 音訊的語音編碼內容是以格式標記0x00A 來識別。</span><span class="sxs-lookup"><span data-stu-id="252c2-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="252c2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="252c2-110">Requirements</span></span>



| <span data-ttu-id="252c2-111">需求</span><span class="sxs-lookup"><span data-stu-id="252c2-111">Requirement</span></span> | <span data-ttu-id="252c2-112">值</span><span class="sxs-lookup"><span data-stu-id="252c2-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="252c2-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="252c2-113">Client</span></span><br/> | <span data-ttu-id="252c2-114">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="252c2-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="252c2-115">標頭</span><span class="sxs-lookup"><span data-stu-id="252c2-115">Header</span></span><br/> | <dl> <span data-ttu-id="252c2-116"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="252c2-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="252c2-117">DLL</span><span class="sxs-lookup"><span data-stu-id="252c2-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="252c2-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="252c2-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252c2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="252c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252c2-120">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="252c2-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="252c2-121">使用 Windows Media 音訊語音編解碼器</span><span class="sxs-lookup"><span data-stu-id="252c2-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="252c2-122">Windows Media 音訊語音編碼器</span><span class="sxs-lookup"><span data-stu-id="252c2-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




