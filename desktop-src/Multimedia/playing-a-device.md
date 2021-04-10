---
title: 播放裝置
description: 播放裝置
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY 命令
- MCIAVI 播放視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933238"
---
# <a name="playing-a-device"></a><span data-ttu-id="6a582-105">播放裝置</span><span class="sxs-lookup"><span data-stu-id="6a582-105">Playing a Device</span></span>

<span data-ttu-id="6a582-106">[**Play**](play.md) ([**MCI \_ play**](mci-play.md)) 命令會開始播放裝置。</span><span class="sxs-lookup"><span data-stu-id="6a582-106">The [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) command starts playing a device.</span></span> <span data-ttu-id="6a582-107">如果沒有任何旗標，此命令會從目前的位置開始播放並播放，直到命令中斷或到達媒體或檔案的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="6a582-107">Without any flags, this command starts playing from the current position and plays until the command is interrupted or until the end of the media or file is reached.</span></span> <span data-ttu-id="6a582-108">播放之後，目前的位置是在媒體的結尾。</span><span class="sxs-lookup"><span data-stu-id="6a582-108">After playback, the current position is at the end of the media.</span></span> <span data-ttu-id="6a582-109">您也可以使用 [**搜尋**](seek.md) ([**MCI \_ 搜尋**](mci-seek.md)) 命令來變更目前的位置。</span><span class="sxs-lookup"><span data-stu-id="6a582-109">You can also use the [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)) command to change the current position.</span></span>

<span data-ttu-id="6a582-110">大部分支援 **play** 命令的裝置也都支援 \_ 從)  (mci，以及將 (MCI 傳送 \_ 至) 旗標。</span><span class="sxs-lookup"><span data-stu-id="6a582-110">Most devices that support the **play** command also support the "from" (MCI\_FROM) and "to" (MCI\_TO) flags.</span></span> <span data-ttu-id="6a582-111">這些旗標會指出裝置應該開始和停止播放的位置。</span><span class="sxs-lookup"><span data-stu-id="6a582-111">These flags indicate the position at which the device should start and stop playing.</span></span> <span data-ttu-id="6a582-112">例如，下列命令會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式，從第一個播放軌的開頭播放 CD 音訊光碟：</span><span class="sxs-lookup"><span data-stu-id="6a582-112">For example, the following command plays a CD audio disc from the beginning of the first track using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="6a582-113">某些裝置類型會擴充此命令，以利用特定裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="6a582-113">Some device types extend this command to exploit the capabilities of a particular device.</span></span> <span data-ttu-id="6a582-114">例如， **videodisc** 裝置類型的 [**play**](play.md)命令包含「快速」 (MCI \_ VD \_ \_ 快速) 、「慢」 (mci \_ VD \_ 播放 \_ 慢) 和「掃描」 (mci \_ VD \_ play \_ 掃描) 旗標。</span><span class="sxs-lookup"><span data-stu-id="6a582-114">For example, the [**play**](play.md) command for the **videodisc** device type includes the "fast" (MCI\_VD\_PLAY\_FAST) , "slow" (MCI\_VD\_PLAY\_SLOW), and "scan" (MCI\_VD\_PLAY\_SCAN) flags.</span></span>

> [!Note]  
> <span data-ttu-id="6a582-115">指派給位置值的單位取決於裝置所使用的時間格式。</span><span class="sxs-lookup"><span data-stu-id="6a582-115">The units assigned to the position value depend on the time format used by the device.</span></span> <span data-ttu-id="6a582-116">每個裝置都有預設的時間格式，但您應該先使用 [**set**](set.md) ([**MCI \_ set**](mci-set.md)) 命令來指定時間格式，然後再發出使用位置值的任何命令。</span><span class="sxs-lookup"><span data-stu-id="6a582-116">Each device has a default time format, but you should specify the time format by using the [**set**](set.md) ([**MCI\_SET**](mci-set.md)) command before issuing any commands that use position values.</span></span>

 

## <a name="playing-an-avi-file"></a><span data-ttu-id="6a582-117">播放 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="6a582-117">Playing an AVI File</span></span>

<span data-ttu-id="6a582-118">Windows 中的影片檔案是由至少兩個交錯資料流程所組成：影片 (圖形) 串流和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="6a582-118">Video files in Windows are made up of at least two interleaved data streams: a video (pictorial) stream and an audio stream.</span></span> <span data-ttu-id="6a582-119">您可以使用 MCI 命令輕鬆地播放這些 (AVI) 檔案的音訊影片。</span><span class="sxs-lookup"><span data-stu-id="6a582-119">You can easily play these audio-video interleaved (AVI) files by using MCI commands.</span></span> <span data-ttu-id="6a582-120">下列各節討論如何播放 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="6a582-120">The following sections discuss playing AVI files.</span></span>

## <a name="setting-up-an-mciavi-playback-window"></a><span data-ttu-id="6a582-121">設定 MCIAVI 播放視窗</span><span class="sxs-lookup"><span data-stu-id="6a582-121">Setting Up an MCIAVI Playback Window</span></span>

<span data-ttu-id="6a582-122">您的應用程式可以指定下列選項，以定義播放 AVI 檔案的播放視窗：</span><span class="sxs-lookup"><span data-stu-id="6a582-122">Your application can specify the following options to define the playback window for playing an AVI file:</span></span>

-   <span data-ttu-id="6a582-123">使用 MCIAVI 驅動程式的預設快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-123">Use the MCIAVI driver's default pop-up window.</span></span>
-   <span data-ttu-id="6a582-124">指定可供 MCIAVI 驅動程式用來建立播放視窗的父視窗和視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="6a582-124">Specify a parent window and window style that the MCIAVI driver can use to create the playback window.</span></span>
-   <span data-ttu-id="6a582-125">指定 MCIAVI 驅動程式用來播放的播放視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-125">Specify a playback window for the MCIAVI driver to use for playback.</span></span>
-   <span data-ttu-id="6a582-126">在全螢幕顯示上播放 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="6a582-126">Play the AVI file on a full-screen display.</span></span>

<span data-ttu-id="6a582-127">如果您的應用程式未指定任何視窗選項，MCIAVI 驅動程式會建立播放順序的預設視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-127">If your application does not specify any window options, the MCIAVI driver creates a default window for playing the sequence.</span></span> <span data-ttu-id="6a582-128">驅動程式會針對 [**開啟**](open.md) 的 ([**MCI \_ open**](mci-open.md)) 命令建立此播放視窗，但在您的應用程式傳送命令以顯示視窗或播放檔案之前，不會顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-128">The driver creates this playback window for the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command, but it does not display the window until your application sends a command to either display the window or play the file.</span></span> <span data-ttu-id="6a582-129">此預設播放視窗是一個快顯視窗，具有調整大小框線、標題列、寬框架、 **視窗** 功能表及最小化按鈕。</span><span class="sxs-lookup"><span data-stu-id="6a582-129">This default playback window is a pop-up window with a sizing border, title bar, a thick frame, a **window** menu, and a Minimize button.</span></span>

<span data-ttu-id="6a582-130">當您的應用程式發出 **open** 命令時，也可以指定父視窗控制碼和視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="6a582-130">Your application can also specify a parent window handle and a window style when it issues the **open** command.</span></span> <span data-ttu-id="6a582-131">在此情況下，MCIAVI 驅動程式會根據這些規格（而不是預設的快顯視窗）來建立視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-131">In this case, the MCIAVI driver creates a window based on these specifications instead of the default pop-up window.</span></span> <span data-ttu-id="6a582-132">您的應用程式可以指定適用于 [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數的任何視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="6a582-132">Your application can specify any window style available for the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="6a582-133">需要父視窗的樣式（例如 WS 子系 \_ ）應該包含父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="6a582-133">Styles that require a parent window, such as WS\_CHILD, should include a parent window handle.</span></span>

<span data-ttu-id="6a582-134">您的應用程式也可以建立自己的視窗，並使用 [**window**](window.md) ([**MCI \_ 視窗**](mci-window.md)) 命令，提供 MCIAVI 驅動程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6a582-134">Your application can also create its own window and supply the handle to the MCIAVI driver by using the [**window**](window.md) ([**MCI\_WINDOW**](mci-window.md)) command.</span></span> <span data-ttu-id="6a582-135">MCIAVI 驅動程式會使用這個視窗，而不是建立它自己的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6a582-135">The MCIAVI driver uses this window instead of creating one of its own.</span></span>

<span data-ttu-id="6a582-136">當 MCIAVI 驅動程式建立播放視窗，或從您的應用程式取得視窗控制碼時，在您的應用程式播放序列或傳送命令以顯示視窗之前，不會顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="6a582-136">When the MCIAVI driver creates the playback window or obtains a window handle from your application, it does not display the window until your application either plays the sequence or sends a command to display the window.</span></span> <span data-ttu-id="6a582-137">您的應用程式可以使用 [ **視窗]** 命令來顯示視窗，而不播放順序。</span><span class="sxs-lookup"><span data-stu-id="6a582-137">Your application can use the **window** command to display the window without playing the sequence.</span></span> <span data-ttu-id="6a582-138">例如，下列命令會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85))來顯示視窗：</span><span class="sxs-lookup"><span data-stu-id="6a582-138">For example, the following command displays the window using [**mciSendString**](/previous-versions//dd757161(v=vs.85)):</span></span>


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="6a582-139">在此範例中，「電影」是數位視訊裝置的別名。</span><span class="sxs-lookup"><span data-stu-id="6a582-139">In this example, "movie" is an alias for the digital-video device.</span></span>

<span data-ttu-id="6a582-140">您的應用程式也可以全螢幕播放 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="6a582-140">Your application can also play an AVI file full-screen.</span></span> <span data-ttu-id="6a582-141">若要播放全螢幕，請使用 [](play.md) 「全螢幕」 (mci MCIAVI play 全螢幕) 旗標來修改 Play ([**MCI \_ play**](mci-play.md)) 命令 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6a582-141">To play full-screen, modify the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) command with the "fullscreen" (MCI\_MCIAVI\_PLAY\_FULLSCREEN) flag.</span></span> <span data-ttu-id="6a582-142">當您的應用程式使用這個旗標時，MCIAVI 驅動程式會使用 320 x 240 圖元的全螢幕格式來播放序列。</span><span class="sxs-lookup"><span data-stu-id="6a582-142">When your application uses this flag, the MCIAVI driver uses a 320- by 240-pixel full-screen format for playing the sequence.</span></span> <span data-ttu-id="6a582-143">例如，下列命令會使用 "movie" 作為別名) 來播放開啟的檔案全螢幕 (：</span><span class="sxs-lookup"><span data-stu-id="6a582-143">For example, the following command plays the opened file full-screen (using "movie" as an alias):</span></span>


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a><span data-ttu-id="6a582-144">變更 AVI 檔案的播放狀態</span><span class="sxs-lookup"><span data-stu-id="6a582-144">Changing the Playback State for an AVI file</span></span>

<span data-ttu-id="6a582-145">您的應用程式可以使用 [**搜尋**](seek.md) ([**MCI \_ 搜尋**](mci-seek.md)) 命令將目前位置移至 AVI 檔案中的開頭、結尾或任意位置。</span><span class="sxs-lookup"><span data-stu-id="6a582-145">Your application can use the [**seek**](seek.md) ([**MCI\_SEEK**](mci-seek.md)) command to move the current position to the beginning, the end, or an arbitrary position in an AVI file.</span></span> <span data-ttu-id="6a582-146">MCIAVI 驅動程式有兩種搜尋模式：精確且不精確。</span><span class="sxs-lookup"><span data-stu-id="6a582-146">There are two seek modes for the MCIAVI driver: exact and inexact.</span></span> <span data-ttu-id="6a582-147">您的應用程式可以使用 [**set**](set.md) ([**MCI \_ set**](mci-set.md)) 命令來變更搜尋模式。</span><span class="sxs-lookup"><span data-stu-id="6a582-147">Your application can change the seek mode by using the [**set**](set.md) ([**MCI\_SET**](mci-set.md)) command.</span></span> <span data-ttu-id="6a582-148">當您使用 **set** 「精確搜尋」時，MCIAVI 驅動程式會精確搜尋您應用程式所指定的框架。</span><span class="sxs-lookup"><span data-stu-id="6a582-148">When you use **set** "seek exactly on", the MCIAVI driver seeks exactly to the frame your application specifies.</span></span> <span data-ttu-id="6a582-149">如果檔案暫時壓縮，而您的應用程式未指定主要畫面格，這可能會造成延遲。</span><span class="sxs-lookup"><span data-stu-id="6a582-149">This might cause a delay if the file is temporally compressed and your application does not specify a key frame.</span></span> <span data-ttu-id="6a582-150">當您使用 **set** "seek off" 時，MCIAVI 驅動程式會搜尋暫時壓縮檔案中最接近的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="6a582-150">When you use **set** "seek exactly off", the MCIAVI driver seeks to the nearest key frame in a temporally compressed file.</span></span>

<span data-ttu-id="6a582-151">有些 MCI 命令可讓您的應用程式以其他方式改變 AVI 檔案的播放。</span><span class="sxs-lookup"><span data-stu-id="6a582-151">Some MCI commands let your application alter the playback of an AVI file in other ways.</span></span> <span data-ttu-id="6a582-152">例如，AVI 檔案預設會以正常速度播放，但您的應用程式可以使用「速度」旗標搭配 **set** 命令來增加或減少此速度。</span><span class="sxs-lookup"><span data-stu-id="6a582-152">For example, an AVI file, by default, plays at its normal speed, but your application can increase or decrease this speed by using the "speed" flag with the **set** command.</span></span> <span data-ttu-id="6a582-153">若是 AVI 檔案，通常會有1000的速度值。</span><span class="sxs-lookup"><span data-stu-id="6a582-153">For AVI files, a speed value of 1000 is typical.</span></span> <span data-ttu-id="6a582-154">因此，若要以一半的一般速度播放電影，您的應用程式可以使用命令 **集** 「movie 速度500」;或者，它可以使用 **設定** 的 "movie speed 2000"，以其正常速度的兩倍播放序列。</span><span class="sxs-lookup"><span data-stu-id="6a582-154">Thus, to play a movie at half its typical speed, your application can use the command **set** "movie speed 500"; alternatively, it can use **set** "movie speed 2000" to play the sequence at twice its normal speed.</span></span>

<span data-ttu-id="6a582-155">[**Setaudio**](setaudio.md) ([**MCI \_ setaudio**](mci-setaudio.md)) 命令可讓您的應用程式控制 AVI 檔案的音訊部分。</span><span class="sxs-lookup"><span data-stu-id="6a582-155">The [**setaudio**](setaudio.md) ([**MCI\_SETAUDIO**](mci-setaudio.md)) command lets your application control the audio portion of an AVI file.</span></span> <span data-ttu-id="6a582-156">您的應用程式可以在播放期間將音訊靜音，或者，如果有多個音訊串流檔案，請選取播放的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="6a582-156">Your application can mute audio during playback or, in the case of multiple audio stream files, select the audio stream that is played.</span></span>

<span data-ttu-id="6a582-157">MCIAVI 驅動程式具有對話方塊，可控制其一些播放選項。</span><span class="sxs-lookup"><span data-stu-id="6a582-157">The MCIAVI driver has a dialog box to control some of its playback options.</span></span> <span data-ttu-id="6a582-158">使用者可用的一些選項包括選取視窗導向或全螢幕播放、選取搜尋模式，以及縮放影像。</span><span class="sxs-lookup"><span data-stu-id="6a582-158">Some of the options available to the user include selecting window-oriented or full-screen playback, selecting the seek mode, and zooming the image.</span></span> <span data-ttu-id="6a582-159">您的應用程式可以使用 [ [**設定**](configure.md) ([**MCI \_ 設定**](mci-configure.md)) ] 命令，以 MCIAVI 顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="6a582-159">Your application can have MCIAVI display this dialog box by using the [**configure**](configure.md) ([**MCI\_CONFIGURE**](mci-configure.md)) command.</span></span>

## <a name="stream-handlers"></a><span data-ttu-id="6a582-160">串流處理常式</span><span class="sxs-lookup"><span data-stu-id="6a582-160">Stream Handlers</span></span>

<span data-ttu-id="6a582-161">AVI 檔案中的資料會被視為一連串的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6a582-161">The data in an AVI file is treated as a series of streams.</span></span> <span data-ttu-id="6a582-162">AVI 檔案通常包含音訊和影片串流，也可能有包含文字或某些其他自訂資料的自訂資料流程。</span><span class="sxs-lookup"><span data-stu-id="6a582-162">An AVI file typically contains an audio and video stream, and there might also be a custom stream that contains text or some other custom data.</span></span> <span data-ttu-id="6a582-163">MCIAVI 驅動程式可以針對這些資料流程使用不同的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6a582-163">The MCIAVI driver can use different handlers for these data streams.</span></span> <span data-ttu-id="6a582-164">如需自訂 AVI 檔案的詳細資訊，請參閱 [自訂檔案和資料流程處理常式](custom-file-and-stream-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="6a582-164">For more information about custom AVI files, see [Custom File and Stream Handlers](custom-file-and-stream-handlers.md).</span></span>

 

 