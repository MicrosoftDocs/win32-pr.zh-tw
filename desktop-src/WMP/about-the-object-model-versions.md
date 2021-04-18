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
# <a name="about-the-object-model-versions"></a>關於物件模型版本

Windows Media Player 7.0 引進了新的物件模型。 此物件模型已透過 Windows Media Player 7.1、適用于 Windows XP 的 Windows Media Player、Windows Media Player 9 系列、Windows Media Player 10、Windows Media Player 11 和 Windows Media Player 12 進行擴充。 物件模型參考中的每個主題都包含一個需求區段，以詳細說明個別屬性、方法或事件的最小需求。 下列清單詳細說明自7.0 版以來針對每個版本新增的新物件、方法、屬性和事件。 這些清單也包含新的 c + + 介面、方法和事件。

當新的或更新的介面也公開為物件時，只會列出物件。 若要找出介面，請參閱 [c + + 的物件模型參考](object-model-reference-for-c.md)。 通常，您只需要將 IWMP 前置詞加入至物件名稱。 如果新介面擴充了現有介面，您可能需要尋找最新的版本號碼。 例如，Windows Media Player 9 系列引進了可從 [**Settings**](settings-object.md) 物件取得的新屬性和方法。 在 c + + 中，這些可透過 [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) 介面取得，而這個介面會擴充 [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)。

## <a name="added-for-windows-media-player-71"></a>已針對 Windows Media Player 7.1 新增

-   [**StretchToFit 屬性**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>針對 Windows XP 的 Windows Media Player 新增

-   [**Controls 方法**](controls-step.md)
-   [**DVD 物件**](dvd-object.md)
-   [**Media. error 屬性**](media-error.md)
-   [**DomainChange 事件**](player-player-domainchange.md)
-   [**MediaError 事件**](player-player-mediaerror.md)
-   [**OpenPlaylistSwitch 事件**](player-player-openplaylistswitch.md)
-   [**WindowlessVideo 屬性**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>針對 Windows Media Player 9 系列新增

-   [**ClosedCaption. getSAMILangID 方法**](closedcaption-getsamilangid.md)
-   [**ClosedCaption. getSAMILangName 方法**](closedcaption-getsamilangname.md)
-   [**ClosedCaption. getSAMIStyleName 方法**](closedcaption-getsamistylename.md)
-   [**ClosedCaption. SAMILangCount 屬性**](closedcaption-samilangcount.md)
-   [**ClosedCaption. SAMIStyleCount 屬性**](closedcaption-samistylecount.md)
-   [**AudioLanguageCount 屬性**](controls-audiolanguagecount.md)
-   [**CurrentAudioLanguage 屬性**](controls-currentaudiolanguage.md)
-   [**CurrentAudioLanguageIndex 屬性**](controls-currentaudiolanguageindex.md)
-   [**CurrentPositionTimecode 屬性**](controls-currentpositiontimecode.md)
-   [**GetAudioLanguageDescription 方法**](controls-getaudiolanguagedescription.md)
-   [**GetAudioLanguageID 方法**](controls-getaudiolanguageid.md)
-   [**GetLanguageName 方法**](controls-getlanguagename.md)
-   [**ErrorItem。 condition 屬性**](erroritem-condition.md)
-   [**AppColorLight 屬性**](external-appcolorlight.md)
-   [**OnColorChange 事件**](external-oncolorchange-event.md)
-   [**External. version 屬性**](external-version.md)
-   [**IWMPEvents：:P layerDockedStateChange 事件**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents：:P layerReconnect 事件**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**IWMPEvents：： SwitchedToControl 事件**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**IWMPEvents：： SwitchedToPlayerApplication 事件**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**IWMPPlayerServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**IWMPRemoteMediaServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**IWMPSkinManager 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**GetAttributeCountByType 方法**](media-getattributecountbytype.md)
-   [**GetItemInfoByType 方法**](media-getiteminfobytype.md)
-   [**MetadataPicture 物件**](metadatapicture-object.md)
-   [**MetadataText 物件**](metadatatext-object.md)
-   [**AudioLanguageChange 事件**](player-player-audiolanguagechange.md)
-   [**IsRemote 屬性**](player-isremote.md)
-   [**MediaCollectionAttributeStringChanged 事件**](player-player-mediacollectionattributestringchanged.md)
-   [**NewMedia 方法**](player-newmedia.md)
-   [**[] 方法**](player-newplaylist.md)
-   [**OpenPlayer 方法**](player-openplayer.md)
-   [**PlayerApplication 屬性**](player-playerapplication.md)
-   [**StatusChange 事件**](player-player-statuschange.md)
-   [**PlayerApplication 物件**](playerapplication-object.md)
-   [**DefaultAudioLanguage 屬性**](settings-defaultaudiolanguage.md)
-   [**MediaAccessRights 屬性**](settings-mediaaccessrights.md)
-   [**RequestMediaAccessRights 方法**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>針對 Windows Media Player 10 新增

-   [**IWMPGraphCreation 介面**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**IWMPPlayerServices2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**IWMPSyncDevice 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**IWMPSyncServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**WMPDeviceStatus 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**WMPSyncState 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>針對 Windows Media Player 11 新增

-   [**IWMPCdromBurn 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
-   [**IWMPCdromRip 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**IWMPCdromRip 介面 (VB 和 c # )**](iwmpcdromrip--vb-and-c.md)
-   [**IWMPEvents3 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**IWMPFolderMonitorServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPLibrary 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**IWMPLibrary 介面 (VB 和 c # )**](iwmplibrary--vb-and-c.md)
-   [**IWMPLibraryServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**IWMPLibraryServices 介面 (VB 和 c # )**](iwmplibraryservices--vb-and-c.md)
-   [**IWMPLibrarySharingServices 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**IWMPMediaCollection2 介面 (VB 和 c # )**](iwmpmediacollection2--vb-and-c.md)
-   [**IWMPQuery 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**IWMPQuery 介面 (VB 和 c # )**](iwmpquery--vb-and-c.md)
-   [**IWMPRenderConfig 介面**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**IWMPStringCollection2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**IWMPStringCollection2 介面 (VB 和 c # )**](iwmpstringcollection2--vb-and-c.md)
-   [**IWMPSyncDevice2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig 介面**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Query 物件**](query-object.md)
-   [**WMPBurnFormat 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**WMPBurnState 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**WMPLibraryType 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**WMPRipState 列舉**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>針對 Windows Media Player 12 新增

-   [**IWMPAudioRenderConfig 介面**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




