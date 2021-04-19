---
title: 關於 CD 翻錄
description: 關於 CD 翻錄
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，關於
- 翻錄 Cd、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106990886"
---
# <a name="about-cd-ripping"></a><span data-ttu-id="07fb9-112">關於 CD 翻錄</span><span class="sxs-lookup"><span data-stu-id="07fb9-112">About CD Ripping</span></span>

<span data-ttu-id="07fb9-113">Windows Media Player 11 SDK 引進了新功能，可將音訊曲目從 Cd 複製到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="07fb9-113">The Windows Media Player 11 SDK introduces new functionality for copying audio tracks from CDs to the user's computer.</span></span> <span data-ttu-id="07fb9-114">此進程稱為「 *翻錄*」。</span><span class="sxs-lookup"><span data-stu-id="07fb9-114">This process is called *ripping*.</span></span>

<span data-ttu-id="07fb9-115">當您使用 Windows Media Player SDK 介面來翻錄音訊播放軌時，會使用使用者在 [Windows Media Player **選項** ] 對話方塊中定義的設定來建立所產生的音樂曲目。</span><span class="sxs-lookup"><span data-stu-id="07fb9-115">When you rip audio tracks by using the Windows Media Player SDK interfaces, the resulting music tracks are created by using the settings that the user defined in the Windows Media Player **Options** dialog box.</span></span>

<span data-ttu-id="07fb9-116">若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="07fb9-116">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="07fb9-117">您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="07fb9-117">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span> <span data-ttu-id="07fb9-118">藉由使用 **count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 **IWMPCdrom** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="07fb9-118">By using the **count** and **item** methods, you can iterate the collection to retrieve an **IWMPCdrom** interface pointer for each CD drive on the user's computer.</span></span> <span data-ttu-id="07fb9-119">**IWMPCdrom** 介面代表個別的 CD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="07fb9-119">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="07fb9-120">開始將 CD 翻錄之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 **IWMPCdromRip** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="07fb9-120">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the **IWMPCdromRip** interface.</span></span>

<span data-ttu-id="07fb9-121">若要開始進行翻錄作業，只要呼叫 [IWMPCdromRip：： startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)即可。</span><span class="sxs-lookup"><span data-stu-id="07fb9-121">To start the ripping operation, simply call [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span> <span data-ttu-id="07fb9-122">您可以定期呼叫 [IWMPCdromRip：： get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)來監視翻錄作業的進度。</span><span class="sxs-lookup"><span data-stu-id="07fb9-122">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="07fb9-123">這個方法會抓取整個翻錄作業的進度值。</span><span class="sxs-lookup"><span data-stu-id="07fb9-123">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="07fb9-124">抓取的值是表示完成的完成百分比的數位。</span><span class="sxs-lookup"><span data-stu-id="07fb9-124">The value retrieved is a number that represents the percentage of ripping completed.</span></span> <span data-ttu-id="07fb9-125">您可以定期呼叫 [IWMPCdromRip：： get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)來監視翻錄作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="07fb9-125">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="07fb9-126">這個方法會抓取 [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) 列舉值，這個值表示作業正在進行中或已停止。</span><span class="sxs-lookup"><span data-stu-id="07fb9-126">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="07fb9-127">您也可以藉由處理 [IWMPEvents3：： CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) 事件，來監視「翻錄」作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="07fb9-127">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="07fb9-128">請小心將事件) 所提供的 **IWMPCdromRip** 指標 (與代表您的翻錄作業的指標進行比較，以確保您的作業會引發事件。</span><span class="sxs-lookup"><span data-stu-id="07fb9-128">You should be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation to ensure that the event was raised by your operation.</span></span> <span data-ttu-id="07fb9-129">您可以藉由呼叫 [IWMPCdromRip：： stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)來停止翻錄作業。</span><span class="sxs-lookup"><span data-stu-id="07fb9-129">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>

<span data-ttu-id="07fb9-130">若要接收有關翻錄作業的錯誤通知，您可以處理 [IWMPEvents3：： CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) 事件。</span><span class="sxs-lookup"><span data-stu-id="07fb9-130">To receive error notifications about a ripping operation, you can handle the [IWMPEvents3::CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) event.</span></span> <span data-ttu-id="07fb9-131">如同 **CdromRipStateChange**，這個事件提供 **IWMPCdromRip** 介面指標，代表引發事件的翻錄作業。</span><span class="sxs-lookup"><span data-stu-id="07fb9-131">Like **CdromRipStateChange**, this event provides an **IWMPCdromRip** interface pointer that represents the ripping operation that raised the event.</span></span> <span data-ttu-id="07fb9-132">此事件也會提供代表引發事件之媒體專案的 **IDispatch** 指標。</span><span class="sxs-lookup"><span data-stu-id="07fb9-132">The event also provides an **IDispatch** pointer that represents the media item that raised the event.</span></span> <span data-ttu-id="07fb9-133">您可以透過這個指標呼叫 **QueryInterface** 來取出 **IWMPMedia** 指標。</span><span class="sxs-lookup"><span data-stu-id="07fb9-133">You can call **QueryInterface** through this pointer to retrieve an **IWMPMedia** pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07fb9-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="07fb9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07fb9-135">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="07fb9-135">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




