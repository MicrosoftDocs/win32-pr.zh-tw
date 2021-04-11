---
description: 與舊版音訊 Api 的互通性
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: 與舊版音訊 Api 的互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936413"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="74ba4-103">與舊版音訊 Api 的互通性</span><span class="sxs-lookup"><span data-stu-id="74ba4-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="74ba4-104">許多現有的應用程式都使用舊版音訊 Api，例如 DirectSound、DirectShow 和 Windows 多媒體功能。</span><span class="sxs-lookup"><span data-stu-id="74ba4-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="74ba4-105">只要稍微修改一次，就可以增強這些應用程式，在 Windows Vista 中使用 [裝置角色](device-roles.md)、 [會話磁片區控制項](session-volume-controls.md)，以及核心音訊 api 的其他功能。</span><span class="sxs-lookup"><span data-stu-id="74ba4-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="74ba4-106">如同在 [使用者模式音訊元件](user-mode-audio-components.md)中所討論，核心音訊 api 可作為建立較高層級音訊 api 的基礎。</span><span class="sxs-lookup"><span data-stu-id="74ba4-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="74ba4-107">在 Windows Vista 中，應用程式透過舊版音訊 Api （例如 DirectSound 和 Windows media **waveOutXxx** 和 **waveInXxx** 功能）存取的音訊裝置，實際上是由核心音訊 api 所執行的 [音訊端點裝置](audio-endpoint-devices.md) 。</span><span class="sxs-lookup"><span data-stu-id="74ba4-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="74ba4-108">由於舊版音訊 Api 介面的固有限制，應用程式可以透過這些介面存取音訊端點裝置的部分功能，而不是所有的功能。</span><span class="sxs-lookup"><span data-stu-id="74ba4-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="74ba4-109">下列各節說明透過核心音訊 Api 直接存取音訊端點裝置的其他功能，以增強現有應用程式的技術。</span><span class="sxs-lookup"><span data-stu-id="74ba4-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="74ba4-110">這些增強功能通常只需要對現有應用程式程式碼進行輕微的變更。</span><span class="sxs-lookup"><span data-stu-id="74ba4-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="74ba4-111">下列各節說明如何將核心音訊 Api 的功能併入使用舊版音訊 Api 的現有應用程式：</span><span class="sxs-lookup"><span data-stu-id="74ba4-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="74ba4-112">DirectSound 應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="74ba4-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="74ba4-113">DirectShow 應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="74ba4-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="74ba4-114">舊版 Windows 多媒體應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="74ba4-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="74ba4-115">舊版音訊應用程式的音訊事件</span><span class="sxs-lookup"><span data-stu-id="74ba4-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="74ba4-116">舊版音訊應用程式的通知聲音</span><span class="sxs-lookup"><span data-stu-id="74ba4-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="74ba4-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="74ba4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74ba4-118">裝置角色</span><span class="sxs-lookup"><span data-stu-id="74ba4-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



