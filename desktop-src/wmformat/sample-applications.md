---
title: Windows媒體格式 SDK 範例應用程式
description: Windows媒體格式 SDK 範例應用程式
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows媒體格式 SDK，範例應用程式
- 數位版權管理 (DRM) 、範例應用程式
- DRM (數位版權管理) 、範例應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c778ef1613359f6f3dc6c08d918e32f2f29bade
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475004"
---
# <a name="windows-media-format-sdk-sample-applications"></a>Windows媒體格式 SDK 範例應用程式

此 SDK 提供的範例程式碼是 Microsoft Visual Studio 2005 的專案格式。 大部分的範例都是在 c + + 中，但 ManagedWMFSDKWrapper 和 ManagedMetadataEdit 需要 c #。

除非已安裝 Windows 媒體格式 sdk 或 Windows 播放機 sdk，否則這些範例將無法運作。

每個範例的使用資訊都包含在每個範例目錄的 readme.txt 檔案中。




| 範例 | Description | 
|-------|-------------|
| >audioplayer | 播放 Windows 媒體檔案，包括受 DRM 保護的檔案。 它是透過 GUI 來控制，而命令則包括播放、暫停、搜尋和停止。 它可以播放從網際網路讀取的本機檔案或檔案 (包括使用 WMVNetWrite 範例) 的輸出到網際網路。<blockquote>[!Note]<br />Windows 的 x64 版本不支援此範例的 DRM 部分。</blockquote><br /> | 
| DRMHeader | DRMHeader 是一種主控台應用程式，它會使用中繼資料編輯器的 <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> 介面，在不連結至 drm 靜態程式庫的情況下，讀取檔案的 drm 屬性。<blockquote>[!Note]<br />X64 型版本的 Windows 不支援這個範例。</blockquote><br /> | 
| DRMShow | DRMShow 是一個主控台應用程式，示範如何使用<strong>IWMDRMReader：： GetDRMProperty</strong>方法，讀取 Windows 媒體檔案的<a href="wmformat-glossary.md"><em>DRM</em></a>屬性。這個範例示範如何使用<strong>IWMDRMReader：： GetDRMProperty</strong>方法，以及可從 DRM 讀取器抓取的屬性。 它不會示範如何取得受 DRM 保護內容的授權。 此範例需要 DRM 存根程式庫 WMStubDRM 來建立。<br /><blockquote>[!Note]<br />X64 型版本的 Windows 不支援這個範例。</blockquote><br /> 當您從 Microsoft 取得 WMStubDRM 時，會將應用程式安全性層級指派給該程式庫。 如果您收到的程式庫安全性層級不足以播放受保護的檔案，此範例將會顯示錯誤。<br /> | 
| DirectShowInterop/DSCopy | 使用 DirectShow WM ASF 寫入器篩選器，將一或多個檔案轉碼至 ASF 檔案。 輸入檔可能是 DirectShow 所支援的任何壓縮或未壓縮格式。 | 
| DirectShowInterop/DSPlay | 此範例是互動式音訊/影片媒體檔案播放機（具有 <a href="wmformat-glossary.md"><em>DRM</em></a> 支援）。 它使用 DirectShow 的 WM ASF 讀取器篩選器來播放 Windows 媒體檔案 (ASF、WMA、WMV) 沒有 drm 保護，以及在100或更低層級使用 drm 的檔案。 如需詳細資訊，請參閱範例目錄中的 readme.txt。 | 
| DirectShowInterop/DSSeekFm | 此範例示範如何使用 DirectShow WM ASF 讀取器篩選器在 DirectShow 篩選圖形中播放 ASF 內容，以及如何使用 Windows 媒體格式 SDK 中搜尋支援的畫面格。 | 
| Managed/WMFSDKWrapper | 此 managed 元件可作為 managed 程式碼範例所使用的包裝函式，以存取此 SDK 的一些中繼資料介面。 | 
| Managed/MetadataEdit | 此 c # 應用程式可用來從 Windows 媒體檔案來查看和編輯中繼資料。 | 
| MetaDataEdit | 這是 Managed MetadataEdit 應用程式的 c + + 版本。 | 
| ReadFromStream | 此主控台應用程式範例示範如何使用 WMReader 從 <strong>IStream</strong> 讀取資料。 已將<strong>IStream</strong>來源實作為使用 Windows 媒體格式的檔案 (WMA/WMV/ASF) 。<blockquote>[!Note]<br />此範例不會示範如何處理 WMReader 中所推出的媒體範例。 如需有關如何處理音訊/影片或其他媒體範例類型的範例，請參閱 Windows 媒體格式 SDK 隨附的其他範例，例如 >audioplayer。</blockquote><br /> | 
| UncompAVIToWMV | 此主控台應用程式範例會顯示將 AVI 檔案壓縮成 WMV 檔案的必要程式碼。 它會示範如何合併數個 AVI 檔案中的音訊和影片串流範例，並將其合併成類似的資料流程，或根據來來源資料流設定檔建立新的資料流程。 它也會示範如何建立任意資料流程、進行 multipass 編碼、新增 SMPTE 時間代碼，以及套用 DRM 第1版保護。 | 
| WMGenProfile/exe | 此範例已從7.1 版本更新。 它現在是 MFC 對話應用程式。 WMGenProfile 範例示範如何使用 WMGenProfile 靜態程式庫。 它也可做為建立設定檔的工具。 這項工具適用于熟悉 Windows 媒體格式的開發人員。 UI 尚未經過測試以取得使用者經驗，也不是將此資訊提供給使用者的建議。 | 
| WMGenProfile/lib | GenProfile 程式庫範例會示範如何建立設定檔。 它會示範如何建立各種串流類型的媒體類型和資料流程 (音訊、影片、腳本、影像、檔案傳輸和 Web) 。 它不會示範如何使用系統設定檔，或是如何將系統設定檔轉換成指定 Windows Media 音訊和 Video 9 系列編解碼器的設定檔。 | 
| WMProp | 此主控台應用程式示範如何使用「中繼資料編輯器」物件和「讀取器」中的設定檔資訊來取出屬性。 | 
| WMStats | 此主控台應用程式會顯示讀取器和寫入器統計資料。 您也可以在一部電腦上同時使用多個 WMStats 實例。 以伺服器的形式啟動一個實例，以將資料流程傳送至網路，然後以用戶端的形式執行第二個實例，以確認伺服器已正確串流處理。 | 
| WMSyncReader | 此主控台應用程式範例示範如何使用 <strong>IWMSyncReader</strong> 讀取媒體檔案，而不需要建立任何額外的執行緒或使用回呼。 會執行下列功能：讀取已壓縮或解壓縮的範例<br /> 以時間為基礎的搜尋<br /> 以框架為基礎的搜尋<br /><strong>IStream</strong> 衍生來源<br /> | 
| WMVAppend | 此主控台應用程式會使用兩個 Windows 媒體檔案進行輸入，並嘗試建立一個輸出檔案，其中包含第一個的內容，後面接著第二個。 此範例會比較兩個輸入檔的設定檔，以確保它們的相似之處。 如果不是這種情況，就會出現錯誤訊息。 例如，當一個檔案僅為音訊，第二個是音訊影片檔案，或兩個音訊檔案有不同的位速率時，就會出現錯誤訊息。此範例會 (VBR) 來源接受可變的位元速率。 不過，在比較兩個 VBR 來源的設定檔時，此範例會忽略平均位元速率差異，因為兩個 VBR 資料流程會有不同的平均位速率，即使它們是使用相同的設定檔建立的。 WMVAppend 無法比較未受限制之以位速率為基礎的 VBR 資料流程或品質層級的 VBR 資料流程的尖峰位速率，因為這項資訊不存在於原始程式檔中。 因此，使用者必須負責確定兩個來源檔案是使用相同的設定檔所建立。 否則，就可以建立不正確內容。<br /> | 
| WMVCopy | 此範例顯示覆制 WMV 檔案所需的程式碼。 它會顯示如何讀取和寫入壓縮的範例、讀取標頭屬性和腳本，以及修改標頭屬性。 | 
| WMVNetWrite | 此主控台應用程式顯示如何在網際網路上串流處理 Windows 媒體檔案。 此範例需要指定埠，然後才能使用播放檔播放該檔案。 | 
| WMVRecompress | 此主控台應用程式顯示如何重新壓縮 WMV 檔案。 它會示範如何讀取未壓縮的範例、撰寫未壓縮的範例，以及進行多重傳遞編碼、多重通道輸出和智慧型 recompression。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows 媒體格式 SDK**](about-the-windows-media-format-sdk.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 





