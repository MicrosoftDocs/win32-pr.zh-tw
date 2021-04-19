---
title: 記錄
description: 記錄
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- MCI_RECORD 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965561"
---
# <a name="recording"></a><span data-ttu-id="d12bf-104">記錄</span><span class="sxs-lookup"><span data-stu-id="d12bf-104">Recording</span></span>

<span data-ttu-id="d12bf-105">一般 MCI 規格支援錄製數位影片、MIDI sequencer、視頻/磁帶錄製器 (VCR) 和波形音訊裝置;不過，只有波形音訊和 VCR 裝置目前會執行錄製功能。</span><span class="sxs-lookup"><span data-stu-id="d12bf-105">The general MCI specification supports recording with digital-video, MIDI sequencer, video-cassette recorder (VCR), and waveform-audio devices; however, only waveform-audio and VCR devices currently implement recording capabilities.</span></span> <span data-ttu-id="d12bf-106">您可以將記錄的資訊插入或覆寫到現有的檔案或記錄到新的檔案中。</span><span class="sxs-lookup"><span data-stu-id="d12bf-106">You can insert or overwrite recorded information into an existing file or record into a new file.</span></span> <span data-ttu-id="d12bf-107">若要記錄到現有的檔案，請像平常一樣開啟波形音訊裝置和檔案。</span><span class="sxs-lookup"><span data-stu-id="d12bf-107">To record to an existing file, open a waveform-audio device and file as you would normally.</span></span> <span data-ttu-id="d12bf-108">若要記錄到新的檔案，當您開啟裝置時，如果您使用命令字串介面，請指定 "new" 作為裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="d12bf-108">To record into a new file, when you open the device specify "new" as the device name if you are using the command-string interface.</span></span> <span data-ttu-id="d12bf-109">如果您使用命令訊息介面，請指定長度為零的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d12bf-109">If you are using the command-message interface, specify a zero-length filename.</span></span>

<span data-ttu-id="d12bf-110">當 MCI 建立要錄製的新檔案時，資料格式會設定為設備磁碟機所指定的預設格式。</span><span class="sxs-lookup"><span data-stu-id="d12bf-110">When MCI creates a new file for recording, the data format is set to a default format specified by the device driver.</span></span> <span data-ttu-id="d12bf-111">若要使用預設格式以外的格式，您可以使用 [**set**](set.md) ([**MCI \_ set**](mci-set.md)) 命令。</span><span class="sxs-lookup"><span data-stu-id="d12bf-111">To use a format other than the default format, you can use the [**set**](set.md) ([**MCI\_SET**](mci-set.md)) command.</span></span>

<span data-ttu-id="d12bf-112">若要開始錄製，請使用 [**記錄**](record.md) 命令 (或 [**mci \_ 記錄**](mci-record.md) ，以及) 的 [**mci \_ 記錄 \_ PARMS**](mci-record-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d12bf-112">To begin recording, use the [**record**](record.md) command (or [**MCI\_RECORD**](mci-record.md) and the [**MCI\_RECORD\_PARMS**](mci-record-parms.md) structure).</span></span>

<span data-ttu-id="d12bf-113">如果您以插入模式記錄到現有的檔案，您可以使用) 的 "from" (MCI \_ 和 "to" (mci \_ 來) **記錄** 命令的旗標，以指定錄製的開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="d12bf-113">If you record in insert mode to an existing file, you can use the "from" (MCI\_FROM) and "to" (MCI\_TO) flags of the **record** command to specify starting and ending positions for recording.</span></span> <span data-ttu-id="d12bf-114">例如，如果您記錄至長度為20秒的檔案，而且您在5秒內開始錄製，並于10秒結束錄製，則產生的檔案會是25秒的時間。</span><span class="sxs-lookup"><span data-stu-id="d12bf-114">For example, if you record to a file that is 20 seconds long, and you begin recording at 5 seconds and end recording at 10 seconds, the resulting file will be 25 seconds long.</span></span> <span data-ttu-id="d12bf-115">檔案將會有5秒的區段插入原始錄製的5秒。</span><span class="sxs-lookup"><span data-stu-id="d12bf-115">The file will have a 5-second segment inserted 5 seconds into the original recording.</span></span>

<span data-ttu-id="d12bf-116">如果您以覆寫模式錄製至現有的檔案，您可以使用 "from" 和 "to" 旗標來指定覆寫之區段的開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="d12bf-116">If you record with overwrite mode to an existing file, you can use the "from" and "to" flags to specify starting and ending locations of the section that is overwritten.</span></span> <span data-ttu-id="d12bf-117">例如，如果您記錄至長度為20秒的檔案，並在5秒內開始記錄，並在10秒後結束記錄，則您的記錄仍會有20秒的時間，但從5秒開始並以10秒結束的區段將會被取代。</span><span class="sxs-lookup"><span data-stu-id="d12bf-117">For example, if you record to a file that is 20 seconds long, and you begin recording at 5 seconds and end recording at 10 seconds, you still have a recording 20 seconds long, but the section beginning at 5 seconds and ending at 10 seconds will have been replaced.</span></span>

<span data-ttu-id="d12bf-118">如果您未指定結束位置，記錄會繼續進行，直到您傳送 [**stop**](stop.md) ([**MCI \_ stop**](mci-stop.md)) 命令，或直到驅動程式可用磁碟空間不足為止。</span><span class="sxs-lookup"><span data-stu-id="d12bf-118">If you do not specify an ending location, recording continues until you send a [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command, or until the driver runs out of free disk space.</span></span> <span data-ttu-id="d12bf-119">如果您錄製至新的檔案，您可以省略 "from" 旗標，或將它設為零以開始在新檔案的開頭錄製。</span><span class="sxs-lookup"><span data-stu-id="d12bf-119">If you record to a new file, you can omit the "from" flag or set it to zero to start recording at the beginning of a new file.</span></span> <span data-ttu-id="d12bf-120">您可以指定在錄製至新檔案時終止錄製的結束位置。</span><span class="sxs-lookup"><span data-stu-id="d12bf-120">You can specify an ending location to terminate recording when recording to a new file.</span></span>

<span data-ttu-id="d12bf-121">[**記錄**](record.md)命令有時候會精確地在啟動位置的1秒內，例如使用 VCR 裝置。</span><span class="sxs-lookup"><span data-stu-id="d12bf-121">The [**record**](record.md) command is sometimes accurate to within only 1 second of the starting location, such as with VCR devices.</span></span> <span data-ttu-id="d12bf-122">若要更精確地記錄，您應該使用 [**提示**](cue.md) ([**MCI \_ 提示**](mci-cue.md)) 命令。</span><span class="sxs-lookup"><span data-stu-id="d12bf-122">To record more accurately, you should use the [**cue**](cue.md) ([**MCI\_CUE**](mci-cue.md)) command.</span></span> <span data-ttu-id="d12bf-123">數位影片、VCR 和波形音訊裝置可辨識此命令。</span><span class="sxs-lookup"><span data-stu-id="d12bf-123">This command is recognized by digital-video, VCR, and waveform-audio devices.</span></span> <span data-ttu-id="d12bf-124">如需使用 VCR 裝置錄製的詳細資訊，請參閱 [Vcr 服務](vcr-services.md)。</span><span class="sxs-lookup"><span data-stu-id="d12bf-124">For more information about recording with VCR devices, see [VCR Services](vcr-services.md).</span></span>

## <a name="saving-a-recorded-file"></a><span data-ttu-id="d12bf-125">儲存錄製的檔案</span><span class="sxs-lookup"><span data-stu-id="d12bf-125">Saving a Recorded File</span></span>

<span data-ttu-id="d12bf-126">錄製完成時，請使用 [ [**儲存**](save.md) ] 命令 (或 [**mci \_ 儲存**](mci-save.md) ，然後在關閉裝置之前儲存記錄檔，然後再) 儲存 [**\_ \_ PARMS**](mci-save-parms.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="d12bf-126">When recording is complete, use the [**save**](save.md) command (or [**MCI\_SAVE**](mci-save.md) and the [**MCI\_SAVE\_PARMS**](mci-save-parms.md) structure) to save the recording before closing the device.</span></span>

> [!Note]  
> <span data-ttu-id="d12bf-127">如果您在未儲存的情況下關閉裝置，則會遺失記錄的資料。</span><span class="sxs-lookup"><span data-stu-id="d12bf-127">If you close the device without saving, the recorded data is lost.</span></span>

 

## <a name="checking-input-levels-pcm-only"></a><span data-ttu-id="d12bf-128">只 (PCM 檢查輸入層級) </span><span class="sxs-lookup"><span data-stu-id="d12bf-128">Checking Input Levels (PCM Only)</span></span>

<span data-ttu-id="d12bf-129">若要先取得輸入信號的層級，然後在 PCM 上錄製 (脈衝程式碼調製) 波形音訊輸入裝置，請使用 [**狀態**](status.md) ([**MCI \_ 狀態**](mci-status.md)) 命令。</span><span class="sxs-lookup"><span data-stu-id="d12bf-129">To get the level of the input signal before recording on a PCM (Pulse Code Modulation) waveform-audio input device, use the [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)) command.</span></span> <span data-ttu-id="d12bf-130">指定「等級」旗標 (或 MCI \_ 狀態 \_ 專案旗標，並將 [**mci \_ 狀態 \_ PARMS**](mci-status-parms.md)結構的 **dwItem** 成員設定為) 的 mci \_ WAVE \_ 狀態 \_ 層級。</span><span class="sxs-lookup"><span data-stu-id="d12bf-130">Specify the "level" flag (or the MCI\_STATUS\_ITEM flag and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_WAVE\_STATUS\_LEVEL).</span></span> <span data-ttu-id="d12bf-131">傳回平均輸入信號等級。</span><span class="sxs-lookup"><span data-stu-id="d12bf-131">The average input signal level is returned.</span></span> <span data-ttu-id="d12bf-132">左聲道值是在高序位字組中，而右或 mono 通道值是在低序位字組中。</span><span class="sxs-lookup"><span data-stu-id="d12bf-132">The left-channel value is in the high-order word and the right- or mono-channel value is in the low-order word.</span></span>

<span data-ttu-id="d12bf-133">輸入層級會以不帶正負號的值表示。</span><span class="sxs-lookup"><span data-stu-id="d12bf-133">The input level is represented as an unsigned value.</span></span> <span data-ttu-id="d12bf-134">若為8位範例，此值的範圍介於0到 127 (0x7F) 。</span><span class="sxs-lookup"><span data-stu-id="d12bf-134">For 8-bit samples, this value is in the range 0 through 127 (0x7F).</span></span> <span data-ttu-id="d12bf-135">在16位範例中，它的範圍是0到 32767 (0x7FFF) 。</span><span class="sxs-lookup"><span data-stu-id="d12bf-135">For 16-bit samples, it is in the range 0 through 32,767 (0x7FFF).</span></span>

 

 




