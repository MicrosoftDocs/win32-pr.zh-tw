---
title: OpenState
description: OpenState 屬性會抓取值，指出內容來源的狀態。
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- OpenState Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986168"
---
# <a name="playeropenstate"></a><span data-ttu-id="3651c-104">OpenState</span><span class="sxs-lookup"><span data-stu-id="3651c-104">Player.openState</span></span>

<span data-ttu-id="3651c-105">**OpenState** 屬性會抓取值，指出內容來源的狀態。</span><span class="sxs-lookup"><span data-stu-id="3651c-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="3651c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3651c-106">Syntax</span></span>

<span data-ttu-id="3651c-107">*玩家* 。**openState**</span><span class="sxs-lookup"><span data-stu-id="3651c-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3651c-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="3651c-108">Possible Values</span></span>

<span data-ttu-id="3651c-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="3651c-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="3651c-110">C 樣式的列舉常數可以藉由在 state 值前面加上 "wmpos" 來衍生。</span><span class="sxs-lookup"><span data-stu-id="3651c-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="3651c-111">例如，PlaylistOpening 狀態的常數為 **wmposPlaylistOpening**。</span><span class="sxs-lookup"><span data-stu-id="3651c-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="3651c-112">值</span><span class="sxs-lookup"><span data-stu-id="3651c-112">Value</span></span> | <span data-ttu-id="3651c-113">州</span><span class="sxs-lookup"><span data-stu-id="3651c-113">State</span></span>                   | <span data-ttu-id="3651c-114">描述</span><span class="sxs-lookup"><span data-stu-id="3651c-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3651c-115">0</span><span class="sxs-lookup"><span data-stu-id="3651c-115">0</span></span>     | <span data-ttu-id="3651c-116">未定義</span><span class="sxs-lookup"><span data-stu-id="3651c-116">Undefined</span></span>               | <span data-ttu-id="3651c-117">Windows Media Player 處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="3651c-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="3651c-118">1</span><span class="sxs-lookup"><span data-stu-id="3651c-118">1</span></span>     | <span data-ttu-id="3651c-119">PlaylistChanging</span><span class="sxs-lookup"><span data-stu-id="3651c-119">PlaylistChanging</span></span>        | <span data-ttu-id="3651c-120">即將載入新的播放清單。</span><span class="sxs-lookup"><span data-stu-id="3651c-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="3651c-121">2</span><span class="sxs-lookup"><span data-stu-id="3651c-121">2</span></span>     | <span data-ttu-id="3651c-122">PlaylistLocating</span><span class="sxs-lookup"><span data-stu-id="3651c-122">PlaylistLocating</span></span>        | <span data-ttu-id="3651c-123">Windows Media Player 正在嘗試找出播放清單。</span><span class="sxs-lookup"><span data-stu-id="3651c-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="3651c-124">播放清單可以是本機 (程式庫，或副檔名為 .asx 的中繼檔) 或遠端。</span><span class="sxs-lookup"><span data-stu-id="3651c-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="3651c-125">3</span><span class="sxs-lookup"><span data-stu-id="3651c-125">3</span></span>     | <span data-ttu-id="3651c-126">PlaylistConnecting</span><span class="sxs-lookup"><span data-stu-id="3651c-126">PlaylistConnecting</span></span>      | <span data-ttu-id="3651c-127">連接到播放清單。</span><span class="sxs-lookup"><span data-stu-id="3651c-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="3651c-128">4</span><span class="sxs-lookup"><span data-stu-id="3651c-128">4</span></span>     | <span data-ttu-id="3651c-129">PlaylistLoading</span><span class="sxs-lookup"><span data-stu-id="3651c-129">PlaylistLoading</span></span>         | <span data-ttu-id="3651c-130">已找到播放清單，現在正在進行取出。</span><span class="sxs-lookup"><span data-stu-id="3651c-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="3651c-131">5</span><span class="sxs-lookup"><span data-stu-id="3651c-131">5</span></span>     | <span data-ttu-id="3651c-132">PlaylistOpening</span><span class="sxs-lookup"><span data-stu-id="3651c-132">PlaylistOpening</span></span>         | <span data-ttu-id="3651c-133">播放清單已被取出，現在正在進行剖析和載入。</span><span class="sxs-lookup"><span data-stu-id="3651c-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="3651c-134">6</span><span class="sxs-lookup"><span data-stu-id="3651c-134">6</span></span>     | <span data-ttu-id="3651c-135">PlaylistOpenNoMedia</span><span class="sxs-lookup"><span data-stu-id="3651c-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="3651c-136">播放清單已開啟。</span><span class="sxs-lookup"><span data-stu-id="3651c-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="3651c-137">7</span><span class="sxs-lookup"><span data-stu-id="3651c-137">7</span></span>     | <span data-ttu-id="3651c-138">PlaylistChanged</span><span class="sxs-lookup"><span data-stu-id="3651c-138">PlaylistChanged</span></span>         | <span data-ttu-id="3651c-139">已將新的播放清單指派給 **currentPlaylist**。</span><span class="sxs-lookup"><span data-stu-id="3651c-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="3651c-140">8</span><span class="sxs-lookup"><span data-stu-id="3651c-140">8</span></span>     | <span data-ttu-id="3651c-141">MediaChanging</span><span class="sxs-lookup"><span data-stu-id="3651c-141">MediaChanging</span></span>           | <span data-ttu-id="3651c-142">即將載入新的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="3651c-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="3651c-143">9</span><span class="sxs-lookup"><span data-stu-id="3651c-143">9</span></span>     | <span data-ttu-id="3651c-144">MediaLocating</span><span class="sxs-lookup"><span data-stu-id="3651c-144">MediaLocating</span></span>           | <span data-ttu-id="3651c-145">Windows Media Player 正在尋找媒體專案。</span><span class="sxs-lookup"><span data-stu-id="3651c-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="3651c-146">檔案可以是本機或遠端。</span><span class="sxs-lookup"><span data-stu-id="3651c-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="3651c-147">10</span><span class="sxs-lookup"><span data-stu-id="3651c-147">10</span></span>    | <span data-ttu-id="3651c-148">MediaConnecting</span><span class="sxs-lookup"><span data-stu-id="3651c-148">MediaConnecting</span></span>         | <span data-ttu-id="3651c-149">連接到保存媒體專案的伺服器。</span><span class="sxs-lookup"><span data-stu-id="3651c-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="3651c-150">11</span><span class="sxs-lookup"><span data-stu-id="3651c-150">11</span></span>    | <span data-ttu-id="3651c-151">MediaLoading</span><span class="sxs-lookup"><span data-stu-id="3651c-151">MediaLoading</span></span>            | <span data-ttu-id="3651c-152">媒體專案已存在，現在正在進行取出。</span><span class="sxs-lookup"><span data-stu-id="3651c-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="3651c-153">12</span><span class="sxs-lookup"><span data-stu-id="3651c-153">12</span></span>    | <span data-ttu-id="3651c-154">MediaOpening</span><span class="sxs-lookup"><span data-stu-id="3651c-154">MediaOpening</span></span>            | <span data-ttu-id="3651c-155">媒體專案已被取出，現在正在開啟。</span><span class="sxs-lookup"><span data-stu-id="3651c-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="3651c-156">13</span><span class="sxs-lookup"><span data-stu-id="3651c-156">13</span></span>    | <span data-ttu-id="3651c-157">MediaOpen</span><span class="sxs-lookup"><span data-stu-id="3651c-157">MediaOpen</span></span>               | <span data-ttu-id="3651c-158">媒體專案現在已開啟。</span><span class="sxs-lookup"><span data-stu-id="3651c-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="3651c-159">14</span><span class="sxs-lookup"><span data-stu-id="3651c-159">14</span></span>    | <span data-ttu-id="3651c-160">BeginCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="3651c-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="3651c-161">正在開始取得編解碼器。</span><span class="sxs-lookup"><span data-stu-id="3651c-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="3651c-162">15</span><span class="sxs-lookup"><span data-stu-id="3651c-162">15</span></span>    | <span data-ttu-id="3651c-163">EndCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="3651c-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="3651c-164">編解碼器取得已完成。</span><span class="sxs-lookup"><span data-stu-id="3651c-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="3651c-165">16</span><span class="sxs-lookup"><span data-stu-id="3651c-165">16</span></span>    | <span data-ttu-id="3651c-166">BeginLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="3651c-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="3651c-167">取得用來播放受 DRM 保護內容的授權。</span><span class="sxs-lookup"><span data-stu-id="3651c-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="3651c-168">17</span><span class="sxs-lookup"><span data-stu-id="3651c-168">17</span></span>    | <span data-ttu-id="3651c-169">EndLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="3651c-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="3651c-170">已取得播放受 DRM 保護內容的授權。</span><span class="sxs-lookup"><span data-stu-id="3651c-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="3651c-171">18</span><span class="sxs-lookup"><span data-stu-id="3651c-171">18</span></span>    | <span data-ttu-id="3651c-172">BeginIndividualization</span><span class="sxs-lookup"><span data-stu-id="3651c-172">BeginIndividualization</span></span>  | <span data-ttu-id="3651c-173">開始 DRM 的個人化。</span><span class="sxs-lookup"><span data-stu-id="3651c-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="3651c-174">19</span><span class="sxs-lookup"><span data-stu-id="3651c-174">19</span></span>    | <span data-ttu-id="3651c-175">EndIndividualization</span><span class="sxs-lookup"><span data-stu-id="3651c-175">EndIndividualization</span></span>    | <span data-ttu-id="3651c-176">已完成 DRM 的個人化。</span><span class="sxs-lookup"><span data-stu-id="3651c-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="3651c-177">20</span><span class="sxs-lookup"><span data-stu-id="3651c-177">20</span></span>    | <span data-ttu-id="3651c-178">MediaWaiting</span><span class="sxs-lookup"><span data-stu-id="3651c-178">MediaWaiting</span></span>            | <span data-ttu-id="3651c-179">正在等候媒體專案。</span><span class="sxs-lookup"><span data-stu-id="3651c-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="3651c-180">21</span><span class="sxs-lookup"><span data-stu-id="3651c-180">21</span></span>    | <span data-ttu-id="3651c-181">OpeningUnknownURL</span><span class="sxs-lookup"><span data-stu-id="3651c-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="3651c-182">開啟具有未知類型的 URL。</span><span class="sxs-lookup"><span data-stu-id="3651c-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3651c-183">備註</span><span class="sxs-lookup"><span data-stu-id="3651c-183">Remarks</span></span>

<span data-ttu-id="3651c-184">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="3651c-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="3651c-185">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="3651c-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="3651c-186">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3651c-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3651c-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="3651c-187">Requirements</span></span>



| <span data-ttu-id="3651c-188">需求</span><span class="sxs-lookup"><span data-stu-id="3651c-188">Requirement</span></span> | <span data-ttu-id="3651c-189">值</span><span class="sxs-lookup"><span data-stu-id="3651c-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3651c-190">版本</span><span class="sxs-lookup"><span data-stu-id="3651c-190">Version</span></span><br/> | <span data-ttu-id="3651c-191">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3651c-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3651c-192">DLL</span><span class="sxs-lookup"><span data-stu-id="3651c-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="3651c-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3651c-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3651c-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3651c-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3651c-195">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="3651c-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="3651c-196">**OpenStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="3651c-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





