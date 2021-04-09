---
description: 重要事項已淘汰。
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: MFPlayer2 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848447"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="0f22d-103">MFPlayer2 範例</span><span class="sxs-lookup"><span data-stu-id="0f22d-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f22d-104">已取代。</span><span class="sxs-lookup"><span data-stu-id="0f22d-104">Deprecated.</span></span> <span data-ttu-id="0f22d-105">此 API 可能會從 Windows 的未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="0f22d-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="0f22d-106">應用程式應該使用 [媒體會話](media-session.md) 來播放。</span><span class="sxs-lookup"><span data-stu-id="0f22d-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="0f22d-107">示範 [SimplePlay](simpleplay-sample.md) 範例中省略的一些播放功能，例如：</span><span class="sxs-lookup"><span data-stu-id="0f22d-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="0f22d-108">尋求</span><span class="sxs-lookup"><span data-stu-id="0f22d-108">Seeking</span></span>
-   <span data-ttu-id="0f22d-109">速率控制 (向前快轉和倒轉) </span><span class="sxs-lookup"><span data-stu-id="0f22d-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="0f22d-110">音訊音量和靜音控制項</span><span class="sxs-lookup"><span data-stu-id="0f22d-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="0f22d-111">影片縮放</span><span class="sxs-lookup"><span data-stu-id="0f22d-111">Video zoom</span></span>

<span data-ttu-id="0f22d-112">下圖顯示這些功能所使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="0f22d-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="0f22d-113">mfplayer 範例的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="0f22d-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="0f22d-114">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="0f22d-114">APIs Demonstrated</span></span>

<span data-ttu-id="0f22d-115">此範例示範下列 Api。</span><span class="sxs-lookup"><span data-stu-id="0f22d-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="0f22d-116">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="0f22d-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="0f22d-117">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="0f22d-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="0f22d-118">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="0f22d-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="0f22d-119">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="0f22d-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="0f22d-120">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="0f22d-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="0f22d-121">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="0f22d-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="0f22d-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="0f22d-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="0f22d-123">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="0f22d-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="0f22d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f22d-124">Requirements</span></span>



| <span data-ttu-id="0f22d-125">產品</span><span class="sxs-lookup"><span data-stu-id="0f22d-125">Product</span></span>                                                        | <span data-ttu-id="0f22d-126">版本</span><span class="sxs-lookup"><span data-stu-id="0f22d-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0f22d-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0f22d-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0f22d-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f22d-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0f22d-129">下載範例</span><span class="sxs-lookup"><span data-stu-id="0f22d-129">Downloading the Sample</span></span>

<span data-ttu-id="0f22d-130">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)中取得。</span><span class="sxs-lookup"><span data-stu-id="0f22d-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f22d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="0f22d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f22d-132">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="0f22d-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0f22d-133">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="0f22d-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
