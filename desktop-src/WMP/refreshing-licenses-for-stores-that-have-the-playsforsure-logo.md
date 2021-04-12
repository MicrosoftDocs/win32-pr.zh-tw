---
title: 重新整理具有 PlaysForSure 標誌之商店的授權
description: 重新整理具有 PlaysForSure 標誌之商店的授權
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player 線上商店，重新整理授權
- 線上商店、授權重新整理
- Windows Media Player 線上商店、授權重新整理
- 線上商店，重新整理授權
- Windows Media Player 線上商店，PlaysForSure 標誌
- 線上商店，PlaysForSure 標誌
- 重新整理授權
- 授權，重新整理
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092556"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="19e61-112">重新整理具有 PlaysForSure 標誌之商店的授權</span><span class="sxs-lookup"><span data-stu-id="19e61-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="19e61-113">某些線上音樂商店具有 PlaysForSure 標誌，但未與 Windows Media Player 11 整合。</span><span class="sxs-lookup"><span data-stu-id="19e61-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="19e61-114">這些存放區必須提供 ServiceInfo 檔和輕量元件，讓 Windows Media Player 11 可以取得並更新其內容的授權。</span><span class="sxs-lookup"><span data-stu-id="19e61-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="19e61-115">下列範例說明授權更新程式的運作方式。</span><span class="sxs-lookup"><span data-stu-id="19e61-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="19e61-116">使用者從 Proseware online store 取得50音樂曲目。</span><span class="sxs-lookup"><span data-stu-id="19e61-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="19e61-117">每個曲目都是副檔名為 .wma 的檔案。</span><span class="sxs-lookup"><span data-stu-id="19e61-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="19e61-118">除了曲目之外，使用者還會取得用來播放曲目的授權。</span><span class="sxs-lookup"><span data-stu-id="19e61-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="19e61-119">使用者將50軌複製到已安裝 Windows Media Player 11 的新電腦，並將這些曲目新增至 Windows Media Player 程式庫。</span><span class="sxs-lookup"><span data-stu-id="19e61-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="19e61-120">在稍後的時間，授權重新整理模組 (LRM) （Windows Media Player 11 的一部分）會檢查50追蹤中的中繼資料，並判斷 Proseware 是否為內容提供者。</span><span class="sxs-lookup"><span data-stu-id="19e61-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="19e61-121">Windows Media Player 可以藉由檢查媒體檔案中的 **ContentDistributor** 屬性來識別內容提供者。</span><span class="sxs-lookup"><span data-stu-id="19e61-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="19e61-122">如果有 PlaysForSure 標誌的線上商店提供的媒體檔案使用 Windows Media 數位 Rights Management (WMDRM) ，線上商店必須將 **ContentDistributor** 屬性放置在媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="19e61-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="19e61-123">如需詳細資訊，請參閱 Windows Media Player SDK 中的新增內容散發者屬性。</span><span class="sxs-lookup"><span data-stu-id="19e61-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="19e61-124">LRM 會查閱 Proseware 的 ServiceInfo 檔的 URL、下載檔案，以及檢查檔的 **Install** 元素，以取得 LRM 可用於安裝 Proseware 元件的封裝 url。</span><span class="sxs-lookup"><span data-stu-id="19e61-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="19e61-125">LRM 會安裝並載入元件。</span><span class="sxs-lookup"><span data-stu-id="19e61-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="19e61-126">針對每個50曲目，LRM 會呼叫 Proseware 元件的 [IWMPSubscriptionService：： allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) 方法。</span><span class="sxs-lookup"><span data-stu-id="19e61-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="19e61-127">**AllowPlay** 方法會在新電腦上放置個別曲目的授權，並在 *pfAllowPlay* 參數中傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="19e61-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="19e61-128">Proseware 元件必須提供播放個別播放軌所需的所有授權。也就是說，元件必須提供根授權和分葉授權（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="19e61-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="19e61-129">在第一次呼叫 **allowPlay** 方法時，Proseware 元件必須顯示對話方塊，以確認目前的使用者具有 Proseware 帳戶，且具有播放播放軌的許可權。在後續呼叫 **allowPlay** 時，元件可以使用第一次呼叫中取得的認證，確認使用者有權播放其餘的曲目。</span><span class="sxs-lookup"><span data-stu-id="19e61-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="19e61-130">線上商店所撰寫的元件必須執行 **IWMPSubscriptionService** 介面的 **allowPlay** 方法。</span><span class="sxs-lookup"><span data-stu-id="19e61-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="19e61-131">元件必須 \_ 從其他三個方法傳回 E >notimpl： **allowCDBurn**、 **allowPDATransfer** 和 **startBackgroundProcessing**。</span><span class="sxs-lookup"><span data-stu-id="19e61-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="19e61-132">此外，元件還必須將 **功能** 登錄專案的值設為 1;也就是說， \_ \_ 必須設定訂用帳戶端點 ALLOWPLAY 功能旗標，且必須清除所有其他功能旗標。</span><span class="sxs-lookup"><span data-stu-id="19e61-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="19e61-133">如需註冊元件的詳細資訊，請參閱 [類型2線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-2-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="19e61-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="19e61-134">如需建立可執行 **IWMPSubscriptionService** 介面之元件的詳細資訊，請參閱 [建立類型2線上商店的外掛程式](building-the-plug-in-for-a-type-2-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="19e61-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="19e61-135">如需提供 Microsoft ServiceInfo 檔的相關資訊，請將電子郵件傳送給 Windows Media Player 的虛擬服務小組。</span><span class="sxs-lookup"><span data-stu-id="19e61-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="19e61-136">小組的電子郵件地址為 mpsvctm@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="19e61-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="19e61-137">如需使用各種 Windows Media Sdk 來建立提供授權數位媒體內容的服務的技術指引，請前往 [Microsoft Windows Media 開發人員中心](https://msdn.microsoft.com/windowsmedia/default.aspx) ，並搜尋「建立 Windows Media Player 10 訂閱線上商店」。</span><span class="sxs-lookup"><span data-stu-id="19e61-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="19e61-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="19e61-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19e61-139">**ServiceInfo 檔**</span><span class="sxs-lookup"><span data-stu-id="19e61-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="19e61-140">**Windows Media Player 線上商店**</span><span class="sxs-lookup"><span data-stu-id="19e61-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




