---
title: 播放清單。資料行
description: Columns 屬性會定義出現在播放清單元素中的資料行。
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- 播放清單. 資料行 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976002"
---
# <a name="playlistcolumns"></a><span data-ttu-id="c9b33-104">播放清單。資料行</span><span class="sxs-lookup"><span data-stu-id="c9b33-104">PLAYLIST.columns</span></span>

<span data-ttu-id="c9b33-105">**Columns** 屬性會定義出現在 **播放清單** 元素中的資料行。</span><span class="sxs-lookup"><span data-stu-id="c9b33-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="c9b33-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c9b33-106">Possible Values</span></span>

<span data-ttu-id="c9b33-107">這個屬性是具有下列格式的讀取/寫入 **字串** ：</span><span class="sxs-lookup"><span data-stu-id="c9b33-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="c9b33-108">DB \_ 名稱 = 易記 \_ 名稱; 資料庫 \_ 名稱 = 易記 \_ 名稱;</span><span class="sxs-lookup"><span data-stu-id="c9b33-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="c9b33-109">易記 \_ 名稱是顯示在播放清單元素之資料行標頭中的值，而資料庫 \_ 名稱是下表中的值。</span><span class="sxs-lookup"><span data-stu-id="c9b33-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="c9b33-110">請注意，播放清單專案可能是來自媒體櫃或 CD 的媒體專案，也可能是由使用者建立或取自 CD 的另一個 **播放清單** 。</span><span class="sxs-lookup"><span data-stu-id="c9b33-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="c9b33-111">某些資料行只有在 [描述] 欄中指出的特定播放清單專案才有效。</span><span class="sxs-lookup"><span data-stu-id="c9b33-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="c9b33-112">值</span><span class="sxs-lookup"><span data-stu-id="c9b33-112">Value</span></span>             | <span data-ttu-id="c9b33-113">描述</span><span class="sxs-lookup"><span data-stu-id="c9b33-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b33-114">專輯</span><span class="sxs-lookup"><span data-stu-id="c9b33-114">Album</span></span>             | <span data-ttu-id="c9b33-115">專輯的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9b33-115">The name of the album.</span></span> <span data-ttu-id="c9b33-116">僅搭配媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="c9b33-117">演出者</span><span class="sxs-lookup"><span data-stu-id="c9b33-117">Artist</span></span>            | <span data-ttu-id="c9b33-118">演出者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9b33-118">The name of the artist.</span></span> <span data-ttu-id="c9b33-119">不適用於使用者建立的播放清單。</span><span class="sxs-lookup"><span data-stu-id="c9b33-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="c9b33-120">作者</span><span class="sxs-lookup"><span data-stu-id="c9b33-120">Author</span></span>            | <span data-ttu-id="c9b33-121">演出者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9b33-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="c9b33-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="c9b33-122">Bitrate</span></span>           | <span data-ttu-id="c9b33-123">內容的位元速率。</span><span class="sxs-lookup"><span data-stu-id="c9b33-123">The bit rate of the content.</span></span> <span data-ttu-id="c9b33-124">只能與媒體櫃中的媒體專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="c9b33-125">CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="c9b33-125">CDTrackEnabled</span></span>    | <span data-ttu-id="c9b33-126">指出是否已啟用 CD 曲目。</span><span class="sxs-lookup"><span data-stu-id="c9b33-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="c9b33-127">只能搭配 CD 媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="c9b33-128">已核取</span><span class="sxs-lookup"><span data-stu-id="c9b33-128">Checked</span></span>           | <span data-ttu-id="c9b33-129">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-130">著作權</span><span class="sxs-lookup"><span data-stu-id="c9b33-130">Copyright</span></span>         | <span data-ttu-id="c9b33-131">播放清單的著作權。</span><span class="sxs-lookup"><span data-stu-id="c9b33-131">The copyright of the playlist.</span></span> <span data-ttu-id="c9b33-132">未搭配 CD 播放清單或媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="c9b33-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="c9b33-133">CreationDate</span></span>      | <span data-ttu-id="c9b33-134">程式庫中專案的建立日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c9b33-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="c9b33-135">只能與程式庫中的專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="c9b33-136">DigitallySecure</span><span class="sxs-lookup"><span data-stu-id="c9b33-136">DigitallySecure</span></span>   | <span data-ttu-id="c9b33-137">指出專案是否以 Windows Media Rights Manager 保護。</span><span class="sxs-lookup"><span data-stu-id="c9b33-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="c9b33-138">只能與媒體櫃中的媒體專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="c9b33-139">持續時間</span><span class="sxs-lookup"><span data-stu-id="c9b33-139">Duration</span></span>          | <span data-ttu-id="c9b33-140">媒體專案的持續時間。</span><span class="sxs-lookup"><span data-stu-id="c9b33-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="c9b33-141">FileType</span><span class="sxs-lookup"><span data-stu-id="c9b33-141">FileType</span></span>          | <span data-ttu-id="c9b33-142">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-143">Genre</span><span class="sxs-lookup"><span data-stu-id="c9b33-143">Genre</span></span>             | <span data-ttu-id="c9b33-144">播放清單的類型。</span><span class="sxs-lookup"><span data-stu-id="c9b33-144">The genre of the playlist.</span></span> <span data-ttu-id="c9b33-145">不適用於 Cd 的播放清單。</span><span class="sxs-lookup"><span data-stu-id="c9b33-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="c9b33-146">MediaAttribute</span><span class="sxs-lookup"><span data-stu-id="c9b33-146">MediaAttribute</span></span>    | <span data-ttu-id="c9b33-147">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="c9b33-148">MediaType</span></span>         | <span data-ttu-id="c9b33-149">媒體專案的類型 (音訊或影片) 。</span><span class="sxs-lookup"><span data-stu-id="c9b33-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="c9b33-150">MetadataSource</span><span class="sxs-lookup"><span data-stu-id="c9b33-150">MetadataSource</span></span>    | <span data-ttu-id="c9b33-151">此 CD 軌的中繼資料來源 (AMG、WindowsMedia.com 等) 。</span><span class="sxs-lookup"><span data-stu-id="c9b33-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="c9b33-152">只能搭配 CD 媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="c9b33-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="c9b33-153">ModifiedBy</span></span>        | <span data-ttu-id="c9b33-154">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-155">Name</span><span class="sxs-lookup"><span data-stu-id="c9b33-155">Name</span></span>              | <span data-ttu-id="c9b33-156">播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9b33-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="c9b33-157">OriginalIndex</span><span class="sxs-lookup"><span data-stu-id="c9b33-157">OriginalIndex</span></span>     | <span data-ttu-id="c9b33-158">如果適用的話，則為對應的 CD 播放軌識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9b33-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="c9b33-159">只能搭配 CD 媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="c9b33-160">PlayCount</span><span class="sxs-lookup"><span data-stu-id="c9b33-160">PlayCount</span></span>         | <span data-ttu-id="c9b33-161">已播放內容到結尾的次數。</span><span class="sxs-lookup"><span data-stu-id="c9b33-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="c9b33-162">只能與媒體櫃中的媒體專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="c9b33-163">PlaylistAttribute</span><span class="sxs-lookup"><span data-stu-id="c9b33-163">PlaylistAttribute</span></span> | <span data-ttu-id="c9b33-164">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-165">分級</span><span class="sxs-lookup"><span data-stu-id="c9b33-165">Rating</span></span>            | <span data-ttu-id="c9b33-166">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="c9b33-167">SourceURL</span></span>         | <span data-ttu-id="c9b33-168">內容的路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="c9b33-168">The path or URL to the content.</span></span> <span data-ttu-id="c9b33-169">只能與媒體櫃中的媒體專案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="c9b33-170">狀態</span><span class="sxs-lookup"><span data-stu-id="c9b33-170">Status</span></span>            | <span data-ttu-id="c9b33-171">要複製之 CD 播放軌的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="c9b33-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="c9b33-172">只能搭配 CD 媒體專案使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="c9b33-173">樣式</span><span class="sxs-lookup"><span data-stu-id="c9b33-173">Style</span></span>             | <span data-ttu-id="c9b33-174">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c9b33-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="c9b33-175">目錄</span><span class="sxs-lookup"><span data-stu-id="c9b33-175">TOC</span></span>               | <span data-ttu-id="c9b33-176">如果適用的話，則為對應的 CD 目錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9b33-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="c9b33-177">不適用於使用者建立的播放清單。</span><span class="sxs-lookup"><span data-stu-id="c9b33-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="c9b33-178">備註</span><span class="sxs-lookup"><span data-stu-id="c9b33-178">Remarks</span></span>

<span data-ttu-id="c9b33-179">如果其中一個資料行不存在於文件庫中，則會保留空白。</span><span class="sxs-lookup"><span data-stu-id="c9b33-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="c9b33-180">最多可以指定31個數據行。</span><span class="sxs-lookup"><span data-stu-id="c9b33-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="c9b33-181">如果您指定重複的資料行，第一個資料行中的資料將會靠左對齊，但是所有其他重複的資料行都會靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="c9b33-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="c9b33-182">例如，如果您有兩個持續時間資料行，資料將會靠左對齊，並在第二個靠右對齊。</span><span class="sxs-lookup"><span data-stu-id="c9b33-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b33-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9b33-183">Requirements</span></span>



| <span data-ttu-id="c9b33-184">需求</span><span class="sxs-lookup"><span data-stu-id="c9b33-184">Requirement</span></span> | <span data-ttu-id="c9b33-185">值</span><span class="sxs-lookup"><span data-stu-id="c9b33-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c9b33-186">版本</span><span class="sxs-lookup"><span data-stu-id="c9b33-186">Version</span></span><br/> | <span data-ttu-id="c9b33-187">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c9b33-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9b33-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9b33-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b33-189">**播放清單元素**</span><span class="sxs-lookup"><span data-stu-id="c9b33-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="c9b33-190">**播放清單。 columnsVisible**</span><span class="sxs-lookup"><span data-stu-id="c9b33-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





