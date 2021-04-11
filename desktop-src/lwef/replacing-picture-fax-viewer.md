---
title: 使用預覽動詞來取代 Windows 圖片和傳真檢視器應用程式
description: 在 Windows XP 中，使用者可以查看、旋轉、列印和縮放影像。
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows 圖片和傳真檢視器
- 預覽動詞
- 最佳做法、Windows 圖片和傳真檢視器
- 最佳做法，預覽動詞
- 效能、Windows 圖片和傳真檢視器
- 效能，預覽動詞
- 註冊、預覽動詞
- 註冊、投影片動詞
- 投影片動詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6769e13aaea41b3b05bbf674ea95d7f88fb646
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933243"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a><span data-ttu-id="8c9bb-112">使用預覽動詞來取代 Windows 圖片和傳真檢視器應用程式</span><span class="sxs-lookup"><span data-stu-id="8c9bb-112">Replacing the Windows Picture and Fax Viewer Application Using the Preview Verb</span></span>

<span data-ttu-id="8c9bb-113">\[只有在 Windows XP 下才支援圖片和傳真檢視器功能。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-113">\[The Picture and Fax Viewer feature is supported only under Windows XP.</span></span> <span data-ttu-id="8c9bb-114">\]</span><span class="sxs-lookup"><span data-stu-id="8c9bb-114">\]</span></span>

<span data-ttu-id="8c9bb-115">在 Windows XP 中，使用者可以查看、旋轉、列印和縮放影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-115">As of Windows XP, users can view, rotate, print, and zoom images.</span></span> <span data-ttu-id="8c9bb-116">其中有些功能是透過 Windows Shell 提供，有些則是透過 Windows 圖片和傳真檢視器應用程式來提供。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-116">Some of these features are provided through the Windows Shell, and others through the Windows Picture and Fax Viewer application.</span></span> <span data-ttu-id="8c9bb-117">雖然 Windows 圖片和傳真檢視器提供絕佳的功能基準，而且是映射體驗的重要部分，如果您選擇，則可以輕鬆地將它取代為不同的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-117">While Windows Picture and Fax Viewer provides an excellent baseline of features and is a key part of the imaging experience, if you choose to, you can easily replace it with a different application.</span></span> <span data-ttu-id="8c9bb-118">本檔的設計目的是協助您有效地取代 Windows 圖片和傳真檢視器應用程式，而不會遺失重要功能或降低使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-118">This document is designed to help you effectively replace the Windows Picture and Fax Viewer application without losing important features or degrading the user experience.</span></span>

-   [<span data-ttu-id="8c9bb-119">最佳作法</span><span class="sxs-lookup"><span data-stu-id="8c9bb-119">Best Practices</span></span>](#best-practices)
    -   [<span data-ttu-id="8c9bb-120">效能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-120">Performance</span></span>](#performance)
    -   [<span data-ttu-id="8c9bb-121">功能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-121">Features</span></span>](#features)
    -   [<span data-ttu-id="8c9bb-122">格式支援</span><span class="sxs-lookup"><span data-stu-id="8c9bb-122">Format Support</span></span>](#format-support)
-   [<span data-ttu-id="8c9bb-123">註冊預覽動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-123">Registering for the Preview Verb</span></span>](#registering-for-the-preview-verb)
-   [<span data-ttu-id="8c9bb-124">註冊編輯動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-124">Registering for the Edit Verb</span></span>](#registering-for-the-edit-verb)
-   [<span data-ttu-id="8c9bb-125">註冊投影片動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-125">Registering for the Slideshow Verb</span></span>](#registering-for-the-slideshow-verb)
-   [<span data-ttu-id="8c9bb-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c9bb-126">Related topics</span></span>](#related-topics)

## <a name="best-practices"></a><span data-ttu-id="8c9bb-127">最佳做法</span><span class="sxs-lookup"><span data-stu-id="8c9bb-127">Best Practices</span></span>

<span data-ttu-id="8c9bb-128">在 Windows XP 和更新版本中，Shell 包含的動詞命令可讓使用者預覽影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-128">In Windows XP and later, the Shell includes a verb that you can use to enable users to preview images.</span></span> <span data-ttu-id="8c9bb-129">這稱為 *預覽*。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-129">It is called *Preview*.</span></span> <span data-ttu-id="8c9bb-130">此動詞會反白顯示影像的主要使用者工作，也就是正在觀看的影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-130">This verb highlights the main user task for images, which is viewing.</span></span> <span data-ttu-id="8c9bb-131">為了讓此體驗順利運作，Windows 圖片和傳真檢視器應用程式預設會擁有預覽關聯。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-131">To make this experience work well, the Windows Picture and Fax Viewer application owns the preview association by default.</span></span>

<span data-ttu-id="8c9bb-132">Windows 圖片和傳真檢視器，或任何擁有檔案關聯的應用程式，都包含啟動使用者編輯應用程式的專案。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-132">The Windows Picture and Fax Viewer, or any application that owns a file association, includes an item that launches the user's editing application.</span></span> <span data-ttu-id="8c9bb-133">因為預覽動詞命令只是用來預覽影像，而不是編輯它們，所以您的應用程式在宣告該關聯時，必須小心遵循本檔中的建議。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-133">Because the Preview verb is only used to preview images rather than edit them, your application must be careful to follow the recommendations in this document when claiming that association.</span></span>

<span data-ttu-id="8c9bb-134">您想要確保編輯影像的應用程式仍然可以接管編輯動詞。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-134">You want to ensure that an application that edits images can still take over the Edit verb.</span></span> <span data-ttu-id="8c9bb-135">例如，如果使用者有 Microsoft 圖片！</span><span class="sxs-lookup"><span data-stu-id="8c9bb-135">For example, if a user has Microsoft Picture It!</span></span> <span data-ttu-id="8c9bb-136">已安裝，當他們按兩下 .jpg 檔案時，電腦應該會啟動 [Windows 圖片及傳真檢視器] 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-136">installed, when they double-click a .jpg file the computer should launch the Windows Picture and Fax Viewer application.</span></span> <span data-ttu-id="8c9bb-137">但是，當他們按一下工具列中的 [ **編輯** ] 時，電腦應該會啟動圖片！</span><span class="sxs-lookup"><span data-stu-id="8c9bb-137">But, when they click **Edit** in the toolbar, then the computer should launch Picture It!</span></span> <span data-ttu-id="8c9bb-138">使用這個 .jpg 檔。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-138">with that .jpg file.</span></span>

<span data-ttu-id="8c9bb-139">當您取代 Windows 圖片和傳真檢視器時，應該考慮三個考慮。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-139">There are three considerations you should take into account when you replace the Windows Picture and Fax Viewer.</span></span> <span data-ttu-id="8c9bb-140">這些警告是：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-140">These are:</span></span>

-   [<span data-ttu-id="8c9bb-141">效能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-141">Performance</span></span>](#performance)
-   [<span data-ttu-id="8c9bb-142">功能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-142">Features</span></span>](#features)
-   [<span data-ttu-id="8c9bb-143">格式支援</span><span class="sxs-lookup"><span data-stu-id="8c9bb-143">Format Support</span></span>](#format-support)

### <a name="performance"></a><span data-ttu-id="8c9bb-144">效能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-144">Performance</span></span>

<span data-ttu-id="8c9bb-145">效能的主要考慮是映射載入的速度。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-145">The main consideration with performance is the speed at which images load.</span></span> <span data-ttu-id="8c9bb-146">雖然此處未提供任何效能計量，但您應該嘗試使用符合或提高效能的應用程式來取代 Windows 圖片和傳真檢視器。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-146">While no performance metric is provided here, you should attempt to replace Windows Picture and Fax Viewer with an application that matches or increases the performance.</span></span>

<span data-ttu-id="8c9bb-147">應用程式本身應該很快就會載入。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-147">The application itself should load quickly.</span></span> <span data-ttu-id="8c9bb-148">當應用程式載入時，使用者使用應用程式時所遇到的其中一個主要問題，就是等候時間。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-148">One of the major issues users experience with applications that take over image associations is the wait time while the application loads.</span></span> <span data-ttu-id="8c9bb-149">這通常是因為當使用者只想要查看檔案時，有強大的編輯應用程式負載，而不是在使用者按兩下影像檔時。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-149">This often stems from having a powerful editing application load when they double-click an image file, even when the user simply wants to view the file.</span></span> <span data-ttu-id="8c9bb-150">如果您提供一些選項，讓使用者可以快速地將這些選項帶到應用程式，讓他們只能在需要時編輯影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-150">It is best for the user if you provide options that quickly take them to an application where they can edit the image only when that is their wish.</span></span>

### <a name="features"></a><span data-ttu-id="8c9bb-151">功能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-151">Features</span></span>

<span data-ttu-id="8c9bb-152">當您取代 Windows 圖片和傳真檢視器應用程式時，您的應用程式應該提供一組最基本的功能。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-152">There is a minimal set of features your application should provide when you replace the Windows Picture and Fax Viewer application.</span></span> <span data-ttu-id="8c9bb-153">如下所示：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-153">They are as follows:</span></span>



| <span data-ttu-id="8c9bb-154">功能</span><span class="sxs-lookup"><span data-stu-id="8c9bb-154">Feature</span></span>                            | <span data-ttu-id="8c9bb-155">描述</span><span class="sxs-lookup"><span data-stu-id="8c9bb-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9bb-156">顯示最適合的影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-156">Show image at best fit</span></span>             | <span data-ttu-id="8c9bb-157">如此一來，使用者就可以選擇看到整個影像，並將其調整為最適合應用程式視窗的可見空間大小。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-157">This gives the user the option to see the entire image scaled to the size where i best fits into the viewable space of the application window.</span></span> <span data-ttu-id="8c9bb-158">如此一來，即使縮小，也可以看到整個影像。當映射載入大於可見空間時，這應該是預設設定。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-158">In this way, they can see the entire image, even if it is slightly degraded by zooming out. This should be the default setting whenever an image loads that is larger than the viewable space.</span></span> <span data-ttu-id="8c9bb-159">否則，影像應該會顯示為實際大小。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-159">Otherwise, the image should appear in its actual size.</span></span> <span data-ttu-id="8c9bb-160">例如，64 x 64 圖元影像不應調整為 600 x 600 大小，因為這是應用程式的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-160">For example, a 64 x 64 pixel image should not be scaled to a 600 x 600 size simply because that is the application's window size.</span></span> |
| <span data-ttu-id="8c9bb-161">顯示實際大小的影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-161">Show image at actual size</span></span>          | <span data-ttu-id="8c9bb-162">這可讓使用者選擇以實際的解析度查看整個影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-162">This gives the user the option to see the entire image at its actual resolution.</span></span> <span data-ttu-id="8c9bb-163">這可讓他們以適當的大小加以查看，並平移影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-163">This allows them to view it at its appropriate size and pan about the image.</span></span> <span data-ttu-id="8c9bb-164">除非影像小於應用程式中的可查看空間，否則這不應該是預設視圖。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-164">This should not be the default view unless the image is smaller than the viewable space in the application.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8c9bb-165">放大影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-165">Zoom into image</span></span>                    | <span data-ttu-id="8c9bb-166">這可讓使用者放大影像的一部分，以調查更精細的詳細資料，或只是放大小型影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-166">This enables the user to zoom into a portion of the image to investigate finer details, or simply enlarge a small image.</span></span> <span data-ttu-id="8c9bb-167">這類似于顯示影像的實際大小，但是可讓使用者控制影像的觀看程度。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-167">This is similar to showing the image actual size, but enables the user to control how closely they view the image.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="8c9bb-168">縮小影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-168">Zoom out of image</span></span>                  | <span data-ttu-id="8c9bb-169">這可讓使用者縮小並取得更廣泛的觀點。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-169">This enables the user to zoom out and get a broader view.</span></span> <span data-ttu-id="8c9bb-170">這類似于顯示最適合的影像，但可讓使用者控制其查看影像的距離。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-170">This is similar to showing the image at best fit, but enables the user to control how far back they view the image.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8c9bb-171">下一個影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-171">Next image</span></span>                         | <span data-ttu-id="8c9bb-172">這可讓使用者查看清單中的下一個影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-172">This enables the user to see the next image in the list.</span></span> <span data-ttu-id="8c9bb-173">這份清單可以是目前資料夾中的所有影像，或是使用者選取做為多重選取作業一部分的所有影像;也就是說，當他或她按一下並拖曳來反白顯示影像，或按住控制項按鈕並按一下個別檔案時。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-173">This list can be all the images in the current folder or all the images the user selects as part of a multiselect operation; that is, when he or she clicks and drags to highlight images or holds down the control button and clicks individual files.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="8c9bb-174">上一個影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-174">Previous image</span></span>                     | <span data-ttu-id="8c9bb-175">這可讓使用者查看清單中的上一個影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-175">This enables the user to view the previous image in the list.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8c9bb-176">順時針旋轉90度</span><span class="sxs-lookup"><span data-stu-id="8c9bb-176">Rotate clockwise 90 degrees</span></span>        | <span data-ttu-id="8c9bb-177">如此一來，使用者就能依季順時針旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-177">This enables the user to rotate the image clockwise by quarters.</span></span> <span data-ttu-id="8c9bb-178">Windows XP 會在旋轉時自動儲存映射，以降低影像品質的損失。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-178">Windows XP automatically saves the image when it rotates it to reduce the loss of image quality.</span></span> <span data-ttu-id="8c9bb-179">應用程式也可以旋轉較小的遞增，但90度則是數位相片最常見的旋轉標準。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-179">The application can also rotate smaller increments, but 90 degrees is the standard as the most common rotation for digital pictures.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="8c9bb-180">逆時針旋轉90度</span><span class="sxs-lookup"><span data-stu-id="8c9bb-180">Rotate counterclockwise 90 degrees</span></span> | <span data-ttu-id="8c9bb-181">這可讓使用者以季為依據的季旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-181">This enables the user to rotate the image counterclockwise by quarters.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8c9bb-182">列印</span><span class="sxs-lookup"><span data-stu-id="8c9bb-182">Print</span></span>                              | <span data-ttu-id="8c9bb-183">這可讓使用者列印目前顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-183">This enables the user to print the image that currently appears.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8c9bb-184">另存新檔</span><span class="sxs-lookup"><span data-stu-id="8c9bb-184">Save As</span></span>                            | <span data-ttu-id="8c9bb-185">這可讓使用者將影像儲存至指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-185">This enables the user to save the image to a specified folder.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8c9bb-186">刪除影像</span><span class="sxs-lookup"><span data-stu-id="8c9bb-186">Delete image</span></span>                       | <span data-ttu-id="8c9bb-187">這可讓使用者刪除影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-187">This enables the user to delete the image.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8c9bb-188">Help</span><span class="sxs-lookup"><span data-stu-id="8c9bb-188">Help</span></span>                               | <span data-ttu-id="8c9bb-189">這會為使用者提供有關使用「觀看」應用程式的說明文件。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-189">This provides the user with help documentation concerned with the use of the viewing application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8c9bb-190">屬性</span><span class="sxs-lookup"><span data-stu-id="8c9bb-190">Properties</span></span>                         | <span data-ttu-id="8c9bb-191">這可讓使用者查看或編輯影像的屬性，通常是交換影像檔案 (每個影像中所儲存的 EXIF) 資訊。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-191">This enables the user to view or edit the properties of the image, typically the Exchangeable Image File (EXIF) information stored in each image.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8c9bb-192">編輯</span><span class="sxs-lookup"><span data-stu-id="8c9bb-192">Edit</span></span>                               | <span data-ttu-id="8c9bb-193">這可讓使用者啟動其慣用的編輯程式，其已針對影像上的編輯動詞註冊。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-193">This enables the user to launch their preferred editing program registered for the Edit verb on the image.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a><span data-ttu-id="8c9bb-194">格式支援</span><span class="sxs-lookup"><span data-stu-id="8c9bb-194">Format Support</span></span>

<span data-ttu-id="8c9bb-195">由於應用程式很難支援所有不同的映射，因此建議應用程式使用 Windows GDI + 支援影像格式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-195">Because it is difficult for an application to support all different images, it is recommended that the application use Windows GDI+ to support image formats.</span></span> <span data-ttu-id="8c9bb-196">但是，如果您選擇不使用 GDI +，您的應用程式應該只接管已經過測試且已知可以運作的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-196">However, if you choose not to use GDI+, your application should take over only those file associations for which it has been tested and is known to work.</span></span> <span data-ttu-id="8c9bb-197">然後，如果使用者需要查看您未處理的格式，Windows 圖片和傳真檢視器仍然可以提供存取權。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-197">Then, if the user needs to view a format that you do not handle, Windows Picture and Fax Viewer can still provide access.</span></span>

<span data-ttu-id="8c9bb-198">例如，[Windows 圖片及傳真檢視器] 提供一些工具來編輯 tiff 影像中的注釋。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-198">For example, Windows Picture and Fax Viewer provides a number of tools for editing annotations in .tiff images.</span></span> <span data-ttu-id="8c9bb-199">除非您的應用程式中有重複的這項功能，否則您不應該註冊應用程式來處理 tiff 影像。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-199">Unless this functionality is duplicated in your application, you should not register your application to handle .tiff images.</span></span> <span data-ttu-id="8c9bb-200">駕駛準則應確保使用者不會失去任何功能。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-200">The driving principle should be to ensure that the user loses no functionality whatsoever.</span></span>

## <a name="registering-for-the-preview-verb"></a><span data-ttu-id="8c9bb-201">註冊預覽動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-201">Registering for the Preview Verb</span></span>

<span data-ttu-id="8c9bb-202">註冊應用程式以處理預覽動詞命令相當簡單。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-202">Registering an application to handle the Preview verb is fairly simple.</span></span> <span data-ttu-id="8c9bb-203">在登錄中找出應用程式的下列值，其中應用程式會代表應用程式的檔案關聯機碼名稱 (如需詳細資料，請參閱 [預設程式](/windows/desktop/shell/default-programs)) ：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-203">Locate the application's following value in the registry, where Application.Jpeg represents the name of the application's file association key (see [Default Programs](/windows/desktop/shell/default-programs) for more details):</span></span>

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

<span data-ttu-id="8c9bb-204">將 **開啟** 的子機碼名稱變更為「預覽」，如下所示。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-204">Change the name of the **open** subkey to "preview" as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

<span data-ttu-id="8c9bb-205">這會註冊應用程式，並使其成為 .jpg 檔案預覽動詞命令的預設應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-205">This registers the application and makes it the default application for the Preview verb for a .jpg file.</span></span> <span data-ttu-id="8c9bb-206">也需要下列各項。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-206">The following is also required.</span></span>

<span data-ttu-id="8c9bb-207">**HKEY \_類別 \_ 根目錄** \\ **.jpg** \( 預設) = 應用程式. Jpeg</span><span class="sxs-lookup"><span data-stu-id="8c9bb-207">**HKEY\_CLASSES\_ROOT**\\ **.jpg**\(Default) = Application.Jpeg</span></span>

## <a name="registering-for-the-edit-verb"></a><span data-ttu-id="8c9bb-208">註冊編輯動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-208">Registering for the Edit Verb</span></span>

<span data-ttu-id="8c9bb-209">這會為編輯動詞註冊應用程式，並使其成為編輯影像的新預設應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-209">This registers an application for the Edit Verb and makes it the new default application for editing an image.</span></span> <span data-ttu-id="8c9bb-210">註冊的應用程式應該在安裝時接管現有預設應用程式的編輯功能，並在卸載時將其安裝回處理常式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-210">The registered application should take over the editing capability of the existing default application at the install time and install it back as the handler at the time of uninstall.</span></span> <span data-ttu-id="8c9bb-211">這可以藉由在關聯清單中比預設應用程式更低的方式註冊新的應用程式來達成。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-211">This can be achieved by registering the new application lower in the association list than the default application.</span></span> <span data-ttu-id="8c9bb-212">預設的應用程式會在這裡註冊：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-212">The default application is registered here:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

<span data-ttu-id="8c9bb-213">新的應用程式應該在此註冊：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-213">New application should register here:</span></span>

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a><span data-ttu-id="8c9bb-214">註冊投影片動詞</span><span class="sxs-lookup"><span data-stu-id="8c9bb-214">Registering for the Slideshow Verb</span></span>

<span data-ttu-id="8c9bb-215">在 Windows Vista 中，應用程式也可以註冊投影 **片動詞。**</span><span class="sxs-lookup"><span data-stu-id="8c9bb-215">As of Windows Vista, an application can also register the **slideshow** verb.</span></span> <span data-ttu-id="8c9bb-216">執行投影片節目的應用程式可以註冊在選擇投影片動詞時叫用。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-216">Applications that implement a slide show can register to be invoked when the Slideshow verb is chosen.</span></span> <span data-ttu-id="8c9bb-217">此註冊的完成方式與上述預覽動詞命令的方式完全相同。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-217">This registration is accomplished in exactly the same fashion as explained for the preview verb above.</span></span> <span data-ttu-id="8c9bb-218">強烈建議應用程式執行動詞的 DropTarget 形式。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-218">It is strongly recommended that applications implement the DropTarget form of the verb.</span></span> <span data-ttu-id="8c9bb-219">如此一來，就可以將一組完整的專案傳遞給它們。</span><span class="sxs-lookup"><span data-stu-id="8c9bb-219">In that way, they can be passed a complete set of items.</span></span> <span data-ttu-id="8c9bb-220">DropTarget 的執行已註冊，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8c9bb-220">The DropTarget implementation is registered as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a><span data-ttu-id="8c9bb-221">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c9bb-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c9bb-222">檔案關聯簡介</span><span class="sxs-lookup"><span data-stu-id="8c9bb-222">Introduction to File Associations</span></span>](/windows/desktop/shell/fa-intro)
</dt> <dt>

[<span data-ttu-id="8c9bb-223">關於 GDI +</span><span class="sxs-lookup"><span data-stu-id="8c9bb-223">About GDI+</span></span>](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 