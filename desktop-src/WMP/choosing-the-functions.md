---
title: 選擇函數
description: 選擇函數
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player 行動外觀、音訊函式
- 適用于音訊的外觀、功能
- 建立面板、音訊功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372543"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="4e84c-106">選擇函數</span><span class="sxs-lookup"><span data-stu-id="4e84c-106">Choosing the Functions</span></span>

<span data-ttu-id="4e84c-107">此外觀的目的是要提供播放音訊的基本功能。</span><span class="sxs-lookup"><span data-stu-id="4e84c-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="4e84c-108">將會使用下列函數：</span><span class="sxs-lookup"><span data-stu-id="4e84c-108">The following functions will be used:</span></span>



| <span data-ttu-id="4e84c-109">函式</span><span class="sxs-lookup"><span data-stu-id="4e84c-109">Function</span></span>                     | <span data-ttu-id="4e84c-110">描述</span><span class="sxs-lookup"><span data-stu-id="4e84c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e84c-111">PlayPause 或 PlayPauseStop\*</span><span class="sxs-lookup"><span data-stu-id="4e84c-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="4e84c-112">啟動媒體專案的重要性很重要。</span><span class="sxs-lookup"><span data-stu-id="4e84c-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="4e84c-113">如果您要建立 Windows Media Player 10 行動裝置版或更新版本的面板，則應該使用 PlayPauseStop。</span><span class="sxs-lookup"><span data-stu-id="4e84c-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="4e84c-114">如果您使用的是舊版 Windows Media Player 行動裝置版，則必須使用 PlayPause。</span><span class="sxs-lookup"><span data-stu-id="4e84c-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="4e84c-115">這兩個函式可讓您新增暫停的功能，但只有在無法使用暫停功能時，才可使用 PlayPauseStop 來停止即時廣播。</span><span class="sxs-lookup"><span data-stu-id="4e84c-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="4e84c-116">停止</span><span class="sxs-lookup"><span data-stu-id="4e84c-116">Stop</span></span>                         | <span data-ttu-id="4e84c-117">您會想要新增停止以停止播放專案。</span><span class="sxs-lookup"><span data-stu-id="4e84c-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="4e84c-118">如果您要為 Windows Media Player 10 行動裝置版或更新版本建立面板，PlayPauseStop 函式已提供此功能。</span><span class="sxs-lookup"><span data-stu-id="4e84c-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4e84c-119">下一個</span><span class="sxs-lookup"><span data-stu-id="4e84c-119">Next</span></span>                         | <span data-ttu-id="4e84c-120">如果您有播放清單，您會想要能夠選擇下一個專案。</span><span class="sxs-lookup"><span data-stu-id="4e84c-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="4e84c-121">您需要這項程式才能進行數位媒體的基本導覽。</span><span class="sxs-lookup"><span data-stu-id="4e84c-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4e84c-122">上一頁</span><span class="sxs-lookup"><span data-stu-id="4e84c-122">Prev</span></span>                         | <span data-ttu-id="4e84c-123">雖然您可以使用 [下一步] 迴圈播放播放清單，直到您開始進行為止，新增 [上一步] 可讓使用者在流覽播放清單時，可以更輕鬆地回溯和向前移動。</span><span class="sxs-lookup"><span data-stu-id="4e84c-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="4e84c-124">VolumeUp 或 VolumeDown\*</span><span class="sxs-lookup"><span data-stu-id="4e84c-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="4e84c-125">您會想要提供使用者開啟或關閉磁片區的能力。</span><span class="sxs-lookup"><span data-stu-id="4e84c-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="4e84c-126">\*適用于 Windows Media Player 10 行動裝置版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4e84c-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e84c-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e84c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e84c-128">**外觀指南**</span><span class="sxs-lookup"><span data-stu-id="4e84c-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




