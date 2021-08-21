---
title: Windows媒體裝置管理員架構
description: Windows媒體裝置管理員架構
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows媒體裝置管理員，架構
- 裝置管理員，架構
- Windows 媒體裝置管理員的架構
- Windows媒體裝置管理員，桌面應用程式
- 裝置管理員，桌面應用程式
- Windows媒體裝置管理員、服務提供者
- 裝置管理員，服務提供者
- Windows媒體裝置管理員、外掛程式
- 裝置管理員、外掛程式
- 桌面應用程式、Windows 媒體裝置管理員架構
- 服務提供者、Windows 媒體裝置管理員架構
- 外掛程式，Windows 媒體裝置管理員架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deadb7e5a85c4d7331a276a515add2ace30e566c2b683404b7b4466bf891dbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055592"
---
# <a name="windows-media-device-manager-architecture"></a>Windows媒體裝置管理員架構

Windows媒體裝置管理員可讓應用程式或外掛程式與裝置通訊。 應用程式可以要求裝置中繼資料、列舉和探索連接的裝置，以及傳送或接收物件 (資料夾、檔案、播放清單等) 。 WindowsMedia 裝置管理員提供單一 API 給呼叫的應用程式，不論 (MTP 或大量儲存體類別所呼叫的裝置類型為何，都是在以舊版 Windows 媒體裝置管理員) 上建立的服務提供者。

Windows媒體裝置管理員可作為系統的三個主要元件之間的移入：應用程式，此應用程式會要求 (資訊、讀取或寫入資料，以及) ;安全內容提供者，其為處理受 DRM 保護檔案之通訊的元件;和服務提供者，會接收來自應用程式的要求，並與裝置通訊以執行這些要求。 應用程式和服務提供者都是以 Windows 媒體裝置管理員 SDK 為基礎。

下圖顯示桌面應用程式如何使用 Windows 媒體裝置管理員11來與裝置通訊。

![此圖顯示與四種不同類型的裝置通訊的應用程式。](images/wmdm-device-communication.gif)

上圖顯示的應用程式與四種不同類型的裝置通訊，每個裝置都有自己的服務提供者。 每個服務提供者的設計都是為了與特定類型的裝置通訊;下圖顯示三個 Microsoft 提供的服務提供者 (適用于大量儲存體類別裝置、RAPI 裝置和 MTP 裝置) 的一般類別驅動程式，以及由協力廠商所建立之專屬裝置的自訂服務提供者。 當裝置連線時，Windows 媒體裝置管理員具現化該裝置所註冊之服務提供者的實例。 服務提供者會透過其所執行的 Windows 媒體裝置管理員介面，從應用程式取得要求、使用適當的驅動程式與裝置通訊，以及傳回適當的結果。 服務提供者與裝置之間的通訊，位於 Windows 媒體裝置管理員的網域之外。

應用程式無法看到服務提供者;應用程式只會看到「裝置」清單，因為 Windows 媒體裝置管理員為所有裝置公開一組標準的方法和介面。 如果製造商建立自訂服務提供者，則如果應用程式能夠使用裝置，則必須處理所有標準 Windows 媒體裝置管理員方法。

此圖表也會顯示 (SCP) 模組的安全內容提供者。 本課程模組負責處理 (DRM) 受保護內容的數位版權管理。 Microsoft 提供可處理受 DRM 保護的 WMA 和 WMV 檔案的 SCP 模組。 如果應用程式或裝置打算處理其他受保護的格式，則必須提供自己的 SCP 模組。 應用程式和服務提供者都不會直接處理 SCP。

應用程式和服務提供者都建置於 Windows 媒體裝置管理員上，其會在應用程式和裝置的適當服務提供者之間路由呼叫;服務提供者負責直接與裝置通訊。 Windows媒體裝置管理員執行某些動作本身 (例如列舉連線的裝置、路由呼叫，以及處理元件驗證) ;不過，大部分的工作都是由服務提供者完成，它會接收來自應用程式的要求，並與裝置通訊。

Windows 媒體裝置管理員上建的應用程式，可以與以舊版 Windows 媒體裝置管理員建立的裝置和服務提供者通訊。不過，這些較舊的裝置將會透過9個系列元件執行， (不會顯示) ，而且不支援最新的功能，特別是更先進的數位版權管理技術。

裝置的架構

下圖顯示使用 Windows 媒體裝置管理員的應用程式所看到的簡化裝置和儲存體階層。

![顯示裝置上存放裝置的圖表。](images/wmdm-basic-device-layout.gif)

上圖顯示連接快閃磁片磁碟機的簡化版本，如 Windows 媒體裝置管理員應用程式所見。 快閃磁片磁碟機有屬性和屬性，例如序號和支援的格式設定。 Flash 裝置的直屬子系是根儲存物件，它包含資料夾，其本身包含影像和歌曲。

應用程式會藉由呼叫根 [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) 介面所公開的列舉方法來列舉附加裝置的清單。 裝置會以 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (或衍生) 介面表示。 此介面會公開方法，以抓取裝置名稱、格式功能、序號等，以及列舉裝置上之 *存儲* 設備的方法。 在 Windows 媒體裝置管理員中，不論是否為實際的資料 blob，儲存體都是裝置上的任何一種物件。 例如：儲存為檔案的音訊檔案、文字檔、資料夾、播放清單，以及儲存為中繼資料的播放清單都會被視為儲存，即使資料夾和中繼資料專案可能不代表實體檔案也是一樣。 您可以藉由呼叫 [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (或 [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)，要求儲存) 的格式，來抓取儲存體的類型 (或格式) 。

裝置上的儲存體會以階層方式儲存，所有裝置都有根儲存體。 每個儲存區可以保留零個或多個子物件，藉由呼叫該儲存體的 [**IWMDMStorage：： EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) 方法來列舉。

請注意，圖表中的每個儲存區都有相關聯的屬性和中繼資料 (並非所有值都會顯示) 。 屬性很簡單，也就是布林資訊，通常描述管理或導覽資訊 (例如「有資料夾」或「可刪除」 ) ，中繼資料可以是字串值、數位或複雜的資訊 (例如) 的轉譯功能。 屬性是由 SDK 所定義且一組相當有限的旗標所描述，並藉由呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) 或 [**IWMDMStorage2：： GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)來加以取出。 中繼資料值是以唯一名稱抓取;SDK 會定義許多裝置應該支援的中繼資料值，但裝置可以定義自己的 [中繼資料常數](metadata-constants.md)。 但是，如果裝置或服務提供者定義了新的中繼資料常數，除非應用程式開發人員知道這個新的常數，否則應用程式將無法要求或設定這個值。 服務提供者必須支援 [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) 或更新版本，才能支援抓取或設定中繼資料。 如需詳細資訊，請參閱 [取得和設定中繼資料和屬性](getting-and-setting-metadata-and-attributes.md)。

服務提供者

服務提供者會作為應用程式與裝置之間的中間人。 應用程式開發人員看不到服務提供者，因此應用程式開發人員不需要知道有關開發服務提供者的任何事項。 不過，它是可執行與裝置通訊之工作的服務提供者。

服務提供者是以 Windows 媒體裝置管理員為基礎的 COM DLL，可接收來自應用程式的要求，並與裝置通訊以執行這些要求。 Windows 媒體裝置管理員 mediated 與桌面應用程式的通訊;與裝置的通訊是在服務提供者的控制之下。

服務提供者會接收來自應用程式的要求，以列舉裝置內容、裝置功能要求、讀取或寫入資料的要求等等。 它必須知道裝置的設計是否足夠，才能以適當的格式和通訊協定來傳送命令。 它也應該能夠隱藏裝置特定需求，例如播放清單的必要副檔名，讓應用程式不需要知道這些需求就能使用裝置。

Microsoft 提供許多標準裝置類型的服務提供者，包括一般 MTP 裝置、大量儲存體類別裝置，以及 RAPI 裝置。 裝置設計工具需要建立自訂服務提供者的唯一原因是，裝置有一些特定或不尋常的標準服務提供者未處理的資料儲存需求，例如，如果檔案必須儲存在特定的位置，而裝置作業系統不會自動處理這種情況。

當裝置連接到電腦時，作業系統會針對每個 Windows 媒體裝置管理員應用程式，建立一個適當服務提供者的實例。 如果第二 Windows 媒體裝置管理員應用程式啟動，則會載入服務提供者的第二個實例。 不過，每個服務提供者都可以處理多個裝置。 下圖顯示這個關係。

![此圖顯示兩個與兩個應用程式通訊的 mtp 裝置。](images/wmdm-sp-to-device.gif)

上圖顯示兩個不同的應用程式與兩個 MTP 裝置通訊。 裝置使用相同的服務提供者類別，但每個應用程式都有自己的相同服務提供者實例。 每個服務提供者實例正在與裝置通訊。 不同的服務提供者實例彼此都不會察覺。

許多應用程式方法都有相對應的名稱服務提供者方法。 當應用程式呼叫方法時，Windows 媒體裝置管理員會將呼叫路由至服務提供者上的對應方法 (但它可能會先執行一些額外的內部動作) 。 例如，當應用程式呼叫 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)時，Windows Media 裝置管理員將此呼叫路由傳送至服務提供者的 [**IMDSPDevice3：： GetProperty 的**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty)。  (大部分的應用程式介面都以 IWMDM 開頭，且對應的服務提供者介面開頭為 IMDSP) 。 服務提供者預期會處理此方法呼叫，並傳回適當的結果。

應用程式永遠不會直接 (探索或與裝置通訊，除非它呼叫 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) 或 [**IWMDMStorage：： SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)) ;應用程式會與服務提供者進行通訊，該服務提供者必須以最具邏輯和簡單的方式來代表裝置。 當應用程式要求裝置的相關資訊，或列舉裝置上的物件時，服務提供者會以適當的方式查詢裝置，並取得並傳回適當的資訊。 它可能會以不同的方式將裝置上的檔案組織公開于裝置上（如果適合的話）。 不過，它會公開裝置，它應該是以一致的邏輯方式，讓應用程式能夠找出所需的內容，並處理它所傳送的命令。 良好的服務提供者將會隱藏裝置特定的特性，例如，如果裝置實際將播放清單儲存為具有自訂副檔名的檔案，則服務提供者應該會在應用程式在裝置上建立播放清單時自動新增該擴充功能;建立播放清單物件時，應用程式不應該知道適當的副檔名。

服務提供者會在呼叫應用程式的進程內執行。 唯一的例外是 MTP 服務提供者，它會在自己的進程中執行。 因此，封鎖的服務提供者會造成呼叫應用程式封鎖的風險。 因此，服務提供者應設計為穩定且防止封鎖，應用程式應設計成在特定方法呼叫不會快速傳回時避免拖延。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](getting-started.md)
</dt> </dl>

 

 




