---
description: 使用影片
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: '使用影片 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320467"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="6e9d6-103">使用影片 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="6e9d6-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="6e9d6-104">雖然個別的視頻編碼器有自己的特性，但全都使用相同的基本程式。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="6e9d6-105">本節說明如何使用 Windows Media 視訊編解碼器來編碼和解碼影片，並解決各項功能的特定功能。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="6e9d6-106">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-106">This section contains the following topics.</span></span>



| <span data-ttu-id="6e9d6-107">主題</span><span class="sxs-lookup"><span data-stu-id="6e9d6-107">Topic</span></span>                                                                                                        | <span data-ttu-id="6e9d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="6e9d6-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e9d6-109">選擇影片編解碼器</span><span class="sxs-lookup"><span data-stu-id="6e9d6-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="6e9d6-110">描述最適合用於每個 Windows Media 視訊編解碼器之壓縮的內容類型。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="6e9d6-111">設定影片編碼</span><span class="sxs-lookup"><span data-stu-id="6e9d6-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="6e9d6-112">說明如何設定影片編碼器 DMOs。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="6e9d6-113">設定影片解碼</span><span class="sxs-lookup"><span data-stu-id="6e9d6-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="6e9d6-114">說明如何設定影片解碼 DMOs。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="6e9d6-115">強制插入主要畫面格</span><span class="sxs-lookup"><span data-stu-id="6e9d6-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="6e9d6-116">描述如何要求將範例編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="6e9d6-117">交錯式影片編碼</span><span class="sxs-lookup"><span data-stu-id="6e9d6-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="6e9d6-118">描述如何在 Windows Media 視訊資料流程中維持交錯。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="6e9d6-119">使用 Windows Media 視訊 9 Advanced Profile 編解碼器</span><span class="sxs-lookup"><span data-stu-id="6e9d6-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="6e9d6-120">說明如何使用 Windows Media 視訊 9 Advanced Profile 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="6e9d6-121">使用 Windows Media 視訊9螢幕編解碼器</span><span class="sxs-lookup"><span data-stu-id="6e9d6-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="6e9d6-122">說明如何使用 Windows Media 視訊9螢幕編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="6e9d6-123">使用 Windows Media 視訊9.1 映射編解碼器</span><span class="sxs-lookup"><span data-stu-id="6e9d6-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="6e9d6-124">說明如何使用 Windows Media 視訊9.1 映射編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6e9d6-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="6e9d6-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e9d6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e9d6-126">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="6e9d6-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



