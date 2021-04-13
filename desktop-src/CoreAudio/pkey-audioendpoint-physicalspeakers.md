---
description: 深入瞭解： PKEY_AudioEndpoint_PhysicalSpeakers
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: 'PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510681"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="97786-103">PKEY \_ AudioEndpoint \_ PhysicalSpeakers</span><span class="sxs-lookup"><span data-stu-id="97786-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="97786-104">**PKEY \_ AudioEndpoint \_ PhysicalSpeakers** 屬性會指定音訊端點裝置的通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="97786-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="97786-105">遮罩會指出一組喇叭的實體設定，並指定喇叭的通道指派。</span><span class="sxs-lookup"><span data-stu-id="97786-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="97786-106">如需通道設定遮罩的詳細資訊，請參閱下列各項：</span><span class="sxs-lookup"><span data-stu-id="97786-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="97786-107">\_ \_ Windows DDK 檔中 KSPROPERTY 音訊通道設定屬性的描述 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97786-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="97786-108">標題為「家用劇院喇叭設定的音訊驅動程式支援」的白皮書， [適用于 Windows 網站的音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx) 。</span><span class="sxs-lookup"><span data-stu-id="97786-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="97786-109">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="97786-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="97786-110">**PROPVARIANT** 結構的 **uintVal** 成員包含轉換成 **UINT** 型別的通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="97786-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="97786-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="97786-111">Requirements</span></span>



| <span data-ttu-id="97786-112">需求</span><span class="sxs-lookup"><span data-stu-id="97786-112">Requirement</span></span> | <span data-ttu-id="97786-113">值</span><span class="sxs-lookup"><span data-stu-id="97786-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97786-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97786-114">Minimum supported client</span></span><br/> | <span data-ttu-id="97786-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97786-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97786-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97786-116">Minimum supported server</span></span><br/> | <span data-ttu-id="97786-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97786-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97786-118">標頭</span><span class="sxs-lookup"><span data-stu-id="97786-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="97786-119"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="97786-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97786-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97786-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97786-121">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="97786-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="97786-122">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="97786-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




