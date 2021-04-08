---
description: 指定音訊轉譯器的音訊原則類別。
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850691"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="8e3d6-103">MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 會話 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="8e3d6-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="8e3d6-104">指定音訊轉譯器的音訊原則類別。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e3d6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8e3d6-105">Data type</span></span>

<span data-ttu-id="8e3d6-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8e3d6-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3d6-107">備註</span><span class="sxs-lookup"><span data-stu-id="8e3d6-107">Remarks</span></span>

<span data-ttu-id="8e3d6-108">這個屬性會將音訊轉譯器與音訊原則類別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="8e3d6-109">每個原則類別都有自己的磁片區和原則控制。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="8e3d6-110">如果未設定此屬性，新的 SAR 會聯結應用程式的預設音訊會話。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="8e3d6-111">如需詳細資訊，請參閱 core 音訊 API 檔中的 [**IAudioClient：： Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) 。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="8e3d6-112">您可以使用這個屬性來設定音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="8e3d6-113">使用方式取決於您呼叫來建立音訊轉譯器的函式：</span><span class="sxs-lookup"><span data-stu-id="8e3d6-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="8e3d6-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="8e3d6-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="8e3d6-116">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="8e3d6-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8e3d6-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3d6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e3d6-118">Requirements</span></span>



| <span data-ttu-id="8e3d6-119">需求</span><span class="sxs-lookup"><span data-stu-id="8e3d6-119">Requirement</span></span> | <span data-ttu-id="8e3d6-120">值</span><span class="sxs-lookup"><span data-stu-id="8e3d6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3d6-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e3d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3d6-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e3d6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e3d6-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e3d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3d6-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e3d6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e3d6-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8e3d6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e3d6-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3d6-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e3d6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e3d6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3d6-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8e3d6-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e3d6-129">音訊轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="8e3d6-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e3d6-130">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="8e3d6-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="8e3d6-131">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="8e3d6-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="8e3d6-132">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="8e3d6-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
