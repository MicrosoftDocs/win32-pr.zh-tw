---
title: 關於程式庫服務
description: 關於程式庫服務
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player 程式庫，關於
- Windows Media Player 程式庫，服務
- 程式庫，服務
- 程式庫，關於
- Windows Media Player、程式庫服務的版本
- 列舉，程式庫服務
- 事件，程式庫服務
- 範例，程式庫服務
- 介面，程式庫服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106967249"
---
# <a name="about-library-services"></a><span data-ttu-id="ba008-119">關於程式庫服務</span><span class="sxs-lookup"><span data-stu-id="ba008-119">About Library Services</span></span>

<span data-ttu-id="ba008-120">在舊版 Windows Media Player 中，軟體會為每個使用者使用單一程式庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-120">In earlier versions of Windows Media Player, the software used a single library database for each user.</span></span> <span data-ttu-id="ba008-121">此資料庫儲存在使用者的電腦上，並且在概念上與使用者和特定的播放程式實例相關聯。</span><span class="sxs-lookup"><span data-stu-id="ba008-121">This database was stored on the user's computer and was conceptually tied to the user and a particular instance of the Player.</span></span>

<span data-ttu-id="ba008-122">Windows Media Player 11 引進了多個和遠端程式庫的概念。</span><span class="sxs-lookup"><span data-stu-id="ba008-122">Windows Media Player 11 introduces the concepts of multiple and remote libraries.</span></span> <span data-ttu-id="ba008-123">現在除了預設值或 *本機* 程式庫之外，Windows Media Player 可以顯示從其他電腦連接到網路的程式庫抓取的內容，其中可能包括其他登入同一部電腦的使用者。</span><span class="sxs-lookup"><span data-stu-id="ba008-123">Now, in addition to its default, or *local*, library, Windows Media Player can display content retrieved from libraries on other computers connected to a network, which might include other users logged on to the same computer.</span></span> <span data-ttu-id="ba008-124">播放機也可以顯示來自其他來源的程式庫視圖，例如已啟用 MTP 的裝置或資料 Cd。</span><span class="sxs-lookup"><span data-stu-id="ba008-124">The Player can also display library views from other sources, such as MTP-enabled devices or data CDs.</span></span> <span data-ttu-id="ba008-125">從使用者的觀點來看，這表示位於許多不同地點的數位媒體內容可以使用相同、熟悉的 Windows Media Player 使用者介面，從多個位置進行管理。</span><span class="sxs-lookup"><span data-stu-id="ba008-125">From the end user's perspective, this means that digital media content located in many different places can be managed from multiple locations by using the same, familiar Windows Media Player user interface.</span></span> <span data-ttu-id="ba008-126">從開發人員的觀點來看，這表示您可以使用 Windows Media Player SDK COM 介面來列舉可用的程式庫，然後使用它們，就像您已在舊版中使用本機程式庫一樣。</span><span class="sxs-lookup"><span data-stu-id="ba008-126">From the developer's perspective, this means that you can use the Windows Media Player SDK COM interfaces to enumerate the available libraries and then use them like you have used the local library in earlier versions.</span></span>

<span data-ttu-id="ba008-127">若要列舉可用的程式庫，請使用 **IWMPLibraryServices** 介面。</span><span class="sxs-lookup"><span data-stu-id="ba008-127">To enumerate the available libraries, use the **IWMPLibraryServices** interface.</span></span> <span data-ttu-id="ba008-128">此介面會公開 [IWMPLibraryServices：： getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) 方法，以抓取指定類型的程式庫計數。</span><span class="sxs-lookup"><span data-stu-id="ba008-128">This interface exposes the [IWMPLibraryServices::getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) method, which retrieves the count of libraries of a given type.</span></span> <span data-ttu-id="ba008-129">程式庫類型是由 [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) 列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="ba008-129">Library types are defined by the [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) enumeration.</span></span> <span data-ttu-id="ba008-130">此列舉包含本機程式庫的值 wmpltLocal。</span><span class="sxs-lookup"><span data-stu-id="ba008-130">This enumeration includes a value for the local library, wmpltLocal.</span></span> <span data-ttu-id="ba008-131">這是因為程式庫服務功能一律可讓您使用 **IWMPLibraryServices** 和相關的介面來處理本機程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-131">This is because the library services feature always enables you work with the local library by using **IWMPLibraryServices** and the related interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="ba008-132">**WMPLibraryType** 列舉包含值 wmpltRemote，代表網路共用的媒體程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-132">The **WMPLibraryType** enumeration includes the value wmpltRemote, which represents media libraries shared by the network.</span></span> <span data-ttu-id="ba008-133">若要存取這些共用程式庫，Player 控制項必須在遠端模式中執行。</span><span class="sxs-lookup"><span data-stu-id="ba008-133">To access those shared libraries, the Player control must be running in remote mode.</span></span> <span data-ttu-id="ba008-134">如需在遠端模式中執行播放程式控制項的相關資訊，請參閱 [遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。</span><span class="sxs-lookup"><span data-stu-id="ba008-134">For information about running the Player control in remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

 

<span data-ttu-id="ba008-135">在您抓取程式庫計數之後，您可以在迴圈中重複呼叫 [IWMPLibraryServices：： getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) 來逐一查看可用的程式庫集合，並傳遞新的索引值給每個反復專案。</span><span class="sxs-lookup"><span data-stu-id="ba008-135">After you retrieve the library count, you can iterate the collection of available libraries by repeatedly calling [IWMPLibraryServices::getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) in a loop, passing a new index value with each iteration.</span></span> <span data-ttu-id="ba008-136">這個方法會抓取 [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) 介面的指標，代表個別的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-136">This method retrieves a pointer to an [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) interface, which represents the individual library.</span></span>

<span data-ttu-id="ba008-137">在您抓取 **IWMPLibrary** 的指標之後，您可以呼叫 [IWMPLibrary：： get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) 來取得 **IWMPMediaCollection** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ba008-137">After you retrieve a pointer to **IWMPLibrary**, you can call [IWMPLibrary::get\_mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) to retrieve a pointer to an **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="ba008-138">您可以使用這個介面指標來使用個別的程式庫，就像使用本機程式庫一樣。</span><span class="sxs-lookup"><span data-stu-id="ba008-138">With this interface pointer, you can work with an individual library much like you would use the local library.</span></span> <span data-ttu-id="ba008-139">您也可以藉由呼叫 [IWMPLibrary：： get \_ name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)來取出包含程式庫名稱的字串，如果您需要對使用者顯示程式庫名稱，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="ba008-139">You can also retrieve a string containing the name of the library by calling [IWMPLibrary::get\_name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), which is useful if you need to display the library name to the user.</span></span> <span data-ttu-id="ba008-140">您可以呼叫 [IWMPLibrary：： get \_ 類型](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) 來取得特定程式庫的 **WMPLibraryType** 。</span><span class="sxs-lookup"><span data-stu-id="ba008-140">You can call [IWMPLibrary::get\_type](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) to get the **WMPLibraryType** of a particular library.</span></span>

<span data-ttu-id="ba008-141">您可以處理 [IWMPEvents3：： LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) 事件，以瞭解程式庫何時可供使用，以及 [IWMPEvents3：： LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) 事件以瞭解程式庫何時中斷連線。</span><span class="sxs-lookup"><span data-stu-id="ba008-141">You can handle the [IWMPEvents3::LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) event to know when a library becomes available and the [IWMPEvents3::LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) event to know when a library disconnects.</span></span> <span data-ttu-id="ba008-142">每個事件都提供 **IWMPLibrary** 指標，表示連接或中斷連接的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-142">Each of these events provides an **IWMPLibrary** pointer that represents the library that connected or disconnected.</span></span> <span data-ttu-id="ba008-143">您可以呼叫 [IWMPLibrary：： isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) 來判斷連接或中斷連線的程式庫是否為您目前使用的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ba008-143">You can call [IWMPLibrary::isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) to determine whether the library that connected or disconnected is a library that you are currently using.</span></span>

<span data-ttu-id="ba008-144">相較于使用 [IWMPCore：： get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection)所抓取的程式庫，使用透過 **IWMPLibraryServices** 介面抓取的程式庫時，有一些重要的差異。</span><span class="sxs-lookup"><span data-stu-id="ba008-144">There are some important differences when you work with a library retrieved through the **IWMPLibraryServices** interface compared to working with a library retrieved by using [IWMPCore::get\_mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection).</span></span> <span data-ttu-id="ba008-145">適用下列差異：</span><span class="sxs-lookup"><span data-stu-id="ba008-145">The following differences apply:</span></span>

-   <span data-ttu-id="ba008-146">從透過 **IWMPLibraryServices** 抓取的程式庫，您通常可以更快地取出查詢結果。</span><span class="sxs-lookup"><span data-stu-id="ba008-146">You can usually retrieve query results much faster from libraries retrieved through **IWMPLibraryServices**.</span></span> <span data-ttu-id="ba008-147"> (這會假設其他因素，例如網路和硬碟存取時間相等。 ) </span><span class="sxs-lookup"><span data-stu-id="ba008-147">(This assumes that other factors such as network and hard disk access times are equal.)</span></span>
-   <span data-ttu-id="ba008-148">從透過 **IWMPLibraryServices** 抓取的程式庫中可用的媒體專案中繼資料屬性清單，通常是透過 [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)抓取之本機程式庫中可用的媒體專案中繼資料屬性的子集。</span><span class="sxs-lookup"><span data-stu-id="ba008-148">The list of media item metadata attributes available from libraries retrieved through **IWMPLibraryServices** is usually a subset of those available from the local library retrieved through [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).</span></span>
-   <span data-ttu-id="ba008-149">如果您透過 **IWMPLibraryServices** 抓取本機程式庫，則可以使用所有相同的屬性，因為當您透過 **IWMPCore** 抓取本機程式庫時可使用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ba008-149">If you retrieve the local library through **IWMPLibraryServices**, all of the same attributes are available for your use as those available when you retrieve the local library through **IWMPCore**.</span></span> <span data-ttu-id="ba008-150">不過，您可以更快速地為最常使用的屬性取得查詢結果。</span><span class="sxs-lookup"><span data-stu-id="ba008-150">However, you will be able to retrieve query results much faster for the most commonly-used attributes.</span></span>
-   <span data-ttu-id="ba008-151">當您使用透過 **IWMPLibraryServices** 抓取的程式庫時，您應該使用字串集合來建立使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="ba008-151">You should use string collections to create user interface elements when you work with libraries retrieved through **IWMPLibraryServices**.</span></span> <span data-ttu-id="ba008-152">例如， [IWMPMediaCollection2：： getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) 可讓您使用由 **IWMPQuery** 介面表示的自訂查詢 (，) 抓取字串集合。</span><span class="sxs-lookup"><span data-stu-id="ba008-152">For example, [IWMPMediaCollection2::getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) enables you to use a custom query (represented by the **IWMPQuery** interface) to retrieve a string collection.</span></span>
-   <span data-ttu-id="ba008-153">透過 **IWMPLibraryServices** 介面抓取的遠端程式庫，可能不一定會連接到目前的播放機實例。</span><span class="sxs-lookup"><span data-stu-id="ba008-153">Remote libraries retrieved through the **IWMPLibraryServices** interface might not always be connected to the current Player instance.</span></span> <span data-ttu-id="ba008-154">這表示，處理 **LibraryConnect** 和 **LibraryDisconnect** 事件，以瞭解程式庫可用性何時變更，以及處理 [IWMPEvents3：： StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) 事件，以瞭解在您用來顯示使用者介面元素的字串集合中加入或移除字串時。</span><span class="sxs-lookup"><span data-stu-id="ba008-154">This means that it is important to handle the **LibraryConnect** and **LibraryDisconnect** events to know when library availability changes, and to handle the [IWMPEvents3::StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) event to know when strings are added to or removed from the string collections you use to display user interface elements.</span></span> <span data-ttu-id="ba008-155">基於類似的原因，您也應該處理本機程式庫的 **StringCollectionChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="ba008-155">You should also handle **StringCollectionChange** events for the local library for similar reasons.</span></span>

<span data-ttu-id="ba008-156">請務必瞭解，特定程式庫的字串集合隨時都可變更。</span><span class="sxs-lookup"><span data-stu-id="ba008-156">It is important to understand that string collections for a particular library can change at any time.</span></span> <span data-ttu-id="ba008-157">當您第一次取出時，字串集合可能是空的，就像是最近連接的程式庫，但播放程式尚未列舉其內容。</span><span class="sxs-lookup"><span data-stu-id="ba008-157">A string collection could be empty when you first retrieve it, as in the case of a library that has recently connected but the Player has not yet enumerated its contents.</span></span> <span data-ttu-id="ba008-158">相反地，字串集合可能已經包含您需要的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="ba008-158">Conversely, a string collection might already contain all the information you need.</span></span> <span data-ttu-id="ba008-159">在這種情況下，您可能永遠不會收到 **StringCollectionChange** 事件，因為在您建立查詢之前已完全列舉程式庫的內容，而且沒有任何其他變更。</span><span class="sxs-lookup"><span data-stu-id="ba008-159">In this case, you might never receive a **StringCollectionChange** event because the library's contents had been completely enumerated before you created your query and nothing else is changing.</span></span>

<span data-ttu-id="ba008-160">因此，若要讓使用者介面保持在最新的，您必須在抓取 **IWMPStringCollection** 介面時列舉字串集合內容，並在發生更新時處理 **StringCollectionChange** 事件以瞭解更新。</span><span class="sxs-lookup"><span data-stu-id="ba008-160">Therefore, to keep your user interface current, you must both enumerate the string collection contents when you retrieve the **IWMPStringCollection** interface and handle the **StringCollectionChange** event to know about updates when they happen.</span></span>

## <a name="sample"></a><span data-ttu-id="ba008-161">範例</span><span class="sxs-lookup"><span data-stu-id="ba008-161">Sample</span></span>

<span data-ttu-id="ba008-162">名為 WMPML 的範例示範如何使用程式庫服務。</span><span class="sxs-lookup"><span data-stu-id="ba008-162">The sample named WMPML demonstrates how to work with library services.</span></span> <span data-ttu-id="ba008-163">如需 Windows Media Player SDK 範例的詳細資訊，請參閱 [範例](samples.md)。</span><span class="sxs-lookup"><span data-stu-id="ba008-163">For more information about Windows Media Player SDK samples, see [Samples](samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba008-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba008-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba008-165">**關於程式庫**</span><span class="sxs-lookup"><span data-stu-id="ba008-165">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="ba008-166">**關於 Query 物件**</span><span class="sxs-lookup"><span data-stu-id="ba008-166">**About the Query Object**</span></span>](about-the-query-object.md)
</dt> <dt>

[<span data-ttu-id="ba008-167">**IWMPEvents3 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-167">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[<span data-ttu-id="ba008-168">**IWMPLibrary 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-168">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[<span data-ttu-id="ba008-169">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ba008-169">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ba008-170">**IWMPLibraryServices 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-170">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[<span data-ttu-id="ba008-171">**IWMPLibraryServices 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ba008-171">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ba008-172">**IWMPMediaCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-172">**IWMPMediaCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[<span data-ttu-id="ba008-173">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ba008-173">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ba008-174">**IWMPStringCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-174">**IWMPStringCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[<span data-ttu-id="ba008-175">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ba008-175">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ba008-176">**IWMPQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="ba008-176">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[<span data-ttu-id="ba008-177">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ba008-177">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ba008-178">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="ba008-178">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




