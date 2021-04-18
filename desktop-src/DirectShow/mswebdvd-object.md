---
description: MSWebDVD 物件
ms.assetid: 74187af4-a86d-4dec-a1f4-203fda0c6309
title: MSWebDVD 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea98f79c3f0f4b97534ef812e70e5a7417759e25
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510177"
---
# <a name="mswebdvd-object"></a>MSWebDVD 物件

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

> [!Note]  
> 此 API 即將淘汰。 如需有關在 DirectShow 播放和流覽 DVD 的詳細資訊，請參閱 [Dvd 應用程式](dvd-applications.md)。

 

MSWebDVD 物件的方法、屬性和事件可讓應用程式控制 DVD-Video 流覽和播放的所有層面，以及從光碟取出資訊。MSWebDVD 物件不會執行實際的流覽工作;相反地，它會將命令傳遞至 [DVD](dvd-navigator-filter.md) 導覽器篩選器，這是可讀取 DVD-Video 光碟的 Microsoft® DirectShow®元件。

MSWebDVD 方法和屬性會作用於 DVD 導覽器的目前狀態或光碟上的資訊，或兩者。 若要在登錄中儲存和取出各種類型的應用程式特定資訊，例如家長監護和 default language 的使用者喜好設定，請使用 [MSDVDAdm](msdvdadm-object.md) 物件的方法。 您可以使用 [**DVDAdm**](dvdadm-property.md) 屬性來存取這個物件。

> [!Note]  
> 從 DirectX 9.0 b，物件只會在信任的區域中載入。 它不會載入不受信任的區域。

 

**依類別分類的方法和屬性**



| 播放                                                                          |                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanStep**](canstep-method.md)                                                 | 判斷本機系統上的 MPEG-2 解碼器是否可以依照指定的方向執行框架逐步執行。                                                                              |
| [**Eject**](eject-method.md)                                                     | 將光碟從或插入磁片磁碟機。                                                                                                                                            |
| [**FramesPerSecond**](framespersecond-property.md)                               | 抓取目前 DVD 標題的影片畫面播放速率。                                                                                                                                   |
| [**暫停**](pause-method.md)                                                     | 暫停目前位置的播放。                                                                                                                                                    |
| [**播放**](play-method.md)                                                       | 播放目前的 DVD 標題。                                                                                                                                                                |
| [**PlayAtTime**](playattime-method.md)                                           | 在指定的時間開始在目前的標題中播放。                                                                                                                                 |
| [**PlayAtTimeInTitle**](playattimeintitle-method.md)                             | 在指定的標題內開始播放指定的時間。                                                                                                                           |
| [**PlayBackwards**](playbackwards-method.md)                                     | 以指定的速度從目前位置開始向前播放。                                                                                                                  |
| [**PlayChapter**](playchapter-method.md)                                         | 從目前標題中的指定章節開始播放。                                                                                                                            |
| [**PlayChapterInTitle**](playchapterintitle-method.md)                           | 在指定的標題中播放指定的章節。                                                                                                                                         |
| [**PlayChaptersAutoStop**](playchaptersautostop-method.md)                       | 針對指定的標題，以指定的章節開始播放指定的章節數。                                                                                      |
| [**PlayForwards**](playforwards-method.md)                                       | 從目前位置開始，以指定的速度向前播放。                                                                                                                   |
| [**PlayNextChapter**](playnextchapter-method.md)                                 | 開始從目前標題的下一章開始播放。                                                                                                                                 |
| [**PlayPeriodInTitleAutoStop**](playperiodintitleautostop-method.md)             | 在指定的時間點開始播放指定的標題，直到指定的停止時間。                                                                                                 |
| [**PlayPrevChapter**](playprevchapter-method.md)                                 | 開始在目前的標題中播放上一章。                                                                                                                             |
| [**PlayTitle**](playtitle-method.md)                                             | 開始在指定的標題開頭播放。                                                                                                                                    |
| [**ReplayChapter**](replaychapter-method.md)                                     | 開始在目前章節的開頭播放。                                                                                                                                    |
| [**繼續**](resume-method.md)                                                   | 在顯示功能表之後繼續播放。                                                                                                                                           |
| [**StillOff**](stilloff-method.md)                                               | 繼續播放，取消仍處於模式。                                                                                                                                                     |
| [**步驟**](step-method.md)                                                       | 將 DVD-Video 資料流程前移指定的畫面格數目。                                                                                                                            |
| [**停止**](stop-method.md)                                                       | 停止播放。                                                                                                                                                                             |
| 功能表                                                                             |                                                                                                                                                                                             |
| [**ActivateAtPosition**](activateatposition-method.md)                           | 啟用指定位置的功能表按鈕。                                                                                                                                        |
| [**ActivateButton**](activatebutton-method.md)                                   | 啟用選取的功能表按鈕。                                                                                                                                                         |
| [**ButtonsAvailable**](buttonsavailable-property.md)                             | 抓取目前功能表上的總按鈕數。                                                                                                                                  |
| [**CurrentButton**](currentbutton-property.md)                                   | 抓取選取的按鈕數目。                                                                                                                                                |
| [**DefaultMenuLanguage**](defaultmenulanguage-property.md)                       | 從光碟取出預設的功能表語言。                                                                                                                                          |
| [**GetButtonAtPosition**](getbuttonatposition-method.md)                         | 抓取指定座標的按鈕數目，而不選取或啟用它。                                                                                         |
| [**GetButtonRect**](getbuttonrect-method.md)                                     | 抓取視窗座標中指定之按鈕的矩形。                                                                                                                    |
| [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                             | 如果功能表是最上層功能表，則會從子功能表傳回顯示，或傳回目前的標題。                                                                                 |
| [**SelectAndActivateButton**](selectandactivatebutton-method.md)                 | 選取並啟用指定的按鈕。                                                                                                                                                 |
| [**SelectAtPosition**](selectatposition-method.md)                               | 選取位於指定位置的功能表按鈕。                                                                                                                                          |
| [**SelectLeftButton**](selectleftbutton-method.md)                               | 從顯示的功能表中選取左方向按鈕。                                                                                                                                |
| [**SelectLowerButton**](selectlowerbutton-method.md)                             | 從顯示的功能表中選取下方的方向按鈕。                                                                                                                               |
| [**SelectRightButton**](selectrightbutton-method.md)                             | 從顯示的功能表中選取正確的方向按鈕。                                                                                                                               |
| [**SelectUpperButton**](selectupperbutton-method.md)                             | 從顯示的功能表中選取上方方向按鈕。                                                                                                                               |
| [**ShowMenu**](showmenu-method.md)                                               | 在螢幕上顯示指定的功能表。                                                                                                                                                  |
| 音訊串流                                                                      |                                                                                                                                                                                             |
| [**AudioStreamsAvailable**](audiostreamsavailable-property.md)                   | 抓取目前標題中可用的音訊資料流程數目。                                                                                                                       |
| [**餘額**](balance-property.md)                                               | 設定或抓取音訊串流輸出的喇叭餘額。                                                                                                                          |
| [**CurrentAudioStream**](currentaudiostream-property.md)                         | 設定或抓取啟用的音訊資料流程數目。                                                                                                                                   |
| [**DefaultAudioLanguage**](defaultaudiolanguage-property.md)                     | 從光碟取出預設音訊語言。                                                                                                                                         |
| [**DefaultAudioLanguageExt**](defaultaudiolanguageext-property.md)               | 從光碟取出預設的音訊語言延伸模組。                                                                                                                               |
| [**GetAudioLanguage**](getaudiolanguage-method.md)                               | 抓取字串，指出指定的音訊資料流程上有哪些語言可用。                                                                                                    |
| [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md)                       | 抓取值，指出目前的標題中是否已啟用指定的音訊資料流程。                                                                                            |
| [**Mute**](mute-property.md)                                                     | 開啟或關閉音訊資料流程輸出。                                                                                                                                                    |
| [**SelectDefaultAudioLanguage**](selectdefaultaudiolanguage-method.md)           | 設定 DVD 導覽器中目前的預設音訊語言。                                                                                                                               |
| [**磁碟區**](volume-property.md)                                                 | 設定或抓取音訊音量層級。                                                                                                                                                   |
| 子圖片資料流程                                                                 |                                                                                                                                                                                             |
| [**CurrentSubpictureStream**](currentsubpicturestream-property.md)               | 抓取選取的子圖片資料流程。                                                                                                                                                   |
| [**DefaultSubpictureLanguage**](defaultsubpicturelanguage-property.md)           | 從光碟取出預設的子圖片語言。                                                                                                                                    |
| [**DefaultSubpictureLanguageExt**](defaultsubpicturelanguageext-property.md)     | 從光碟取出預設的子圖片語言延伸模組。                                                                                                                          |
| [**GetSubpictureLanguage**](getsubpicturelanguage-method.md)                     | 抓取指定之子圖片資料流程的語言。                                                                                                                                 |
| [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md)             | 抓取值，指出目前的標題中是否已啟用指定的子圖片資料流程。                                                                                       |
| [**PreferredSubpictureStream**](preferredsubpicturestream-property.md)           | 為目前的觀看會話設定或抓取使用者慣用的子圖片資料流程。                                                                                                   |
| [**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md) | 在 DVD 導覽器中設定目前的預設子圖片語言。                                                                                                                          |
| [**SubpictureOn**](subpictureon-property.md)                                     | 設定或抓取 (on 或 off) 的目前子圖片狀態。                                                                                                                                 |
| [**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)         | 抓取目前標題中可用的子圖片資料流程數目。                                                                                                                  |
| 影片矩形                                                                   |                                                                                                                                                                                             |
| [**AspectRatio**](aspectratio-property.md)                                       | 抓取目前影片資料流程的外觀比例，如光碟上所撰寫。                                                                                                             |
| [**顏色**](backcolor-property.md)                                           | 當原生影片的長寬比與物件的顯示區域不同時，設定或抓取在影片矩形邊緣周圍出現的橫條色彩。 |
| [**捕獲**](capture-method.md)                                                 | 當 MSWebDVD 物件處於無視窗模式時，從影片框架捕捉靜止影像。                                                                                                 |
| [**FullScreenMode**](fullscreenmode-property.md)                                 | 設定或抓取值，指出顯示器是否處於全螢幕模式。                                                                                                            |
| [**GetClipVideoRect**](getclipvideorect-method.md)                               | 抓取為影片顯示所定義的裁剪矩形。                                                                                                                             |
| [**GetVideoSize**](getvideosize-method.md)                                       | 抓取原生影片維度。                                                                                                                                                      |
| [**SetClipVideoRect**](setclipvideorect-method.md)                               | 設定影片顯示所佔用的裁剪矩形。                                                                                                                                  |
| [**Zoom**](zoom-method.md)                                                       | 放大或縮小影片，並以一組指定的螢幕座標為中心。                                                                                                           |
| 隱藏式字幕功能                                                                 |                                                                                                                                                                                             |
| [**CCActive**](ccactive-property.md)                                             | 設定或抓取隱藏式字幕的目前狀態。                                                                                                                                  |
| [**>colorkey**](colorkey-property.md)                                             | 設定或抓取隱藏式輔助字幕中使用的色彩索引鍵。                                                                                                                                  |
| [**CurrentCCService**](currentccservice-property.md)                             | 設定或抓取目前的封閉標題服務。                                                                                                                                     |
| 角度區塊                                                                      |                                                                                                                                                                                             |
| [**AnglesAvailable**](anglesavailable-property.md)                               | 抓取可用的角度數目。                                                                                                                                                   |
| [**CurrentAngle**](currentangle-property.md)                                     | 設定或抓取角度區塊中的目前角度。                                                                                                                                      |
| 卡拉卡拉音訊                                                                     |                                                                                                                                                                                             |
| [**GetKaraokeChannelAssignment**](getkaraokechannelassignment-method.md)         | 抓取值，指出如何將卡拉卡拉板通道指派給左邊和右邊的喇叭。                                                                                      |
| [**GetKaraokeChannelContent**](getkaraokechannelcontent-method.md)               | 抓取值，這個值表示指定之指定的卡拉的卡拉的卡拉在指定的資料流程中的內容類型。                                                                              |
| [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)     | 設定或抓取輔助的卡拉卡拉板頻道的向左喇叭混合。                                                                                                            |
| 文字字串                                                                      |                                                                                                                                                                                             |
| [**GetDVDTextLanguageLCID**](getdvdtextlanguagelcid-method.md)                   | 抓取指定文字字串區塊 (LCID) 的地區設定識別碼。                                                                                                                 |
| [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md)         | 抓取目前 DVD 目錄中可用的文字語言數目。                                                                                                              |
| [**GetDVDTextNumberOfStrings**](getdvdtextnumberofstrings-method.md)             | 抓取指定語言可用的文字字串數目。                                                                                                                  |
| [**GetDVDTextString**](getdvdtextstring-method.md)                               | 從光碟抓取指定的文字字串。                                                                                                                                          |
| [**GetDVDTextStringType**](getdvdtextstringtype-method.md)                       | 抓取值，指出指定之 DVD 文字字串中所包含的資訊類型。                                                                                        |
| [**GetLangFromLangID**](getlangfromlangid-method.md)                             | 當指定主要語言識別項 (識別碼) 時，會抓取人們可讀取的字串。                                                                                                            |
| 家長管理                                                               |                                                                                                                                                                                             |
| [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)             | 指示 DVD 導覽器接受或拒絕新的暫時家長管理層級。                                                                                                |
| [**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)               | 抓取 DVD 導覽器中所設定的目前國家/地區。                                                                                                                           |
| [**GetPlayerParentalLevel**](getplayerparentallevel-method.md)                   | 抓取 DVD 導覽器中所設定的家長管理層級。                                                                                                                           |
| [**GetTitleParentalLevels**](gettitleparentallevels-method.md)                   | 針對指定的標題抓取家長管理層級。                                                                                                                           |
| [**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)             | 啟用或停用暫存家長管理層級命令的事件處理。                                                                                                    |
| [**SelectParentalCountry**](selectparentalcountry-method.md)                     | 設定指定的家長/區域以進行後續播放。                                                                                                                         |
| [**SelectParentalLevel**](selectparentallevel-method.md)                         | 設定指定的家長層級，以供後續播放之用。                                                                                                                                  |
| 光碟資訊                                                                  |                                                                                                                                                                                             |
| [**CurrentChapter**](currentchapter-property.md)                                 | 抓取目前現正播放的章節編號。                                                                                                                                      |
| [**CurrentDiscSide**](currentdiscside-property.md)                               | 抓取 DVD 的目前端。                                                                                                                                                      |
| [**CurrentDomain**](currentdomain-property.md)                                   | 抓取 DVD 導覽器所在的 DVD 網域。                                                                                                                                      |
| [**CurrentTime**](currenttime-property.md)                                       | 抓取目前的播放時間。                                                                                                                                                        |
| [**CurrentTitle**](currenttitle-property.md)                                     | 抓取目前現正播放的標題數目。                                                                                                                                        |
| [**CurrentVolume**](currentvolume-property.md)                                   | 抓取目前根目錄的磁片區編號。                                                                                                                                 |
| [**DVDDirectory**](dvddirectory-property.md)                                     | 抓取或設定目前 DVD 磁片區的根目錄。                                                                                                                             |
| [**DVDTimeCode2bstr**](dvdtimecode2bstr-method.md)                               | 抓取表示光碟上目前時間的字串。                                                                                                                                 |
| [**DVDUniqueID**](dvduniqueid-property.md)                                       | 抓取可唯一識別目前 DVD 的系統產生數位。                                                                                                               |
| [**GetNumberOfChapters**](getnumberofchapters-method.md)                         | 抓取指定之標題中的章節數。                                                                                                                                    |
| [**TitlesAvailable**](titlesavailable-property.md)                               | 抓取 DVD 上的可用標題數目。                                                                                                                                        |
| [**TotalTitleTime**](totaltitletime-property.md)                                 | 捕獲目前標題的總播放時間。                                                                                                                                    |
| [**UOPValid**](uopvalid-method.md)                                               | 抓取值，這個值表示指定的使用者作業目前是否有效。                                                                                                   |
| [**VolumesAvailable**](volumesavailable-property.md)                             | 抓取值，指定光碟集中的磁片區數目。                                                                                                                         |
| 物件初始化和控制                                                 |                                                                                                                                                                                             |
| [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md)         | 啟用或停用物件的滑鼠處理功能。                                                                                                                            |
| [**DVDAdm**](dvdadm-property.md)                                                 | 提供 [MSDVDAdm](msdvdadm-object.md) 物件的存取權，其中包含用來儲存應用程式和使用者資訊的方法和屬性。                                                |
| [**EnableResetOnStop**](enableresetonstop-property.md)                           | 設定或抓取值，決定當篩選圖形轉換出停止狀態時，播放將如何繼續。                                                                    |
| [**PlayState**](playstate-property.md)                                           | 抓取目前的播放狀態。                                                                                                                                                           |
| [**ReadyState**](readystate-property.md)                                         | 捕獲 MSWebDVD 物件的 ReadyState。                                                                                                                                            |
| [**RegionChange**](regionchange-method.md)                                       | 顯示 [系統] 對話方塊，可讓使用者變更與 DVD 光碟機相關聯的區域。                                                                                      |
| [**轉譯**](render-method.md)                                                   | 初始化 DVD 篩選圖形。                                                                                                                                                           |
| [**WindowlessActivation**](windowlessactivation-property.md)                     | 在設計階段為視窗化或無視窗模式初始化 MSWebDVD 物件。                                                                                                      |
| 書籤                                                                         |                                                                                                                                                                                             |
| [**DeleteBookmark**](deletebookmark-method.md)                                   | 刪除目前的書簽。                                                                                                                                                               |
| [**RestoreBookmark**](restorebookmark-method.md)                                 | 將 DVD 導覽移至 DVD 上的點（如目前書簽中所指定），並還原所有的音訊、影片和子圖片設定。                                               |
| [**SaveBookmark**](savebookmark-method.md)                                       | 將 DVD 導覽器的目前光碟位置和狀態儲存至光碟，讓使用者可以在稍後返回相同位置。                                                                 |
| 資料指標和工具提示                                                              |                                                                                                                                                                                             |
| [**CursorType**](cursortype-property.md)                                         | 設定或抓取目前的資料指標類型。                                                                                                                                                  |
| [**GetDelayTime**](getdelaytime-method.md)                                       | 捕獲與 MSWebDVD 物件相關聯的工具提示延遲時間。                                                                                                               |
| [**SetDelayTime**](setdelaytime.md)                                              | 設定與 MSWebDVD 物件相關聯的工具提示延遲時間。                                                                                                                    |
| [**ShowCursor**](showcursor-method.md)                                           | 當 DVD 導覽器處於全螢幕模式時，讓滑鼠指標變成可見。                                                                                                              |
| [**ToolTip**](tooltip-property.md)                                               | 設定當滑鼠指標停留在 MSWebDVD 的影片矩形上時，將出現的工具提示文字。                                                                                 |
| [**ToolTipMaxWidth**](tooltipmaxwidth-property.md)                               | 設定或抓取與 MSWebDVD 物件相關聯之工具提示的最大寬度。                                                                                                    |
| GPRMs 和 SPRMs                                                                   |                                                                                                                                                                                             |
| [**GetGPRM**](getgprm-method.md)                                                 | 抓取指定的一般參數暫存器。                                                                                                                                         |
| [**GetSPRM**](getsprm-method.md)                                                 | 抓取指定的系統參數 register。                                                                                                                                          |
| [**SetGPRM**](setgprm-method.md)                                                 | 將指定的一般參數暫存器設定為指定的值。                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MSWebDVD ActiveX 控制項](mswebdvd-activex-control.md)
</dt> </dl>

 

 



