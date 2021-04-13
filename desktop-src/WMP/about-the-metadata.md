---
title: 關於中繼資料
description: 關於中繼資料
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player，中繼資料
- 中繼資料，關於
- 中繼資料，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300139"
---
# <a name="about-the-metadata"></a><span data-ttu-id="0d191-106">關於中繼資料</span><span class="sxs-lookup"><span data-stu-id="0d191-106">About the Metadata</span></span>

<span data-ttu-id="0d191-107">Windows Media Player 10 或更新版本會嘗試同步處理下列中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="0d191-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="0d191-108">Player 屬性</span><span class="sxs-lookup"><span data-stu-id="0d191-108">Player attribute</span></span> | <span data-ttu-id="0d191-109">WMDM 全域常數</span><span class="sxs-lookup"><span data-stu-id="0d191-109">WMDM global constant</span></span>  | <span data-ttu-id="0d191-110">Description</span><span class="sxs-lookup"><span data-stu-id="0d191-110">Description</span></span>                                                                                                 | <span data-ttu-id="0d191-111">所需的版本</span><span class="sxs-lookup"><span data-stu-id="0d191-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="0d191-112">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="0d191-112">AlbumArtist</span></span>      | <span data-ttu-id="0d191-113">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="0d191-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="0d191-114">以 Null 終止的 **字串** ，其中包含專輯之主要演出者的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d191-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="0d191-115">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-116">專輯</span><span class="sxs-lookup"><span data-stu-id="0d191-116">Album</span></span>            | <span data-ttu-id="0d191-117">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="0d191-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="0d191-118">以 Null 終止的 **字串** ，其中包含最初發行內容的專輯標題。</span><span class="sxs-lookup"><span data-stu-id="0d191-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="0d191-119">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-120">作者</span><span class="sxs-lookup"><span data-stu-id="0d191-120">Author</span></span>           | <span data-ttu-id="0d191-121">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="0d191-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="0d191-122">以 Null 終止的 **字串** ，包含與內容相關聯之媒體演出者或動作專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d191-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="0d191-123">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-124">BuyNow</span><span class="sxs-lookup"><span data-stu-id="0d191-124">BuyNow</span></span>           | <span data-ttu-id="0d191-125">g \_ wszWMDMBuyNow</span><span class="sxs-lookup"><span data-stu-id="0d191-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="0d191-126">指出使用者是否已選擇購買內容的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="0d191-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="0d191-127">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="0d191-128">WM/內容類型</span><span class="sxs-lookup"><span data-stu-id="0d191-128">WM/Genre</span></span>         | <span data-ttu-id="0d191-129">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="0d191-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="0d191-130">以 Null 終止的 **字串** ，其中包含內容的內容類型。</span><span class="sxs-lookup"><span data-stu-id="0d191-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="0d191-131">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-132">UserPlayCount</span><span class="sxs-lookup"><span data-stu-id="0d191-132">UserPlayCount</span></span>    | <span data-ttu-id="0d191-133">g \_ wszWMDMPlayCount</span><span class="sxs-lookup"><span data-stu-id="0d191-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="0d191-134">**DWORD** ，包含使用者播放數位媒體檔案的次數。</span><span class="sxs-lookup"><span data-stu-id="0d191-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="0d191-135">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="0d191-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="0d191-136">ReleaseDate</span></span>      | <span data-ttu-id="0d191-137">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="0d191-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="0d191-138">專案原始版本的日期。</span><span class="sxs-lookup"><span data-stu-id="0d191-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="0d191-139">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-140">標題</span><span class="sxs-lookup"><span data-stu-id="0d191-140">Title</span></span>            | <span data-ttu-id="0d191-141">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="0d191-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="0d191-142">包含標題的以 Null 結尾的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="0d191-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="0d191-143">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-144">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="0d191-144">WM/TrackNumber</span></span>   | <span data-ttu-id="0d191-145">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="0d191-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="0d191-146">**DWORD** ，其中包含原始釋出的專輯上專案的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="0d191-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="0d191-147">Windows Media Player 11 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0d191-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="0d191-148">UserRating</span></span>       | <span data-ttu-id="0d191-149">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="0d191-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="0d191-150">**DWORD** 包含值，表示使用者為數字媒體檔案指定的星級評等。</span><span class="sxs-lookup"><span data-stu-id="0d191-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="0d191-151">Windows Media Player 10 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0d191-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0d191-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d191-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d191-153">**加速中繼資料傳輸的裝置擴充功能**</span><span class="sxs-lookup"><span data-stu-id="0d191-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




