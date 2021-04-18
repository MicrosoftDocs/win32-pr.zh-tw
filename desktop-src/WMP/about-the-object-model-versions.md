---
title: 關於物件模型版本
description: 關於物件模型版本
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player，版本
- Windows Media Player 物件模型，版本
- 物件模型，版本
- Windows Media Player ActiveX 控制項，物件模型的版本
- ActiveX 控制項，物件模型的版本
- Windows Media Player 的行動 ActiveX 控制項，物件模型的版本
- Windows Media Player 行動版，物件模型的版本
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104374780"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="d55b4-111">關於物件模型版本</span><span class="sxs-lookup"><span data-stu-id="d55b4-111">About the Object Model Versions</span></span>

<span data-ttu-id="d55b4-112">Windows Media Player 7.0 引進了新的物件模型。</span><span class="sxs-lookup"><span data-stu-id="d55b4-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="d55b4-113">此物件模型已透過 Windows Media Player 7.1、適用于 Windows XP 的 Windows Media Player、Windows Media Player 9 系列、Windows Media Player 10、Windows Media Player 11 和 Windows Media Player 12 進行擴充。</span><span class="sxs-lookup"><span data-stu-id="d55b4-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="d55b4-114">物件模型參考中的每個主題都包含一個需求區段，以詳細說明個別屬性、方法或事件的最小需求。</span><span class="sxs-lookup"><span data-stu-id="d55b4-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="d55b4-115">下列清單詳細說明自7.0 版以來針對每個版本新增的新物件、方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="d55b4-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="d55b4-116">這些清單也包含新的 c + + 介面、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="d55b4-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="d55b4-117">當新的或更新的介面也公開為物件時，只會列出物件。</span><span class="sxs-lookup"><span data-stu-id="d55b4-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="d55b4-118">若要找出介面，請參閱 [c + + 的物件模型參考](object-model-reference-for-c.md)。</span><span class="sxs-lookup"><span data-stu-id="d55b4-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="d55b4-119">通常，您只需要將 IWMP 前置詞加入至物件名稱。</span><span class="sxs-lookup"><span data-stu-id="d55b4-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="d55b4-120">如果新介面擴充了現有介面，您可能需要尋找最新的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d55b4-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="d55b4-121">例如，Windows Media Player 9 系列引進了可從 [**Settings**](settings-object.md) 物件取得的新屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="d55b4-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="d55b4-122">在 c + + 中，這些可透過 [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) 介面取得，而這個介面會擴充 [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)。</span><span class="sxs-lookup"><span data-stu-id="d55b4-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="d55b4-123">已針對 Windows Media Player 7.1 新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="d55b4-124">**StretchToFit 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="d55b4-125">針對 Windows XP 的 Windows Media Player 新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="d55b4-126">**Controls 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="d55b4-127">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="d55b4-128">**Media. error 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="d55b4-129">**DomainChange 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="d55b4-130">**MediaError 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="d55b4-131">**OpenPlaylistSwitch 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="d55b4-132">**WindowlessVideo 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="d55b4-133">針對 Windows Media Player 9 系列新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="d55b4-134">**ClosedCaption. getSAMILangID 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="d55b4-135">**ClosedCaption. getSAMILangName 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="d55b4-136">**ClosedCaption. getSAMIStyleName 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="d55b4-137">**ClosedCaption. SAMILangCount 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="d55b4-138">**ClosedCaption. SAMIStyleCount 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="d55b4-139">**AudioLanguageCount 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="d55b4-140">**CurrentAudioLanguage 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="d55b4-141">**CurrentAudioLanguageIndex 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="d55b4-142">**CurrentPositionTimecode 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="d55b4-143">**GetAudioLanguageDescription 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="d55b4-144">**GetAudioLanguageID 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="d55b4-145">**GetLanguageName 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="d55b4-146">**ErrorItem。 condition 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="d55b4-147">**AppColorLight 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="d55b4-148">**OnColorChange 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="d55b4-149">**External. version 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="d55b4-150">**IWMPEvents：:P layerDockedStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="d55b4-151">**IWMPEvents：:P layerReconnect 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="d55b4-152">**IWMPEvents：： SwitchedToControl 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="d55b4-153">**IWMPEvents：： SwitchedToPlayerApplication 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="d55b4-154">**IWMPPlayerServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="d55b4-155">**IWMPRemoteMediaServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="d55b4-156">**IWMPSkinManager 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="d55b4-157">**GetAttributeCountByType 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="d55b4-158">**GetItemInfoByType 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="d55b4-159">**MetadataPicture 物件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="d55b4-160">**MetadataText 物件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="d55b4-161">**AudioLanguageChange 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="d55b4-162">**IsRemote 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="d55b4-163">**MediaCollectionAttributeStringChanged 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="d55b4-164">**NewMedia 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   <span data-ttu-id="d55b4-165">[**[] 方法**](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="d55b4-165">[**Player.newPlaylist Method**](player-newplaylist.md)</span></span>
-   [<span data-ttu-id="d55b4-166">**OpenPlayer 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="d55b4-167">**PlayerApplication 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="d55b4-168">**StatusChange 事件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="d55b4-169">**PlayerApplication 物件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="d55b4-170">**DefaultAudioLanguage 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="d55b4-171">**MediaAccessRights 屬性**</span><span class="sxs-lookup"><span data-stu-id="d55b4-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="d55b4-172">**RequestMediaAccessRights 方法**</span><span class="sxs-lookup"><span data-stu-id="d55b4-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="d55b4-173">針對 Windows Media Player 10 新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="d55b4-174">**IWMPGraphCreation 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="d55b4-175">**IWMPPlayerServices2 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="d55b4-176">**IWMPSyncDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="d55b4-177">**IWMPSyncServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="d55b4-178">**WMPDeviceStatus 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="d55b4-179">**WMPSyncState 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="d55b4-180">針對 Windows Media Player 11 新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="d55b4-181">**IWMPCdromBurn 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="d55b4-182">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="d55b4-183">**IWMPCdromRip 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="d55b4-184">**IWMPCdromRip 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="d55b4-185">**IWMPEvents3 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="d55b4-186">**IWMPFolderMonitorServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="d55b4-187">**IWMPLibrary 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="d55b4-188">**IWMPLibrary 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="d55b4-189">**IWMPLibraryServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="d55b4-190">**IWMPLibraryServices 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="d55b4-191">**IWMPLibrarySharingServices 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="d55b4-192">**IWMPMediaCollection2 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="d55b4-193">**IWMPMediaCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="d55b4-194">**IWMPQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="d55b4-195">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="d55b4-196">**IWMPRenderConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="d55b4-197">**IWMPStringCollection2 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="d55b4-198">**IWMPStringCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d55b4-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="d55b4-199">**IWMPSyncDevice2 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="d55b4-200">**IWMPVideoRenderConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="d55b4-201">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="d55b4-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="d55b4-202">**WMPBurnFormat 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="d55b4-203">**WMPBurnState 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="d55b4-204">**WMPLibraryType 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="d55b4-205">**WMPRipState 列舉**</span><span class="sxs-lookup"><span data-stu-id="d55b4-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="d55b4-206">針對 Windows Media Player 12 新增</span><span class="sxs-lookup"><span data-stu-id="d55b4-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="d55b4-207">**IWMPAudioRenderConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="d55b4-208">**IWMPEvents4 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="d55b4-209">**IWMPLibrary2 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="d55b4-210">**IWMPSyncDevice3 介面**</span><span class="sxs-lookup"><span data-stu-id="d55b4-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="d55b4-211">相關主題</span><span class="sxs-lookup"><span data-stu-id="d55b4-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d55b4-212">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="d55b4-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="d55b4-213">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="d55b4-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




