---
description: 指定串流音訊轉譯器的音訊串流類別 (SAR) 。
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971709"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="6311e-103">MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 資料流程 \_ 類別目錄屬性</span><span class="sxs-lookup"><span data-stu-id="6311e-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="6311e-104">指定 [串流音訊](streaming-audio-renderer.md) 轉譯器的音訊串流類別 (SAR) 。</span><span class="sxs-lookup"><span data-stu-id="6311e-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="6311e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6311e-105">Data type</span></span>

<span data-ttu-id="6311e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6311e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6311e-107">備註</span><span class="sxs-lookup"><span data-stu-id="6311e-107">Remarks</span></span>

<span data-ttu-id="6311e-108">您可以使用這個屬性來設定音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="6311e-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="6311e-109">使用方式取決於您所呼叫用來建立音訊轉譯器的函式。</span><span class="sxs-lookup"><span data-stu-id="6311e-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="6311e-110">函式</span><span class="sxs-lookup"><span data-stu-id="6311e-110">Function</span></span>                                                               | <span data-ttu-id="6311e-111">如何設定屬性</span><span class="sxs-lookup"><span data-stu-id="6311e-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6311e-112">**MFCreateAudioRenderer**</span><span class="sxs-lookup"><span data-stu-id="6311e-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="6311e-113">使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)指標。</span><span class="sxs-lookup"><span data-stu-id="6311e-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="6311e-114">**MFCreateAudioRendererActivate**</span><span class="sxs-lookup"><span data-stu-id="6311e-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="6311e-115">使用 *ppActivate* 參數中所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標。</span><span class="sxs-lookup"><span data-stu-id="6311e-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="6311e-116">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="6311e-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="6311e-117">屬性的值是 [**音訊 \_ 串流 \_ 類別**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="6311e-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="6311e-118">當多個應用程式同時播放音訊時，音訊服務會使用串流類別來判斷音訊原則。</span><span class="sxs-lookup"><span data-stu-id="6311e-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6311e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6311e-119">Requirements</span></span>



| <span data-ttu-id="6311e-120">需求</span><span class="sxs-lookup"><span data-stu-id="6311e-120">Requirement</span></span> | <span data-ttu-id="6311e-121">值</span><span class="sxs-lookup"><span data-stu-id="6311e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6311e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6311e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6311e-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6311e-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6311e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6311e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6311e-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6311e-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6311e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6311e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6311e-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6311e-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6311e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6311e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6311e-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6311e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
