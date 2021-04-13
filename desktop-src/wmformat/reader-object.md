---
title: 讀取器物件
description: 讀取器物件
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media 格式 SDK，讀取器物件
- Advanced Systems Format (ASF) 、reader 物件
- ASF (Advanced Systems Format) 、reader 物件
- 物件、讀取器物件
- 讀者物件，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104374888"
---
# <a name="reader-object"></a>讀取器物件

讀取器物件會從媒體檔案讀取資料範例。 讀取器物件目前支援使用 advanced systems 格式的檔案 (ASF) 檔案結構以及 MP3 檔案。 依預設，讀取器物件所傳遞的資料已解壓縮且可供轉譯，雖然可以在不需要解壓縮的情況下傳遞範例。 範例會以非同步方式從 reader 物件傳遞;您必須設定回呼函數來接收它們。 若要同步播放 ASF 檔案，請使用同步讀取器物件。 讀取器和同步讀取器都不會轉譯任何資料。 您必須提供自己的轉譯常式，才能顯示從檔案取出的媒體。

當檔案包含可使用讀取器物件所支援之編解碼器解碼的編碼媒體時，您可以控制未壓縮輸出的格式。 若要變更資料流程的解壓縮輸出格式，您必須取出該資料流程的預設輸出媒體屬性物件、對其進行變更，然後將它重新指派給讀取器中的資料流程。 輸出媒體屬性物件是讀取器物件的從屬物件，且只能使用 [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) 方法建立。

讀取器物件是由函式 [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader)所建立，它會將指標設定為 **IWMReader** 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得 reader 物件的其他介面。

讀取器物件支援下列介面。



| 介面                                                    | 描述                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IReferenceClock**](ireferenceclock.md)                   | 提供讀取器所使用之系統時鐘的存取權。                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | 管理授權取得、 [*DRM*](wmformat-glossary.md) 屬性和用戶端的個人化。                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | 提供使用輸出保護層級 (OPL) 來指定許可權的授權存取權。                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | 設定及抓取標頭資訊，包括中繼資料、 [*標記*](wmformat-glossary.md)和腳本資料。                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | 抓取用來對檔案中的內容進行編碼之編解碼器的相關資訊。 繼承 **IWMHeaderInfo** 的所有方法。                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | 支援大型屬性大小、重複的屬性名稱，以及多語言支援。 繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | 抓取讀取器中載入之檔案的最大封包大小。                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | 抓取讀取器中載入之檔案中最小的封包大小。                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | 提供讀取器中所載入之檔案的設定檔資訊存取權。                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | 抓取與設定檔相關聯 (GUID) 的全域唯一識別碼（如果有的話）。 繼承 **IWMProfile** 的所有方法。                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | 支援設定檔中的頻寬共用和串流優先順序資訊。 繼承 **IWMProfile** 和 **IWMProfile2** 的所有方法。                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | 提供基本的檔案讀取功能，包括開啟、關閉、啟動、暫停、繼續、停止以及取得和設定輸出屬性等作業。                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | 與 DirectX video 加速通訊。                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | 提供讀取器的 advanced 功能，例如使用者提供的時鐘、緩衝區配置、傳回統計資料，以及資料流程選取通知。                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | 為現有的 reader 物件提供額外的 advanced 方法範圍。 繼承 **IWMReaderAdvanced** 的所有方法。                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | 提供先進的搜尋和串流控制。 繼承 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 的所有方法。                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | 提供 advanced reader 選項，包括多種語言支援。 繼承 **IWMReaderAdvanced**、 **IWMReaderAdvanced2** 和 **IWMReaderAdvanced3** 的所有方法。 |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | 控制網路設定設定。                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | 提供對 advanced network configuration 設定的存取。 繼承 **IWMReaderNetworkConfig** 的所有方法。                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | 設定和取消資料流程時鐘上的計時器，並抓取指定之資料流程時鐘的目前值。                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | 提供讀取器中載入的檔案之 SMPTE 時間碼範圍的相關資訊。                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | 測試資料流程的輸出屬性變更是否正常運作。                                                                                                |



 

您可以在應用程式中執行下列回呼介面，以追蹤讀取器物件的進度。



| 介面                                                      | 描述                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | 取得使用者的認證，並檢查他們是否擁有存取遠端網站的許可權。                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | 提供 **IWMReaderCallbackAdvanced** 介面的 **AllocateForOutput** 和 **AllocateForStream** 方法的擴充替代專案。 |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | 提供 **IWMReader****啟動** 和 **開啟** 方法的回呼方法。                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | 提供 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) 介面之方法的回呼方法。                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | 必須將狀態資訊傳達給主應用程式時，才需要此資訊。                                                                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**同步讀取器物件**](synchronous-reader-object.md)
</dt> </dl>

 

 




