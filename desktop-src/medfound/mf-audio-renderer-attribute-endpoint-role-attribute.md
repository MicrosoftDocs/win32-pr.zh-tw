---
description: 指定音訊轉譯器的音訊端點角色。
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944590"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="84d97-103">MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 端點 \_ 角色屬性</span><span class="sxs-lookup"><span data-stu-id="84d97-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="84d97-104">指定音訊轉譯器的音訊端點角色。</span><span class="sxs-lookup"><span data-stu-id="84d97-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="84d97-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="84d97-105">Data type</span></span>

<span data-ttu-id="84d97-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="84d97-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="84d97-107">備註</span><span class="sxs-lookup"><span data-stu-id="84d97-107">Remarks</span></span>

<span data-ttu-id="84d97-108">您可以使用這個屬性來設定音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="84d97-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="84d97-109">使用方式取決於您呼叫來建立音訊轉譯器的函式：</span><span class="sxs-lookup"><span data-stu-id="84d97-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="84d97-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="84d97-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="84d97-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="84d97-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="84d97-112">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="84d97-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="84d97-113">音訊端點裝置是一種硬體裝置，位於音訊資料路徑的一端，例如耳機或喇叭。</span><span class="sxs-lookup"><span data-stu-id="84d97-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="84d97-114">如果設定此屬性，音訊轉譯器會針對指定的角色使用預設音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="84d97-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="84d97-115">這個屬性的值是 **ERole** 列舉的成員，定義于標頭檔 mmdeviceapi 中。</span><span class="sxs-lookup"><span data-stu-id="84d97-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="84d97-116">如需詳細資訊，請參閱核心音訊 API 檔。</span><span class="sxs-lookup"><span data-stu-id="84d97-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="84d97-117">如果未設定此屬性，音訊轉譯器會使用預設端點裝置。</span><span class="sxs-lookup"><span data-stu-id="84d97-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="84d97-118">如果設定這個屬性，請勿設定 [ [**MF 音訊轉譯 \_ 器 \_ \_ 屬性 \_ 端點 \_ 識別碼**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="84d97-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="84d97-119">如果同時設定了這兩個屬性，則在建立音訊轉譯器時將會發生失敗。</span><span class="sxs-lookup"><span data-stu-id="84d97-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="84d97-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="84d97-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d97-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="84d97-121">Requirements</span></span>



| <span data-ttu-id="84d97-122">需求</span><span class="sxs-lookup"><span data-stu-id="84d97-122">Requirement</span></span> | <span data-ttu-id="84d97-123">值</span><span class="sxs-lookup"><span data-stu-id="84d97-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84d97-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84d97-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84d97-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84d97-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84d97-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84d97-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84d97-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84d97-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="84d97-128">標頭</span><span class="sxs-lookup"><span data-stu-id="84d97-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="84d97-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="84d97-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d97-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84d97-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d97-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="84d97-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84d97-132">音訊轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="84d97-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="84d97-133">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="84d97-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="84d97-134">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="84d97-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="84d97-135">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="84d97-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




