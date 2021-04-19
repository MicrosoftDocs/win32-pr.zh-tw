---
description: 包含用來設定音訊轉譯器的旗標。
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998267"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="a535b-103">MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="a535b-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="a535b-104">包含用來設定音訊轉譯器的旗標。</span><span class="sxs-lookup"><span data-stu-id="a535b-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="a535b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a535b-105">Data type</span></span>

<span data-ttu-id="a535b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a535b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a535b-107">備註</span><span class="sxs-lookup"><span data-stu-id="a535b-107">Remarks</span></span>

<span data-ttu-id="a535b-108">這個屬性的值是下列旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="a535b-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="a535b-109">值</span><span class="sxs-lookup"><span data-stu-id="a535b-109">Value</span></span>                                                   | <span data-ttu-id="a535b-110">描述</span><span class="sxs-lookup"><span data-stu-id="a535b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a535b-111">**MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標 \_ CROSSPROCESS**</span><span class="sxs-lookup"><span data-stu-id="a535b-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="a535b-112">音訊轉譯器使用跨進程音訊會話。</span><span class="sxs-lookup"><span data-stu-id="a535b-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="a535b-113">這個旗標可讓多個進程中的音訊轉譯器共用相同的音訊會話，以及相關聯的磁片區和原則控制項。</span><span class="sxs-lookup"><span data-stu-id="a535b-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="a535b-114">如果未設定此旗標，其他進程中的音訊轉譯器無法共用音訊會話。</span><span class="sxs-lookup"><span data-stu-id="a535b-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="a535b-115">**MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 旗標 \_ NOPERSIST**</span><span class="sxs-lookup"><span data-stu-id="a535b-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="a535b-116">Windows 音訊會話 API (WASAPI) 不會保存此音訊會話的屬性，例如會話量。</span><span class="sxs-lookup"><span data-stu-id="a535b-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="a535b-117">如果未設定此旗標，WASAPI 會保存音訊會話屬性。</span><span class="sxs-lookup"><span data-stu-id="a535b-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="a535b-118">您可以使用這個屬性來設定音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="a535b-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="a535b-119">使用方式取決於您呼叫來建立音訊轉譯器的函式：</span><span class="sxs-lookup"><span data-stu-id="a535b-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="a535b-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a535b-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="a535b-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a535b-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="a535b-122">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="a535b-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="a535b-123">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a535b-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a535b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a535b-124">Requirements</span></span>



| <span data-ttu-id="a535b-125">需求</span><span class="sxs-lookup"><span data-stu-id="a535b-125">Requirement</span></span> | <span data-ttu-id="a535b-126">值</span><span class="sxs-lookup"><span data-stu-id="a535b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a535b-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a535b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a535b-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a535b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a535b-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a535b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a535b-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a535b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a535b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a535b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a535b-132"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a535b-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a535b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a535b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a535b-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a535b-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a535b-135">音訊轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="a535b-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a535b-136">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a535b-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a535b-137">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a535b-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a535b-138">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="a535b-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




