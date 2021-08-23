---
title: 物件 (Windows Media Format 11 SDK)
description: 物件
ms.assetid: f884e115-d41a-4f36-bcef-dfaef78510af
keywords:
- Windows媒體格式 SDK，物件
- Advanced Systems Format (ASF) 、objects
- ASF (Advanced Systems Format) ，objects
- 物件，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccd206a548093602f609a11ed11a8d98b910bc35eefb6ba55b985427ac1d212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707448"
---
# <a name="objects-windows-media-format-11-sdk"></a>物件 (Windows Media Format 11 SDK)

Windows 媒體格式 SDK 會使用數個物件來讀取、寫入、編輯及編制 ASF 檔案的索引，以及建立和編輯設定檔。 每個物件都支援數個介面。 多個物件支援某些介面。 在這些情況下，會在介面的參考區段中討論任何實作為的差異。

Windows 媒體格式 SDK 中的物件符合 COM 規範。 為了簡化開發工作，每個物件都有相關聯的建立函式或方法。 您應該使用建立函式或方法來建立物件，而不是使用 COM 函數 **CoCreateInstance** 手動建立物件。

某些介面的名稱後面會附加一個數位，例如 **IWMProfile2** 和 **IWMWriter3**。 在每個案例中，編號版本會繼承舊版的所有方法，並加入新功能。

在此參考的每個物件頁面上，會先列出主要 COM 物件中包含的介面，後面接著應用程式必須執行的回呼介面。

下表列出此 SDK 所支援的物件，以及每個物件的功能描述，以及用來建立它的函式。



| Object                                                          | 描述                                                                                                                                              | 建立函式                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [備份 Restorer](backup-restorer-object.md)                   | 備份授權（通常移至卸載式媒體），然後將這些授權還原到不同的電腦上。                                           | [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer)                 |
| [裝置註冊](device-registration-object.md)           | 管理裝置註冊資料庫，其中包含可透過網路連線使用之媒體播放裝置的專案。             | [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration)         |
| [DRM Transcryptor](drm-transcryptor-object.md)                 | 將受 DRM 保護的媒體資料轉換成資料流程，該資料流程可以傳送至使用 Windows 媒體 DRM 10 用於網路裝置通訊協定的裝置。 | [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor)               |
| [索引編製程式](indexer-object.md)                                   | 建立 ASF 檔案的索引，以啟用使用影片串流在檔案中搜尋。                                                                            | [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)                               |
| [授權撤銷代理程式](license-revocation-agent-object.md) | 管理授權撤銷。                                                                                                                              | [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) |
| [中繼資料編輯器](metadata-editor-object.md)                   | 編輯 ASF 檔案標頭中的中繼資料。                                                                                                                    | [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)                                 |
| [配置檔案管理員](profile-manager-object.md)                   | 提供用來建立、載入和儲存設定檔的介面。 需要設定檔才能寫入 ASF 檔案。                                                      | [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)                 |
| [讀取者](reader-object.md)                                     | 讀取 ASF 檔。 此物件會使用非同步呼叫模型來進行其作業。                                                                      | [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)                                 |
| [同步讀取器](synchronous-reader-object.md)             | 使用同步呼叫讀取 ASF 檔。                                                                                                                 | [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)                         |
| [作家](writer-object.md)                                     | 寫入 ASF 檔案。                                                                                                                                        | [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)                                 |
| [寫入器檔案接收](writer-file-sink-object.md)                 | 控制寫入器物件所寫入的 ASF 檔。                                                                                                         | [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)                 |
| [寫入器網路接收器](writer-network-sink-object.md)           | 控制寫入器物件所寫入之 ASF 檔案的即時網路串流處理。                                                                               | [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)           |
| [寫入器推送接收](writer-push-sink-object.md)                 | 控制傳送串流內容至發佈伺服器。                                                                                            | [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink)                 |



 

下表列出相依于其他物件的物件。 這些物件是由現有物件的方法所建立。



| Object                                                        | 描述                                                                                                                                                                                                                                                                                                                           | 建立方法                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [頻寬共用](bandwidth-sharing-object.md)             | 管理設定檔中的頻寬共用資訊。 設定檔可能存在一個以上的頻寬共用物件。 根據您要建立新的頻寬共用物件或存取現有的物件，建立頻寬共用物件的方法有很多種。                                           | [**IWMProfile3：： CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)或<br/> [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)<br/>                                                                                                                                                                                                                                      |
| [Buffer](buffer-object.md)                                   | 包含媒體範例和任何相關聯的資料單位延伸模組。 用於撰寫和讀取範例。                                                                                                                                                                                                                           | [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)或<br/> [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex)<br/> OR<br/> [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)<br/> OR<br/> 由讀取器物件自動建立，或用於範例傳遞的同步讀取器物件。<br/> |
| [輸入媒體屬性](input-media-properties-object.md)   | 管理輸入的屬性。 每個輸入都可以有一個輸入屬性物件。                                                                                                                                                                                                                                             | [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)                                                                                                                                                                                                                                                                                                                                                                      |
| [互斥](mutual-exclusion-object.md)               | 管理設定檔中的相互排除資訊。 相互排除的常見用法是多種語言的多位元率內容和 soundtracks。 根據您要建立新的互斥物件或存取現有物件，建立相互排除物件的方法有很多種。         | [**IWMProfile：： CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion)或<br/> [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)<br/>                                                                                                                                                                                                                                              |
| [輸出媒體屬性](output-media-properties-object.md) | 管理輸出的屬性。 每個輸出都可以有一個輸出媒體屬性物件。 這些物件可以由讀取器或同步讀取器建立                                                                                                                                                            | [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops)或<br/> [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)<br/>                                                                                                                                                                                                                                                                      |
| [設定檔](profile-object.md)                                 | 在操作中包含設定檔中的資料。 每當需要操作設定檔時，就會建立設定檔物件。 根據您要建立新的設定檔或存取現有的設定檔，有不同的方法可以建立設定檔物件。                                                  | [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)或<br/> [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)<br/> OR<br/> [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)<br/> OR<br/> [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)<br/>          |
| [串流設定](stream-configuration-object.md)       | 管理設定檔內資料流程的屬性。 每當您需要存取資料流程的相關資訊時，資料流程物件就會建立串流設定物件。 有不同的方法可以建立串流設定物件，取決於您想要建立新的資料流程或存取現有的資料流程。 | [**IWMProfile：： CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)或<br/> [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)<br/> OR<br/> [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)<br/>                                                                                                                                                                                   |
| [資料流程優先順序](stream-prioritization-object.md)     | 維護設定檔的資料流程優先權清單。 如果有限制可用的頻寬，則會依提高優先順序來卸載資料流程。 設定檔中只能有一個資料流程優先處理的物件。                                                                                                                  | [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 





