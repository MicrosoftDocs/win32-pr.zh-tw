---
title: 關於 MCIWnd 視窗類別
description: 關於 MCIWnd 視窗類別
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- MCIWnd 視窗類別，關於
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e459a0e7d93543af126287a776b64130595ad11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372233"
---
# <a name="about-the-mciwnd-window-class"></a><span data-ttu-id="fdd7c-105">關於 MCIWnd 視窗類別</span><span class="sxs-lookup"><span data-stu-id="fdd7c-105">About the MCIWnd Window Class</span></span>

<span data-ttu-id="fdd7c-106">MCIWnd 視窗類別很容易使用。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-106">The MCIWnd Window class is easy to use.</span></span> <span data-ttu-id="fdd7c-107">藉由使用單一函式， [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 您的應用程式可以建立一個控制項，來播放任何使用 media control 介面 (MCI) 的裝置。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-107">By using a single function, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) your application can create a control that plays any device that uses the media control interface (MCI).</span></span> <span data-ttu-id="fdd7c-108">這些裝置包括 CD 音訊、波形音訊、MIDI 和影片裝置。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-108">These devices include CD audio, waveform-audio, MIDI, and video devices.</span></span>

<span data-ttu-id="fdd7c-109">自動化播放也是快速又簡單的。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-109">Automating playback is also quick and easy.</span></span> <span data-ttu-id="fdd7c-110">只要使用一個函式和兩個宏，應用程式就可以建立具有適當媒體裝置的 MCIWnd 視窗、播放裝置，並在內容完成播放時關閉裝置和視窗。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-110">Using only one function and two macros, an application can create an MCIWnd window with the appropriate media device, play the device, and close both the device and the window when the content has finished playing.</span></span>

> [!Note]  
> <span data-ttu-id="fdd7c-111">有些裝置會播放儲存在檔案中的內容。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-111">Some devices play content that is stored in files.</span></span> <span data-ttu-id="fdd7c-112">其他裝置，例如 CD 音訊裝置，則會播放儲存在另一個媒體中的內容。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-112">Other devices, such as CD audio devices, play content that is stored in another medium.</span></span> <span data-ttu-id="fdd7c-113">為了清楚起見，此總覽將這兩種情況都稱為「播放裝置」。</span><span class="sxs-lookup"><span data-stu-id="fdd7c-113">For purposes of clarity, this overview refers to both circumstances as "playing the device."</span></span>

 

 

 




