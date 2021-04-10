---
title: Windows Media Player 12的新功能
description: 本主題列出 Windows Media Player 12 中的新功能。
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player，新功能
- Windows Media Player，新功能
- 軟體發展工具組 (SDK) ，Windows Media Player 12
- SDK (軟體發展工具組) ，Windows Media Player 12
- 檔，Windows Media Player 12 SDK
- 新功能，Windows Media Player 12
- 新功能，Windows Media Player 12
- 介面，Windows Media Player 12 中的新功能
- Windows Media Player 12 中的屬性、新功能
- 中繼資料，Windows Media Player 12 中的新功能
- 列舉，Windows Media Player 12 中的新功能
- Windows Media Player 12 中的旗標、新功能
- 介面，Windows Media Player 12 中已淘汰
- 方法，在 Windows Media Player 11 中已被取代，不是12
- 版本的 Windows Media Player，第12版中的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104092597"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="fb2d0-118">Windows Media Player 12的新功能</span><span class="sxs-lookup"><span data-stu-id="fb2d0-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="fb2d0-119">本主題列出 Windows Media Player 12 中的新功能。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="fb2d0-120">新介面</span><span class="sxs-lookup"><span data-stu-id="fb2d0-120">New Interfaces</span></span>

-   [<span data-ttu-id="fb2d0-121">**IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="fb2d0-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="fb2d0-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="fb2d0-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="fb2d0-125">新屬性</span><span class="sxs-lookup"><span data-stu-id="fb2d0-125">New Attributes</span></span>

<span data-ttu-id="fb2d0-126">下列媒體專案的新屬性可透過 [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) 和 [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) 介面取得。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="fb2d0-127">**AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="fb2d0-128">**AlternateSourceURL**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="fb2d0-129">**DLNASourceURI**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="fb2d0-130">**DLNAServerUDN**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="fb2d0-131">**DTCPIPHost**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="fb2d0-132">**DTCPIPPort**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="fb2d0-133">**LibraryID**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="fb2d0-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="fb2d0-135">新的裝置中繼資料</span><span class="sxs-lookup"><span data-stu-id="fb2d0-135">New Device Metadata</span></span>

<span data-ttu-id="fb2d0-136">您可以藉由呼叫 [**IWMPSyncDevice：： getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)來取出下列新的裝置中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="fb2d0-137">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="fb2d0-138">**SkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="fb2d0-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-139">**SyncFilter**</span></span>

<span data-ttu-id="fb2d0-140">您可以藉由呼叫 [**IWMPSyncDevice2：： setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)來設定下列新的裝置中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="fb2d0-141">**AutoSyncDefaultRules**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="fb2d0-142">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="fb2d0-143">**IncludeSkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="fb2d0-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-144">**SyncFilter**</span></span>
-   <span data-ttu-id="fb2d0-145">**SyncOnConnect**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="fb2d0-146">新的列舉成員</span><span class="sxs-lookup"><span data-stu-id="fb2d0-146">New Enumeration Member</span></span>

<span data-ttu-id="fb2d0-147">[**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)列舉具有下列的新成員。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="fb2d0-148">**wmpssEstimating**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="fb2d0-149">新增旗標</span><span class="sxs-lookup"><span data-stu-id="fb2d0-149">New Flag</span></span>

<span data-ttu-id="fb2d0-150">[**IWMPGraphCreation：： GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags)方法支援下列新旗標。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="fb2d0-151">**WMPGC \_ 旗標 \_ 使用 \_ 自訂 \_ 圖形**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="fb2d0-152">已淘汰的介面</span><span class="sxs-lookup"><span data-stu-id="fb2d0-152">Deprecated Interface</span></span>

<span data-ttu-id="fb2d0-153">下列介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="fb2d0-154">**IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="fb2d0-155">不再被取代的方法</span><span class="sxs-lookup"><span data-stu-id="fb2d0-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="fb2d0-156">下列方法已在 Windows Media Player 11 SDK 中淘汰，但不再被取代。</span><span class="sxs-lookup"><span data-stu-id="fb2d0-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="fb2d0-157">**IWMPGraphCreation::GraphCreationPreRender**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="fb2d0-158">**IWMPGraphCreation::GraphCreationPostRender**</span><span class="sxs-lookup"><span data-stu-id="fb2d0-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="fb2d0-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb2d0-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb2d0-160">關於 Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="fb2d0-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




