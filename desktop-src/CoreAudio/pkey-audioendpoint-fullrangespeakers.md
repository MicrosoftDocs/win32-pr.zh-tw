---
description: PKEY \_ AudioEndpoint \_ FullRangeSpeakers 屬性會為連線到音訊端點裝置的全範圍喇叭指定通道設定遮罩。
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: 'PKEY_AudioEndpoint_FullRangeSpeakers (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111325"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="cea16-103">PKEY \_ AudioEndpoint \_ FullRangeSpeakers</span><span class="sxs-lookup"><span data-stu-id="cea16-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="cea16-104">**PKEY \_ AudioEndpoint \_ FullRangeSpeakers** 屬性會為連線到音訊端點裝置的全範圍喇叭指定通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="cea16-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="cea16-105">遮罩表示全範圍喇叭的實體設定，並指定將通道指派給這些喇叭。</span><span class="sxs-lookup"><span data-stu-id="cea16-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="cea16-106">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="cea16-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="cea16-107">**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 **UINT** 型別的通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="cea16-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="cea16-108">全範圍的喇叭可以從低音到高音的全範圍播放音效。</span><span class="sxs-lookup"><span data-stu-id="cea16-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="cea16-109">通常，較大的喇叭是完整範圍，但較小的喇叭的播放低音音效會大幅降低。</span><span class="sxs-lookup"><span data-stu-id="cea16-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="cea16-110">在 Windows Vista 中，音訊引擎會使用此屬性來管理音訊輸出串流中音訊端點裝置所播放的低音等級。</span><span class="sxs-lookup"><span data-stu-id="cea16-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="cea16-111">這個屬性的通道設定遮罩與 [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) 屬性的通道設定遮罩具有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="cea16-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="cea16-112">如需通道設定遮罩的詳細資訊，請參閱下列各項：</span><span class="sxs-lookup"><span data-stu-id="cea16-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="cea16-113">\_ \_ Windows DDK 檔中 KSPROPERTY 音訊通道設定屬性的描述 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cea16-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="cea16-114">標題為「家用劇院喇叭設定的音訊驅動程式支援」的白皮書， [適用于 Windows 網站的音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx) 。</span><span class="sxs-lookup"><span data-stu-id="cea16-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="cea16-115">系統會 \_ 從使用者取得 PKEY AudioEndpoint FullRangeSpeakers 屬性的通道設定遮罩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cea16-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="cea16-116">使用者透過 [Windows 多媒體] 控制台輸入此資訊，Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="cea16-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="cea16-117">如需 Mmsys.cpl 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="cea16-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="cea16-118">\_音訊端點裝置的 PKEY AudioEndpoint FullRangeSpeakers 屬性的通道設定遮罩 \_ 是 \_ 相同裝置之 PKEY AudioEndpoint PhysicalSpeakers 屬性的通道設定遮罩的子集 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cea16-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="cea16-119">例如，如果音訊端點裝置會驅動一組5.1 環繞音效的喇叭，則 [PKEY AudioEndpoint PhysicalSpeakers] 屬性的通道設定遮罩 \_ \_ 就是 KSAUDIO \_ 喇叭 \_ 5POINT1。</span><span class="sxs-lookup"><span data-stu-id="cea16-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="cea16-120">此遮罩表示前端、前端、前端、側邊和側邊右喇叭的存在，以及喇叭。</span><span class="sxs-lookup"><span data-stu-id="cea16-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="cea16-121">如果左上角和右上方的喇叭大到足以產生低音音效，但較小的前端和側喇叭不是，則 PKEY AudioEndpoint FullRangeSpeakers 內容的通道設定遮罩 \_ \_ 是 KSAUDIO \_ \_ 的喇叭，它只會指出左右喇叭。</span><span class="sxs-lookup"><span data-stu-id="cea16-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="cea16-122">通道設定遮罩 KSAUDIO \_ 喇叭 \_ 5POINT1 和 KSAUDIO \_ 喇叭 \_ 身歷聲定義于標頭檔 Ksmedia .h 中。</span><span class="sxs-lookup"><span data-stu-id="cea16-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea16-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cea16-123">Requirements</span></span>



| <span data-ttu-id="cea16-124">需求</span><span class="sxs-lookup"><span data-stu-id="cea16-124">Requirement</span></span> | <span data-ttu-id="cea16-125">值</span><span class="sxs-lookup"><span data-stu-id="cea16-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea16-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cea16-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cea16-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cea16-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cea16-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cea16-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cea16-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cea16-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cea16-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cea16-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea16-131"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cea16-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea16-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cea16-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea16-133">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="cea16-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="cea16-134">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="cea16-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="cea16-135">**PKEY \_ AudioEndpoint \_ PhysicalSpeakers 屬性**</span><span class="sxs-lookup"><span data-stu-id="cea16-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




