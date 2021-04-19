---
description: 串流處理是指只在記憶體中維護一小部分的播放音訊檔案。 如此一來，就可以播放大型音訊檔案（例如背景音樂），而不會佔用大量的記憶體。
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: XAudio2 串流音訊資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975478"
---
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="56149-104">XAudio2 串流音訊資料</span><span class="sxs-lookup"><span data-stu-id="56149-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="56149-105">串流處理是指只在記憶體中維護一小部分的播放音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="56149-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="56149-106">如此一來，就可以播放大型音訊檔案（例如背景音樂），而不會佔用大量的記憶體。</span><span class="sxs-lookup"><span data-stu-id="56149-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="56149-107">串流處理音訊檔案時，會以區塊的方式從磁片讀取其資料，而不是一次載入整個檔案。</span><span class="sxs-lookup"><span data-stu-id="56149-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="56149-108">串流處理是透過將音訊資料非同步地讀入磁碟緩衝區佇列來完成。</span><span class="sxs-lookup"><span data-stu-id="56149-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="56149-109">每個緩衝區都會填滿，然後提交至來源語音。</span><span class="sxs-lookup"><span data-stu-id="56149-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="56149-110">當語音完成播放緩衝區之後，緩衝區就會變成可供再次讀取。</span><span class="sxs-lookup"><span data-stu-id="56149-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="56149-111">以這種方式逐一查看磁碟緩衝區，可在只載入部分資料的時候播放大型音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="56149-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="56149-112">串流程式碼應該放在個別的執行緒中，在等待長時間執行的磁片和音訊作業完成時，它可以進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="56149-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="56149-113">回呼類別是用來在音訊作業完成時觸發事件，藉此喚醒執行緒。</span><span class="sxs-lookup"><span data-stu-id="56149-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="56149-114">如需如何使用 XAudio2 來完成串流處理的範例，請參閱 [如何：從磁片串流音效](how-to--stream-a-sound-from-disk.md)。</span><span class="sxs-lookup"><span data-stu-id="56149-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56149-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="56149-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56149-116">串流音訊資料</span><span class="sxs-lookup"><span data-stu-id="56149-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="56149-117">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="56149-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



