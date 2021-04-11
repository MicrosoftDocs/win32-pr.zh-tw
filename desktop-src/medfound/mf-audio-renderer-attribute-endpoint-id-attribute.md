---
description: 指定音訊端點裝置的識別碼。
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: 'MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318815"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="0541a-103">MF \_ 音訊轉譯器 \_ \_ 屬性 \_ 端點 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="0541a-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="0541a-104">指定音訊端點裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0541a-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="0541a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0541a-105">Data type</span></span>

<span data-ttu-id="0541a-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="0541a-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="0541a-107">備註</span><span class="sxs-lookup"><span data-stu-id="0541a-107">Remarks</span></span>

<span data-ttu-id="0541a-108">您可以使用這個屬性來設定音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="0541a-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="0541a-109">使用方式取決於您呼叫來建立音訊轉譯器的函式：</span><span class="sxs-lookup"><span data-stu-id="0541a-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="0541a-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)：使用 *pAudioAttributes* 參數中指定的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0541a-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="0541a-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)：使用在 *ppActivate* 參數中抓取的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)介面指標來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0541a-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="0541a-112">呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="0541a-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="0541a-113">音訊端點裝置是一種硬體裝置，位於音訊資料路徑的一端，例如耳機或喇叭。</span><span class="sxs-lookup"><span data-stu-id="0541a-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="0541a-114">若要取得音訊端點識別碼，請使用下列核心音訊 Api：</span><span class="sxs-lookup"><span data-stu-id="0541a-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="0541a-115">您可以使用 [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面來列舉系統上的裝置。</span><span class="sxs-lookup"><span data-stu-id="0541a-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="0541a-116">呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 來取得裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0541a-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="0541a-117">如需詳細資訊，請參閱 [核心音訊](../coreaudio/core-audio-apis-in-windows-vista.md) API 檔。</span><span class="sxs-lookup"><span data-stu-id="0541a-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="0541a-118">如果未設定此屬性，音訊轉譯器會使用預設端點裝置。</span><span class="sxs-lookup"><span data-stu-id="0541a-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="0541a-119">如果設定這個屬性，請勿設定 [ [**MF 音訊轉譯 \_ 器 \_ 屬性 \_ ] \_ 端點 \_ 角色**](mf-audio-renderer-attribute-endpoint-role-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0541a-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="0541a-120">如果同時設定了這兩個屬性，則在建立音訊轉譯器時將會發生失敗。</span><span class="sxs-lookup"><span data-stu-id="0541a-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="0541a-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="0541a-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0541a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0541a-122">Requirements</span></span>



| <span data-ttu-id="0541a-123">需求</span><span class="sxs-lookup"><span data-stu-id="0541a-123">Requirement</span></span> | <span data-ttu-id="0541a-124">值</span><span class="sxs-lookup"><span data-stu-id="0541a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0541a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0541a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0541a-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0541a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0541a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0541a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0541a-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0541a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0541a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0541a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0541a-130"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0541a-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0541a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0541a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0541a-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0541a-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0541a-133">音訊轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="0541a-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0541a-134">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="0541a-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="0541a-135">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="0541a-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="0541a-136">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="0541a-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
