---
description: X3DAudio 是與 XAudio2 搭配使用的 API，可在3D 空間中放置音效，以從空間中的點（相對於相機的位置）建立音效的假像。
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: X3DAudio 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985134"
---
# <a name="x3daudio-overview"></a><span data-ttu-id="25dda-103">X3DAudio 總覽</span><span class="sxs-lookup"><span data-stu-id="25dda-103">X3DAudio Overview</span></span>

<span data-ttu-id="25dda-104">X3DAudio 是與 [XAudio2](programming-guide.md) 搭配使用的 API，可在3d 空間中放置音效，以從空間中的點（相對於相機的位置）建立音效的假像。尤其是，功能3D 場景的標題會想要使用 X3DAudio。</span><span class="sxs-lookup"><span data-stu-id="25dda-104">X3DAudio is an API used with [XAudio2](programming-guide.md) to position sound in 3D space to create the illusion of sound coming from a point in space relative to the position of the camera.In particular, titles that feature 3D scenes will want to use X3DAudio.</span></span> <span data-ttu-id="25dda-105">不需要3D 定位的音效（例如 soundtracks 或非定位的環境音效）可能會完全略過 X3DAudio。</span><span class="sxs-lookup"><span data-stu-id="25dda-105">Sounds not requiring 3D positioning, such as soundtracks or non-positioned ambient sounds, may bypass X3DAudio completely.</span></span>

## <a name="listeners-and-emitters"></a><span data-ttu-id="25dda-106">接聽程式和發射器</span><span class="sxs-lookup"><span data-stu-id="25dda-106">Listeners and Emitters</span></span>

<span data-ttu-id="25dda-107">為了管理3D 空間 *中的音效* ，X3DAudio 採用接聽程式和 *發射器* 的概念。</span><span class="sxs-lookup"><span data-stu-id="25dda-107">To manage sounds in 3D space, X3DAudio employs the concepts of *listeners* and *emitters*.</span></span> <span data-ttu-id="25dda-108">接聽程式和發射器代表任何發音為3D 音效的位置，以及這些音效源自的點。</span><span class="sxs-lookup"><span data-stu-id="25dda-108">Listeners and emitters represent the position of whatever is hearing 3D sounds, and the point from which those sounds originate.</span></span>

-   <span data-ttu-id="25dda-109">接聽程式會定義為空間和方向的點。</span><span class="sxs-lookup"><span data-stu-id="25dda-109">A listener is defined as a point in space and an orientation.</span></span> <span data-ttu-id="25dda-110">這是 *聽到* 音效的位置。</span><span class="sxs-lookup"><span data-stu-id="25dda-110">It is the position at which the sound is *heard*.</span></span> <span data-ttu-id="25dda-111">接聽程式的位置和方向通常與相機的位置和方向相同。</span><span class="sxs-lookup"><span data-stu-id="25dda-111">The position and orientation of the listener generally is the same as the position and orientation of the camera.</span></span> <span data-ttu-id="25dda-112">無論標題使用的是第一個人或協力廠商的觀點觀點，都是如此。</span><span class="sxs-lookup"><span data-stu-id="25dda-112">This is true whether a title uses a first-person or third-person perspective view.</span></span> <span data-ttu-id="25dda-113">接聽程式的位置是以全局座標表示。</span><span class="sxs-lookup"><span data-stu-id="25dda-113">The listener's position is expressed in world coordinates.</span></span> <span data-ttu-id="25dda-114">請務必注意，它是接聽程式 *相對* 于發射器的位置，可決定如何計算最終的喇叭磁片區。</span><span class="sxs-lookup"><span data-stu-id="25dda-114">It is important to note that it is the listener's position *relative* to an emitter that determines how to calculate the final speaker volumes.</span></span>
-   <span data-ttu-id="25dda-115">發射器定義為一個 (或多個) 點 *在音效來源* 的空間中。</span><span class="sxs-lookup"><span data-stu-id="25dda-115">An emitter is defined as one (or more) points in space from which a sound *originates*.</span></span> <span data-ttu-id="25dda-116">發射器的位置可以是3D 空間中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="25dda-116">The position of the emitter can be anywhere in 3D space.</span></span> <span data-ttu-id="25dda-117">如同接聽程式，發射器的位置是以全局座標表示。</span><span class="sxs-lookup"><span data-stu-id="25dda-117">Like a listener, an emitter's position is expressed in world coordinates.</span></span> <span data-ttu-id="25dda-118">它是 *相對* 于接聽程式的發射器位置，可決定最終的喇叭磁片區的計算方式。</span><span class="sxs-lookup"><span data-stu-id="25dda-118">It is the emitter's position *relative* to the listener that determines how the final speaker volumes are calculated.</span></span>
-   <span data-ttu-id="25dda-119">X3DAudio 使用左手型座標。</span><span class="sxs-lookup"><span data-stu-id="25dda-119">X3DAudio uses left-handed coordinates.</span></span> <span data-ttu-id="25dda-120">若要使用右手座標，開發人員必須將 X3DAUDIO 接聽程式 \_ 和 X3DAUDIO 發射器的 OrientTop、OrientFront、Position 和 Velocity 成員的 z 元素否定。 \_</span><span class="sxs-lookup"><span data-stu-id="25dda-120">To use with right-handed coordinates, developers need to negate the .z element of the OrientTop, OrientFront, Position, and Velocity members of X3DAUDIO\_LISTENER and X3DAUDIO\_EMITTER.</span></span>

<span data-ttu-id="25dda-121">除了位置，接聽程式和發射器也可以包含速度。</span><span class="sxs-lookup"><span data-stu-id="25dda-121">In addition to position, listeners and emitters can include velocity.</span></span> <span data-ttu-id="25dda-122">與3D 轉譯引擎不同的是，X3DAudio 只會使用速度計算 Doppler 效果 (不會用來計算位置) 。</span><span class="sxs-lookup"><span data-stu-id="25dda-122">Unlike a 3D rendering engine, X3DAudio only uses velocity to calculate Doppler effects (it is not used to calculate position).</span></span>

<span data-ttu-id="25dda-123">如需接聽程式和發射器的詳細資訊，請參閱 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構參考主題。</span><span class="sxs-lookup"><span data-stu-id="25dda-123">For more details about listeners and emitters, see the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure reference topics.</span></span>

## <a name="using-x3daudio-with-xaudio2"></a><span data-ttu-id="25dda-124">使用 X3DAudio 搭配 XAudio2</span><span class="sxs-lookup"><span data-stu-id="25dda-124">Using X3DAudio with XAudio2</span></span>

<span data-ttu-id="25dda-125">針對 X3DAudio 與 XAudio2 之間的所有互動，請使用下列 X3DAudio 函數。</span><span class="sxs-lookup"><span data-stu-id="25dda-125">For all interaction between X3DAudio and XAudio2, use the following X3DAudio functions.</span></span>

-   [<span data-ttu-id="25dda-126">**X3DAudioInitialize**</span><span class="sxs-lookup"><span data-stu-id="25dda-126">**X3DAudioInitialize**</span></span>](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    <span data-ttu-id="25dda-127">呼叫 [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) 函數來初始化 X3DAudio。</span><span class="sxs-lookup"><span data-stu-id="25dda-127">Call the [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function to initialize X3DAudio.</span></span> <span data-ttu-id="25dda-128">一般而言，您只需要在遊戲的存留期內呼叫 **X3DAudioInitialize** 一次，除非說話者設定有所變更。</span><span class="sxs-lookup"><span data-stu-id="25dda-128">Typically, you only need to call **X3DAudioInitialize** once in the lifetime of a game, unless the speaker configuration is changed.</span></span>

-   [<span data-ttu-id="25dda-129">**X3DAudioCalculate**</span><span class="sxs-lookup"><span data-stu-id="25dda-129">**X3DAudioCalculate**</span></span>](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    <span data-ttu-id="25dda-130">初始化 X3DAudio 之後，您可以將音效的發射器和接聽程式傳遞至 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) 函式，以判斷指定音效的音量和其他值。</span><span class="sxs-lookup"><span data-stu-id="25dda-130">After you initialize X3DAudio, you can determine volume and other values for a given sound by passing the sound's emitter and the listener to the [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) function.</span></span> <span data-ttu-id="25dda-131">然後，您可以針對傳遞給函式的旗標，將 **X3DAudioCalculate** 所計算的值套用至 XAudio2 聲音或效果。</span><span class="sxs-lookup"><span data-stu-id="25dda-131">The values calculated by **X3DAudioCalculate** can then be applied to XAudio2 voices or effects as appropriate for the flags passed to the function.</span></span> <span data-ttu-id="25dda-132">您可以使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 和 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 方法，將 X3DAudio 所計算的音量和音調值套用至語音。</span><span class="sxs-lookup"><span data-stu-id="25dda-132">You can apply volume and pitch values calculated by X3DAudio to a voice with the [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) methods.</span></span> <span data-ttu-id="25dda-133">使用 [**IXAudio2Voice：： SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)方法時，必須將 X3DAudio 所計算的其他值套用至「[**回音」效果**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)。</span><span class="sxs-lookup"><span data-stu-id="25dda-133">Other values calculated by X3DAudio will need to be applied to a [**reverb effect**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) using the [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) method.</span></span>

<span data-ttu-id="25dda-134">如需搭配使用 X3DAudio 與 XAudio2 的逐步範例，請參閱 how [to：整合 X3DAudio 與 XAudio](how-to--integrate-x3daudio-with-xaudio2.md)</span><span class="sxs-lookup"><span data-stu-id="25dda-134">For a step-by-step example of using X3DAudio with XAudio2, see [How to: Integrate X3DAudio with XAudio](how-to--integrate-x3daudio-with-xaudio2.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="25dda-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="25dda-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25dda-136">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="25dda-136">X3DAudio</span></span>](x3daudio.md)
</dt> </dl>

 

 
