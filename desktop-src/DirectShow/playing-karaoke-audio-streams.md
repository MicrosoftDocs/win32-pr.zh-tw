---
description: 播放卡拉卡拉的音訊串流
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: 播放卡拉卡拉的音訊串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973745"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="fe4ba-103">播放卡拉卡拉的音訊串流</span><span class="sxs-lookup"><span data-stu-id="fe4ba-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="fe4ba-104">DVD 導覽器可以播放具有卡拉卡拉 DVD-Video 光碟的視頻串流，但卡拉 ok 播放也需要支援多重通道卡拉器混合的解碼器。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="fe4ba-105">具體而言，解碼器必須支援 [**DVD 卡拉 Ok 屬性集**](dvd-karaoke-property-set.md) (AM \_ 屬性 \_ DVDKARAOKE) 。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="fe4ba-106">卡拉 ok 光碟是一種 DVD-Video 光碟，具有相同的導覽結構。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="fe4ba-107">歌曲通常會格式化為標題，且標題可根據執行者、音樂樣式或其他準則分組為標題組。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="fe4ba-108">「卡拉」和「其他」 DVD-Videos 類型的主要差異在於音訊串流。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="fe4ba-109">卡拉卡拉的所有磁片都包含多頻道音訊，通常是杜比 AC-3。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="fe4ba-110">頻道0和1永遠包含背景的對音樂，而頻道2到5則各自都包含了節目表人聲、指南 melodies 和音效效果的任何組合。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="fe4ba-111">卡拉卡拉（卡拉）應用程式可以控制每個輔助通道的音量和目的地喇叭。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="fe4ba-112">當 DVD 導覽器偵測到光碟上的卡拉 ok 內容，並進入 [卡拉 ok] 模式時，它會通知該解碼器，然後將前三個通道的上方靜音 (輔助通道) ，直到應用程式明確開啟任何或所有通道為止。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="fe4ba-113">「卡拉卡拉」應用程式的基本工作是：</span><span class="sxs-lookup"><span data-stu-id="fe4ba-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="fe4ba-114">使用 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法來判斷輔助通道的數目及其內容。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="fe4ba-115">提供可顯示通道內容的使用者介面，並可讓使用者隨時使用 [**IDvdControl2：： SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode)來開啟或關閉任何輔助通道。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="fe4ba-116">這些步驟會在 **GetAudioAttributes** 方法的 DVDCore .cpp 中的 DVD 範例應用程式中說明。</span><span class="sxs-lookup"><span data-stu-id="fe4ba-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe4ba-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe4ba-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4ba-118">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="fe4ba-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



