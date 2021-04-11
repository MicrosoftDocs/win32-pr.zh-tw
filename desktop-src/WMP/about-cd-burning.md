---
title: 關於 CD 燒錄
description: 關於 CD 燒錄
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media Player 的行動 ActiveX 控制項、CD 燒錄
- Windows Media Player Mobile、CD 燒錄
- CD 燒錄，關於
- 燒錄 Cd，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103681546"
---
# <a name="about-cd-burning"></a><span data-ttu-id="bbfbe-112">關於 CD 燒錄</span><span class="sxs-lookup"><span data-stu-id="bbfbe-112">About CD Burning</span></span>

<span data-ttu-id="bbfbe-113">Windows Media Player 11 SDK 引進了建立 Cd 的新功能。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-113">The Windows Media Player 11 SDK introduces new functionality for creating CDs.</span></span> <span data-ttu-id="bbfbe-114">此進程稱為「 *燒錄*」。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-114">This process is called *burning*.</span></span>

<span data-ttu-id="bbfbe-115">若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-115">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="bbfbe-116">您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-116">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span> <span data-ttu-id="bbfbe-117">藉由使用 **count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 **IWMPCdrom** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-117">By using the **count** and **item** methods, you can iterate the collection to retrieve an **IWMPCdrom** interface pointer for each CD drive on the user's computer.</span></span> <span data-ttu-id="bbfbe-118">**IWMPCdrom** 介面代表個別的 CD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-118">The **IWMPCdrom** interface represents an individual CD drive.</span></span>

<span data-ttu-id="bbfbe-119">開始燒錄 CD 之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 **IWMPCdromBurn** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-119">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the **IWMPCdromBurn** interface.</span></span> <span data-ttu-id="bbfbe-120">藉由使用 **isAvailable** 方法，您可以判斷特定的 cd 光碟機是否可以燒錄 cd、磁片磁碟機中是否有光碟片，以及如何使用 cd。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-120">By using the **isAvailable** method, you can determine whether a particular CD drive can burn CDs, whether there is a CD in the drive, and how the CD can be used.</span></span>

<span data-ttu-id="bbfbe-121">若要指定要燒錄到 CD 的專案，您必須建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-121">To specify the items to burn to CD, you must create a playlist.</span></span> <span data-ttu-id="bbfbe-122">Windows Media Player 使用 **IWMPPlaylist** 介面表示播放清單。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-122">Windows Media Player represents playlists by using the **IWMPPlaylist** interface.</span></span> <span data-ttu-id="bbfbe-123">您可以用任何想要的方式建立此播放清單。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-123">You can create this playlist any way you like.</span></span> <span data-ttu-id="bbfbe-124">例如，您可以藉由呼叫 [IWMPMediaCollection：： getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum)，直接從程式庫取出播放清單。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-124">For example, you might simply retrieve a playlist from the library by calling [IWMPMediaCollection::getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum).</span></span> <span data-ttu-id="bbfbe-125">建立要燒錄到 CD 的播放清單之後，您必須呼叫 [IWMPCdromBurn：:p \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) 方法，並將播放清單指標當作引數傳遞。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-125">After you create the playlist that you want to burn to CD, you must call the [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) method and pass the playlist pointer as an argument.</span></span> <span data-ttu-id="bbfbe-126">這會將您的播放清單設定為 Windows Media Player 將複製到 CD 的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-126">This sets your playlist as the one that Windows Media Player will copy to the CD.</span></span>

<span data-ttu-id="bbfbe-127">如果您從媒體櫃取出播放清單，則對播放清單所做的任何變更都會反映在使用者的程式庫中。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-127">If you retrieve a playlist from the library, any changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="bbfbe-128">若要避免這種情況，請呼叫 [IWMPPlaylist：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo)，並傳遞屬性名稱 "暫時性" 和值 "true"。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-128">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="bbfbe-129">這會將您的播放清單實例轉換成暫時播放清單，而不需要變更原始播放清單即可進行編輯。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-129">This converts your playlist instance to a temporary playlist, which can be edited without changing the original playlist.</span></span>

<span data-ttu-id="bbfbe-130">每次您設定要燒錄的新播放清單，或對現有的燒錄播放清單進行變更時，都必須呼叫 [IWMPCdromBurn：： refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) 來更新狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-130">Each time you set a new playlist for burning, or make changes to an existing burn playlist, you must call [IWMPCdromBurn::refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) to update the status information.</span></span> <span data-ttu-id="bbfbe-131">這可確保 Windows Media Player 會執行必要的處理，以提供正確的 CD 燒錄操作狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-131">This ensures that Windows Media Player does the processing necessary to provide you with accurate status information for the CD burning operation.</span></span>

<span data-ttu-id="bbfbe-132">若要指定要燒錄的 CD 類型，請呼叫 [IWMPCdromBurn：:p 的 \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat)。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-132">To specify the type of CD to burn, call [IWMPCdromBurn::put\_burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat).</span></span> <span data-ttu-id="bbfbe-133">Windows Media Player 可讓您燒錄兩種類型的 Cd：音訊 Cd 和資料 Cd。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-133">Windows Media Player enables you to burn two types of CDs: audio CDs and data CDs.</span></span> <span data-ttu-id="bbfbe-134">[WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)列舉會定義 CD 類型。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-134">The [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) enumeration defines the CD types.</span></span>

<span data-ttu-id="bbfbe-135">您可以藉由呼叫 [IWMPCdromBurn：:p 內容卷 \_ 標](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label)來指定 CD 的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-135">You can specify a volume label for the CD by calling [IWMPCdromBurn::put\_label](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).</span></span>

<span data-ttu-id="bbfbe-136">當您準備好開始燒錄 CD 時，請呼叫 [IWMPCdromBurn：： startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-136">When you are ready to begin burning the CD, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span> <span data-ttu-id="bbfbe-137">您可以定期呼叫 [IWMPCdromBurn：： get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress)來監視燒錄作業的進度。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-137">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress).</span></span> <span data-ttu-id="bbfbe-138">這個方法會抓取整個燒錄作業的進度值。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-138">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="bbfbe-139">抓取的值是代表燒錄完成百分比的數位。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-139">The value retrieved is a number that represents the percentage of burning completed.</span></span> <span data-ttu-id="bbfbe-140">您可以藉由處理 [IWMPEvents3：： CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) 事件來監視燒錄作業的狀態，它會使用 [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) 列舉來指出目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-140">You can monitor the state of the burning operation by handling the [IWMPEvents3::CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) event, which uses the [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) enumeration to indicate the current state.</span></span> <span data-ttu-id="bbfbe-141">您應該小心將事件) 所提供的 **IWMPCdromBurn** 指標 (與代表您的燒錄作業的指標進行比較，以確保您的作業會引發事件。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-141">You should be careful to compare the **IWMPCdromBurn** pointer (provided by the event) to the pointer that represents your burning operation to ensure that the event was raised by your operation.</span></span> <span data-ttu-id="bbfbe-142">您可以藉由呼叫 [IWMPCdromBurn：： stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)來停止燒錄操作。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-142">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>

<span data-ttu-id="bbfbe-143">您可以處理兩個事件，以接收有關燒錄作業的錯誤通知。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-143">There are two events that you can handle to receive error notifications about your burning operation.</span></span> <span data-ttu-id="bbfbe-144">發生泛型錯誤時，就會引發 [IWMPEvents3：： CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) 事件。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-144">The [IWMPEvents3::CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) event is raised when a generic error occurs.</span></span> <span data-ttu-id="bbfbe-145">當特定媒體專案在燒錄期間造成錯誤時，就會引發[IWMPEvents3：： CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) 。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-145">[IWMPEvents3::CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) is raised when a particular media item causes an error during burning.</span></span> <span data-ttu-id="bbfbe-146">如同 **CdromBurnStateChange** 事件，每個事件都提供 **IWMPCdromBurn** 指標，代表引發事件的燒錄作業。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-146">Like the **CdromBurnStateChange** event, each of these events provides an **IWMPCdromBurn** pointer that represents the burning operation that raised the event.</span></span> <span data-ttu-id="bbfbe-147">**CdromBurnMediaError** 事件提供代表引發事件之媒體專案的 **IDispatch** 指標。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-147">The **CdromBurnMediaError** event provides an **IDispatch** pointer that represents the media item that raised the event.</span></span> <span data-ttu-id="bbfbe-148">您可以透過這個指標呼叫 **QueryInterface** 來取出 **IWMPMedia** 指標。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-148">You can call **QueryInterface** through this pointer to retrieve an **IWMPMedia** pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbfbe-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="bbfbe-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbfbe-150">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-150">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="bbfbe-151">**IWMPCdrom 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-151">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="bbfbe-152">**IWMPCdromBurn 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-152">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[<span data-ttu-id="bbfbe-153">**IWMPCdromCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-153">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="bbfbe-154">**IWMPEvents3 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-154">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[<span data-ttu-id="bbfbe-155">**IWMPMedia 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-155">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="bbfbe-156">**IWMPPlaylist 介面**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-156">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="bbfbe-157">**暫存屬性**</span><span class="sxs-lookup"><span data-stu-id="bbfbe-157">**Temporary Attribute**</span></span>](temporary-attribute.md)
</dt> </dl>

 

 




