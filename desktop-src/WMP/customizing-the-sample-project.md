---
title: 自訂範例專案
description: 自訂範例專案
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player 線上商店，自訂範例專案
- 線上商店，自訂範例專案
- 輸入2個線上商店，自訂範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 自訂範例專案
- 範例，請輸入2個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932501"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="22eef-111">自訂範例專案</span><span class="sxs-lookup"><span data-stu-id="22eef-111">Customizing the Sample Project</span></span>

<span data-ttu-id="22eef-112">建立您自己的線上商店時，您會想要在名為 Yourproject。的檔案中變更下列方法的實作為：</span><span class="sxs-lookup"><span data-stu-id="22eef-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="22eef-113">**CYourProject：： allowPlay**。</span><span class="sxs-lookup"><span data-stu-id="22eef-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="22eef-114">您可以使用此函式來套用商務規則，以允許播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="22eef-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="22eef-115">**CYourProject：：允許 cdburn.exe**。</span><span class="sxs-lookup"><span data-stu-id="22eef-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="22eef-116">您可以使用此函式來套用商務規則，讓使用者可以將受保護的內容複製到 CD。</span><span class="sxs-lookup"><span data-stu-id="22eef-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="22eef-117">**CYourProject：： allowPDATransfer**。</span><span class="sxs-lookup"><span data-stu-id="22eef-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="22eef-118">您可以使用此函式來套用商務規則，讓使用者可以將受保護的內容傳送到可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="22eef-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="22eef-119">**CYourProject：： startBackgroundProcessing**。</span><span class="sxs-lookup"><span data-stu-id="22eef-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="22eef-120">使用此函式可起始您所需的任何背景處理工作。</span><span class="sxs-lookup"><span data-stu-id="22eef-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="22eef-121">例如，您可以使用這種方式來檢查過期的授權。</span><span class="sxs-lookup"><span data-stu-id="22eef-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="22eef-122">**CYourProject：:D eviceavailable**。</span><span class="sxs-lookup"><span data-stu-id="22eef-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="22eef-123">使用此函式可起始與連線裝置相關的任何工作。</span><span class="sxs-lookup"><span data-stu-id="22eef-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="22eef-124">**CYourProject：:P repareforsync**。</span><span class="sxs-lookup"><span data-stu-id="22eef-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="22eef-125">使用此函式可在將數位媒體同步至裝置之前，執行必要的工作。</span><span class="sxs-lookup"><span data-stu-id="22eef-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="22eef-126">**CYourProject：： serviceEvent**。</span><span class="sxs-lookup"><span data-stu-id="22eef-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="22eef-127">您可以使用此函式來開始和結束您要在線上商店為使用中時執行的工作。</span><span class="sxs-lookup"><span data-stu-id="22eef-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="22eef-128">**CYourProject：： stopBackgroundProcessing**。</span><span class="sxs-lookup"><span data-stu-id="22eef-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="22eef-129">使用此函式可在 Windows Media Player 呼叫 **CYourProject：： startBackgroundProcessing** 時，停止您啟動的任何背景處理工作。</span><span class="sxs-lookup"><span data-stu-id="22eef-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="22eef-130">使用媒體和播放清單物件</span><span class="sxs-lookup"><span data-stu-id="22eef-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="22eef-131">**AllowPlay** 方法會提供 **IWMPMedia** 介面的指標作為參數。</span><span class="sxs-lookup"><span data-stu-id="22eef-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="22eef-132">此介面是表示媒體物件的 Windows Media Player 介面。</span><span class="sxs-lookup"><span data-stu-id="22eef-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="22eef-133">藉由呼叫此介面上的方法，您可以使用個別媒體專案的屬性和屬性。</span><span class="sxs-lookup"><span data-stu-id="22eef-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="22eef-134">**AllowCDBurn** 和 **AllowPDATransfer** 方法提供 **IWMPPlaylist** 介面的指標作為參數。</span><span class="sxs-lookup"><span data-stu-id="22eef-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="22eef-135">此介面是代表播放清單物件的 Windows Media Player 介面。</span><span class="sxs-lookup"><span data-stu-id="22eef-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="22eef-136">藉由呼叫此介面上的方法，您可以使用播放清單的屬性和屬性、將專案新增至播放清單，或從播放清單中移除專案。</span><span class="sxs-lookup"><span data-stu-id="22eef-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="22eef-137">若要瞭解如何以程式設計方式從播放清單中移除專案，請參閱 **CAllowBaseDialog <T> ：： OnRemoveMediaFromPlaylist** 的實。</span><span class="sxs-lookup"><span data-stu-id="22eef-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="22eef-138">若要深入瞭解如何使用媒體和播放清單物件，請參閱 [指令碼語言的播放程式物件模型](player-object-model-for-scripting-languages.md)。</span><span class="sxs-lookup"><span data-stu-id="22eef-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="22eef-139">可以移除的程式碼</span><span class="sxs-lookup"><span data-stu-id="22eef-139">Code That Can Be Removed</span></span>

<span data-ttu-id="22eef-140">您可能會想要移除開啟對話方塊的程式碼，因為不太可能會想要讓使用者決定哪些媒體專案可以播放或複製。</span><span class="sxs-lookup"><span data-stu-id="22eef-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="22eef-141">從 Yourproject。中移除下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="22eef-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="22eef-142">**CAllowBaseDialog** 的宣告。</span><span class="sxs-lookup"><span data-stu-id="22eef-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="22eef-143">**CAllowBurnDialog** 的宣告。</span><span class="sxs-lookup"><span data-stu-id="22eef-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="22eef-144">**CAllowTransferDialog** 的宣告。</span><span class="sxs-lookup"><span data-stu-id="22eef-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="22eef-145">從 Yourproject。 .cpp 移除下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="22eef-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="22eef-146">**CAllowBaseDialog <T> ：： OnInitDialog** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="22eef-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="22eef-147">**CAllowBaseDialog <T> ：： OnRemoveMediaFromPlaylist** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="22eef-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22eef-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="22eef-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22eef-149">**建立 Type 2 線上商店的外掛程式**</span><span class="sxs-lookup"><span data-stu-id="22eef-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




