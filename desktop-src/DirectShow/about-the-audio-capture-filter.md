---
description: 關於音訊捕獲篩選器
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: 關於音訊捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109688"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="25597-103">關於音訊捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="25597-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="25597-104">DirectShow 可透過 [音訊捕獲篩選器](audio-capture-filter.md)，從音效卡上的類比輸入進行捕捉。</span><span class="sxs-lookup"><span data-stu-id="25597-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="25597-105">此篩選器會使用 waveIn *XXX* api 來控制驅動程式支援這些 api 的任何裝置。</span><span class="sxs-lookup"><span data-stu-id="25597-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="25597-106">系統上的每張卡片都是由篩選準則的個別實例表示。</span><span class="sxs-lookup"><span data-stu-id="25597-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="25597-107">音訊捕獲篩選器會將卡片上的每個輸入（例如麥克風或 MIDI 輸入）公開為輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="25597-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="25597-108">輸入圖釘代表驅動程式公開為音訊來源行的內容。</span><span class="sxs-lookup"><span data-stu-id="25597-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="25597-109">但是，不會透過這些輸入釘傳送任何資料，也不會連接到其他的 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="25597-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="25597-110">它們只是提供一種方法讓應用程式控制輸入。</span><span class="sxs-lookup"><span data-stu-id="25597-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="25597-111">應用程式可以使用輸入 pin 來啟用或停用輸入，或設定混合的屬性，例如低音均衡、高音均衡、移動流覽等等。</span><span class="sxs-lookup"><span data-stu-id="25597-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="25597-112">可用的控制項數量取決於驅動程式。</span><span class="sxs-lookup"><span data-stu-id="25597-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="25597-113">若要完全瞭解並利用特定音效卡的功能，您將需要卡片製造商提供的檔。</span><span class="sxs-lookup"><span data-stu-id="25597-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="25597-114">您可以從 CD-Audio 的輸入進行捕捉，但這個音訊串流已經通過數位轉類比轉換器，所以會從原始 CD 中失去音效品質。</span><span class="sxs-lookup"><span data-stu-id="25597-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="25597-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="25597-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25597-116">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="25597-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



