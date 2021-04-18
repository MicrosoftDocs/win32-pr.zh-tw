---
title: 關於播放清單同步處理
description: 關於播放清單同步處理
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player，播放清單同步處理
- Windows Media Player 物件模型，播放清單同步處理
- 物件模型，播放清單同步處理
- Windows Media Player ActiveX 控制項，播放清單同步處理
- ActiveX 控制項，播放清單同步處理
- Windows Media Player 行動 ActiveX 控制項、播放清單同步處理
- Windows Media Player 行動裝置、播放清單同步處理
- 同步處理裝置、播放清單
- 裝置同步處理，播放清單
- 播放清單，同步處理
- Windows Media 中繼檔播放清單，同步處理
- 中繼檔播放清單，同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314244"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="df038-115">關於播放清單同步處理</span><span class="sxs-lookup"><span data-stu-id="df038-115">About Playlist Synchronization</span></span>

<span data-ttu-id="df038-116">Windows Media Player 10 或更新版本是設計來使用播放清單同步處理模型，將數位媒體內容同步處理至裝置。</span><span class="sxs-lookup"><span data-stu-id="df038-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="df038-117">這表示預定要複製到裝置的內容必須是播放清單的一部分。</span><span class="sxs-lookup"><span data-stu-id="df038-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="df038-118">當使用者選擇將個人的數位媒體內容從電腦傳送到裝置時，Windows Media Player 會將內容新增至預設播放清單以供複製。</span><span class="sxs-lookup"><span data-stu-id="df038-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="df038-119">Windows Media Player 裝置同步處理 Api 的設計，也像這樣。</span><span class="sxs-lookup"><span data-stu-id="df038-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="df038-120">如同 Windows Media Player，您的程式可以向使用者顯示其定義的播放清單清單。</span><span class="sxs-lookup"><span data-stu-id="df038-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="df038-121">然後，您可以讓使用者選擇要與特定裝置同步處理的播放清單，並設定同步處理常式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="df038-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="df038-122">因為可攜式裝置的儲存容量有限，所以使用者可以選擇同步處理比裝置可儲存更多的數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="df038-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="df038-123">Windows Media Player 會以優先權順序同步處理內容。</span><span class="sxs-lookup"><span data-stu-id="df038-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="df038-124">使用者可以使用可從 [ **裝置** ] 功能存取的對話方塊來定義優先權順序。</span><span class="sxs-lookup"><span data-stu-id="df038-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="df038-125">若要回應使用者對您程式的輸入，您可以變更特定播放清單屬性的值，以程式設計方式變更優先順序順序。</span><span class="sxs-lookup"><span data-stu-id="df038-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="df038-126">這些屬性統稱為 *同步* 屬性。</span><span class="sxs-lookup"><span data-stu-id="df038-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="df038-127">媒體櫃中的每個播放清單都有16個同步處理屬性： **Sync01** 至 **Sync16**。</span><span class="sxs-lookup"><span data-stu-id="df038-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="df038-128">每個屬性都代表具有對應合作關係索引的裝置。</span><span class="sxs-lookup"><span data-stu-id="df038-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="df038-129">每個屬性的值會告訴您兩個事項：</span><span class="sxs-lookup"><span data-stu-id="df038-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="df038-130">是否應將播放清單與裝置同步處理。</span><span class="sxs-lookup"><span data-stu-id="df038-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="df038-131">播放清單的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="df038-131">The priority value for the playlist.</span></span>

<span data-ttu-id="df038-132">值為零表示 Windows Media Player 不應嘗試與裝置同步播放播放清單。</span><span class="sxs-lookup"><span data-stu-id="df038-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="df038-133">任何其他值都是優先順序號碼。</span><span class="sxs-lookup"><span data-stu-id="df038-133">Any other value is a priority number.</span></span> <span data-ttu-id="df038-134">較低的值在同步處理期間會獲得較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="df038-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="df038-135">播放清單也有 **>synconly** 屬性，指出播放清單是否僅適用于同步處理。</span><span class="sxs-lookup"><span data-stu-id="df038-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="df038-136">數位媒體內容的個別專案也包含同步處理的相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="df038-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="df038-137">當您從程式庫取出 **媒體** 物件時，您可以檢查 **SyncState** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="df038-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="df038-138">這個屬性會提供有關內容是否已成功複製到裝置的擴充資訊，或是因為無法容納內容而導致複製內容失敗的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="df038-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="df038-139">您應該避免提供使用者介面元素，讓使用者能夠從所有程式庫內容建立播放清單，以進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="df038-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="df038-140">為了優化效能，Windows Media Player 會強制執行一組規則來建立同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="df038-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="df038-141">您的程式應該只針對您提供的內容建立同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="df038-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="df038-142">允許 Windows Media Player 為使用者從其他來源新增至程式庫的內容建立同步播放清單。</span><span class="sxs-lookup"><span data-stu-id="df038-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="df038-143">除了建立您自己的播放清單使用者介面之外，您還可以使用預設對話方塊來顯示使用者，以選擇播放清單及管理裝置的合作關係。</span><span class="sxs-lookup"><span data-stu-id="df038-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="df038-144">若要這樣做，請呼叫 [IWMPSyncDevice：： showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings)。</span><span class="sxs-lookup"><span data-stu-id="df038-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="df038-145">當您叫用此方法時，Windows Media Player 會顯示它的 [同步處理設定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="df038-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="df038-146">當使用者關閉對話方塊時，Windows Media Player 會自動回到先前的停駐狀態，並將控制權傳遞回您的遠端程式。</span><span class="sxs-lookup"><span data-stu-id="df038-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df038-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="df038-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df038-148">**關於裝置同步處理**</span><span class="sxs-lookup"><span data-stu-id="df038-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="df038-149">**管理同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="df038-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="df038-150">**播放清單屬性**</span><span class="sxs-lookup"><span data-stu-id="df038-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




