---
title: 關於 VML 的常見問題
description: 關於 VML 的常見問題
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Vector Markup Language (VML) ，常見問題
- VML (Vector Markup Language) ，常見問題
- 向量圖形，常見問題
- Vector Markup Language (VML) ，常見問題
- VML (Vector Markup Language) ，常見問題
- 向量圖形，常見問題
- Vector Markup Language (VML) 、GIF 差異
- VML (Vector Markup Language) 、GIF 差異
- Vector Markup Language (VML) 、PNG 差異
- VML (Vector Markup Language) ，PNG 差異
- 向量圖形，點陣格式差異
- Vector Markup Language (VML) 、XML
- VML (Vector Markup Language) 、XML
- 向量圖形，XML
- Vector Markup Language (VML) 、動畫
- VML (Vector Markup Language) 、動畫
- 向量圖形、動畫
- Vector Markup Language (VML) ，Macromedia Flash
- VML (Vector Markup Language) ，Macromedia Flash
- 向量圖形，Macromedia Flash
- 點陣格式
- 動畫
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933453"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="13dbc-126">關於 VML 的常見問題</span><span class="sxs-lookup"><span data-stu-id="13dbc-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="13dbc-127">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="13dbc-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="13dbc-128">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="13dbc-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="13dbc-129">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="13dbc-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="13dbc-130">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="13dbc-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="13dbc-131">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="13dbc-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="13dbc-132">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="13dbc-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="13dbc-133">VML 會與 GIF 和 PNG 競爭嗎？</span><span class="sxs-lookup"><span data-stu-id="13dbc-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="13dbc-134">不會。</span><span class="sxs-lookup"><span data-stu-id="13dbc-134">No.</span></span> <span data-ttu-id="13dbc-135">GIF 和 PNG 都是可用於儲存向量圖形的點陣 (或位對應的) 格式。</span><span class="sxs-lookup"><span data-stu-id="13dbc-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="13dbc-136">點陣格式會儲存每個圖元，而像是 VML 的向量格式會使用數學描述或外框來描述圖形。</span><span class="sxs-lookup"><span data-stu-id="13dbc-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="13dbc-137">以向量為基礎的格式儲存的向量圖形比以點陣格式儲存的圖更精簡，讓 Web 使用者的下載時間更快。</span><span class="sxs-lookup"><span data-stu-id="13dbc-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="13dbc-138">此外，VML 圖形會以內嵌方式傳遞至 HTML 網頁，而不是依賴外部檔案，就像是現在使用 GIF 和 PNG 的情況一樣。</span><span class="sxs-lookup"><span data-stu-id="13dbc-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="13dbc-139">這可讓 VML 圖形調整頁面大小，並與其他網頁專案互動，進而改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="13dbc-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="13dbc-140">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="13dbc-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="13dbc-141">當 XML 幾乎不在使用時，Microsoft 如何支援另一個以 XML 為基礎的標準，而且夠好用。</span><span class="sxs-lookup"><span data-stu-id="13dbc-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="13dbc-142">XML 是一種功能強大但簡單的方法，用來表示網路上的結構化資料，並且完全補充 HTML 來顯示。</span><span class="sxs-lookup"><span data-stu-id="13dbc-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="13dbc-143">VML 是許多應用程式專屬的 XML 格式範例，將在未來幾個月內開發和實行。</span><span class="sxs-lookup"><span data-stu-id="13dbc-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="13dbc-144">比方說，在下一版的 Office 中，VML 將用來標注 HTML 檔案，以保留原生 Office 檔案格式與 HTML 之間的 Office 藝術圖形格式資訊，進而讓 Office 使用者能在這兩種格式之間無縫切換。</span><span class="sxs-lookup"><span data-stu-id="13dbc-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="13dbc-145">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="13dbc-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="13dbc-146">誰將支援 VML？</span><span class="sxs-lookup"><span data-stu-id="13dbc-146">Who will support VML?</span></span>

<span data-ttu-id="13dbc-147">我們預期許多廠商都支援 VML。</span><span class="sxs-lookup"><span data-stu-id="13dbc-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="13dbc-148">例如，Autodesk、Hewlett-Packard、Macromedia 和 VISIO 在產品的未來版本中有 pledged 的支援。</span><span class="sxs-lookup"><span data-stu-id="13dbc-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="13dbc-149">Microsoft 在未來的平臺版本（例如 Internet Explorer）中已 pledged 了 VML 的支援。</span><span class="sxs-lookup"><span data-stu-id="13dbc-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="13dbc-150">此外，您還可以在下一代的 Office 中使用 VML 來啟用 Office 格式與 HTML 之間的「往返」。</span><span class="sxs-lookup"><span data-stu-id="13dbc-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="13dbc-151">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="13dbc-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="13dbc-152">VML 支援動畫嗎？</span><span class="sxs-lookup"><span data-stu-id="13dbc-152">Does VML support animation?</span></span>

<span data-ttu-id="13dbc-153">否，目前沒有。</span><span class="sxs-lookup"><span data-stu-id="13dbc-153">No, it currently doesn't.</span></span> <span data-ttu-id="13dbc-154">不過，我們與 VML 合作夥伴合作，將動畫功能加入至 VML 格式。</span><span class="sxs-lookup"><span data-stu-id="13dbc-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="13dbc-155">由於 VML 是以 XML 為基礎，因此可以輕鬆擴充標記集以取得額外的功能。</span><span class="sxs-lookup"><span data-stu-id="13dbc-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="13dbc-156">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="13dbc-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="13dbc-157">VML 會取代 Macromedia Flash 嗎？</span><span class="sxs-lookup"><span data-stu-id="13dbc-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="13dbc-158">未 Macromedia 只是將向量圖形的 Flash 格式提交給 W3C 嗎？</span><span class="sxs-lookup"><span data-stu-id="13dbc-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="13dbc-159">不會。</span><span class="sxs-lookup"><span data-stu-id="13dbc-159">No.</span></span> <span data-ttu-id="13dbc-160">VML 是向量圖形的文字型交換和傳遞格式，而 Flash 是一種二進位格式，可傳遞以向量為基礎的圖形和動畫。</span><span class="sxs-lookup"><span data-stu-id="13dbc-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="13dbc-161">Macromedia 未將其檔案格式提交給 W3C。</span><span class="sxs-lookup"><span data-stu-id="13dbc-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="13dbc-162">不過，他們已針對應用程式開發人員、Web 開發人員和使用者開啟其檔案格式。</span><span class="sxs-lookup"><span data-stu-id="13dbc-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="13dbc-163">如需相關資訊，請參閱 <https://www.macromedia.com> 。</span><span class="sxs-lookup"><span data-stu-id="13dbc-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="13dbc-164">返回 VML 總覽</span><span class="sxs-lookup"><span data-stu-id="13dbc-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 