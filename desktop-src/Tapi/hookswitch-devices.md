---
description: 電話裝置可以有多個 hookswitch 裝置。
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Hookswitch 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512396"
---
# <a name="hookswitch-devices"></a><span data-ttu-id="2521b-103">Hookswitch 裝置</span><span class="sxs-lookup"><span data-stu-id="2521b-103">Hookswitch Devices</span></span>

<span data-ttu-id="2521b-104">電話裝置可以有多個 hookswitch 裝置。</span><span class="sxs-lookup"><span data-stu-id="2521b-104">A phone device can have multiple hookswitch devices.</span></span> <span data-ttu-id="2521b-105">Hookswitch 是連接或中斷裝置與電話線連線的交換器。</span><span class="sxs-lookup"><span data-stu-id="2521b-105">A hookswitch is the switch that connects or disconnects a device from the phone line.</span></span> <span data-ttu-id="2521b-106">例如，在電話上，當使用者從底座中提起接收器以取得新的撥號音時，就會自動啟用此參數。</span><span class="sxs-lookup"><span data-stu-id="2521b-106">On a telephone, for example, this is the switch that is automatically activated when a user lifts the receiver from the cradle to get a new dial tone.</span></span> <span data-ttu-id="2521b-107">TAPI 為電話定義三種類型的 hookswitch 裝置：話筒、話筒和耳機。</span><span class="sxs-lookup"><span data-stu-id="2521b-107">TAPI defines three types of hookswitch devices for a phone: handset, speakerphone, and headset.</span></span> <span data-ttu-id="2521b-108">每個 hookswitch 裝置都有一個喇叭和一個麥克風元件，並以四種 hookswitch 模式的其中一種運作：</span><span class="sxs-lookup"><span data-stu-id="2521b-108">Each hookswitch device has a speaker and a microphone component, and operates in one of four hookswitch modes:</span></span>

-   <span data-ttu-id="2521b-109">**Onhook** Hookswitch 裝置是 onhook，而且其麥克風和喇叭都已停用。</span><span class="sxs-lookup"><span data-stu-id="2521b-109">**Onhook** The hookswitch device is onhook, and both its microphone and speaker are disabled.</span></span>
-   <span data-ttu-id="2521b-110">**僅限麥克風** Hookswitch 裝置為 offhook、其麥克風已啟用，且其喇叭為靜音。</span><span class="sxs-lookup"><span data-stu-id="2521b-110">**Microphone only** The hookswitch device is offhook, its microphone is enabled, and its speaker is mute.</span></span>
-   <span data-ttu-id="2521b-111">**僅限說話者** Hookswitch 裝置是 offhook，其麥克風為靜音，並已啟用其喇叭。</span><span class="sxs-lookup"><span data-stu-id="2521b-111">**Speaker only** The hookswitch device is offhook, its microphone is mute, and its speaker is enabled.</span></span>
-   <span data-ttu-id="2521b-112">**麥克風和喇叭** Hookswitch 裝置是 offhook，而且會啟用麥克風和喇叭。</span><span class="sxs-lookup"><span data-stu-id="2521b-112">**Microphone and speaker** The hookswitch device is offhook, and both microphone and speaker are enabled.</span></span>

<span data-ttu-id="2521b-113">[**PhoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch)函式是用來設定一或多個開啟的電話裝置 hookswitch 裝置的 hookswitch 模式。</span><span class="sxs-lookup"><span data-stu-id="2521b-113">The [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) function is used to set the hookswitch mode of one or more of the hookswitch devices of an open phone device.</span></span> <span data-ttu-id="2521b-114">例如，若要將 hookswitch 裝置的麥克風或喇叭元件靜音或取消靜音，請使用 **phoneSetHookSwitch** 搭配適當的 hookswitch 模式。</span><span class="sxs-lookup"><span data-stu-id="2521b-114">For example, to mute or unmute the microphone or speaker component of a hookswitch device, use **phoneSetHookSwitch** with the appropriate hookswitch mode.</span></span> <span data-ttu-id="2521b-115">[**PhoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch)函式可用來查詢 open phone 裝置之 hookswitch 裝置的 hookswitch 模式。</span><span class="sxs-lookup"><span data-stu-id="2521b-115">The [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) function can be used to query the hookswitch mode of a hookswitch device of an open phone device.</span></span>

<span data-ttu-id="2521b-116">以手動方式變更手機 hookswitch 裝置的模式時（例如從其底座中取出話筒），會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。</span><span class="sxs-lookup"><span data-stu-id="2521b-116">When the mode of a phone's hookswitch device is changed manually, for example by lifting the handset from its cradle, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="2521b-117">此訊息的參數提供了變更的指示。</span><span class="sxs-lookup"><span data-stu-id="2521b-117">Parameters to this message provide an indication of the change.</span></span>

<span data-ttu-id="2521b-118">Hookswitch 裝置的喇叭元件數量可以使用 [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)來設定。</span><span class="sxs-lookup"><span data-stu-id="2521b-118">The volume of the speaker component of a hookswitch device can be set with [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume).</span></span> <span data-ttu-id="2521b-119">音量設定不同于靜音的喇叭和更新版本靜音它會保留喇叭的音量設定。</span><span class="sxs-lookup"><span data-stu-id="2521b-119">Volume setting is different from mute in that muting a speaker and later unmuting it will preserve the volume setting of the speaker.</span></span> <span data-ttu-id="2521b-120">[**PhoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)函式可用來傳回開啟的電話裝置之 hookswitch 裝置喇叭的目前磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="2521b-120">The [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) function can be used to return the current volume setting of a hookswitch device's speaker of an open phone device.</span></span>

<span data-ttu-id="2521b-121">Hookswitch 裝置的麥克風元件也可以獲得控制。</span><span class="sxs-lookup"><span data-stu-id="2521b-121">The microphone component of a hookswitch device can also be gain controlled.</span></span> <span data-ttu-id="2521b-122">[增益] 設定不同于靜音的麥克風和後續靜音它將會保留麥克風的 [增益] 設定。</span><span class="sxs-lookup"><span data-stu-id="2521b-122">Gain setting is different from mute in that muting a microphone and later unmuting it will preserve the gain setting of the microphone.</span></span> <span data-ttu-id="2521b-123">使用 [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) 來設定 hookswitch 裝置麥克風的 open phone 裝置，並使用 [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) 來傳回已開啟之手機的 hookswitch 裝置麥克風增益設定。</span><span class="sxs-lookup"><span data-stu-id="2521b-123">Use [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) to set the gain of a hookswitch device's microphone of an open phone device, and [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) to return the gain setting of a hookswitch device's microphone of an opened phone.</span></span>

<span data-ttu-id="2521b-124">當行動電話的音量或增益變更時， \_ 就會將電話狀態訊息傳送至應用程式函式，以通知應用程式狀態變更。</span><span class="sxs-lookup"><span data-stu-id="2521b-124">When the volume or gain of a phone's hookswitch device is changed, a PHONE\_STATE message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="2521b-125">此訊息的參數提供了變更的指示。</span><span class="sxs-lookup"><span data-stu-id="2521b-125">Parameters to this message provide an indication of the change.</span></span>

 

 



