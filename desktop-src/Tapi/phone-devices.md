---
description: 電話裝置支援是互補的，而不是基本的，因此服務提供者不需要支援電話裝置。
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: 電話裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943598"
---
# <a name="phone-devices"></a><span data-ttu-id="6a056-103">電話裝置</span><span class="sxs-lookup"><span data-stu-id="6a056-103">Phone Devices</span></span>

<span data-ttu-id="6a056-104">電話裝置支援是互補的，而不是基本的，因此服務提供者不需要支援電話裝置。</span><span class="sxs-lookup"><span data-stu-id="6a056-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="6a056-105">就像線路裝置類別是實體線路裝置的抽象概念，phone 裝置類別代表與裝置無關的電話組抽象概念。</span><span class="sxs-lookup"><span data-stu-id="6a056-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="6a056-106">TAPI 會將線路和電話裝置視為彼此獨立的裝置。</span><span class="sxs-lookup"><span data-stu-id="6a056-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="6a056-107">換句話說，您可以在不使用相關行的情況下，使用電話 (裝置) ，也可以在不使用電話的情況下使用線路 (裝置) 。</span><span class="sxs-lookup"><span data-stu-id="6a056-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="6a056-108">完全採用此獨立性的服務提供者可提供這些裝置的使用，這些裝置不是由傳統的電話語音通訊協定所定義。</span><span class="sxs-lookup"><span data-stu-id="6a056-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="6a056-109">例如，使用者可以使用桌上型電腦電話的話筒作為語音錄製或播放的波形音訊裝置，可能不會因為切換電話正在使用中而不知道。</span><span class="sxs-lookup"><span data-stu-id="6a056-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="6a056-110">在這種情況下，將本機電話聽筒不需要自動傳送 offhook 信號至交換器。</span><span class="sxs-lookup"><span data-stu-id="6a056-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="6a056-111">這種獨立性也可讓應用程式以與來電無關的方式來撥打局域電話。</span><span class="sxs-lookup"><span data-stu-id="6a056-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="6a056-112">服務提供者的功能受限於用來將交換器、電話和電腦互連的硬體和軟體功能。</span><span class="sxs-lookup"><span data-stu-id="6a056-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="6a056-113">TAPI 包含可取得裝置功能的函式，可讓用戶端判斷是否支援這類使用模型。</span><span class="sxs-lookup"><span data-stu-id="6a056-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="6a056-114">本節說明電話裝置，並說明如何使用 TAPI 電話功能來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="6a056-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="6a056-115">手機裝置</span><span class="sxs-lookup"><span data-stu-id="6a056-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="6a056-116">初始化和關閉</span><span class="sxs-lookup"><span data-stu-id="6a056-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



