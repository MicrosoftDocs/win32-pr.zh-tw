---
title: 應用程式的介面
description: 應用程式的介面
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows媒體裝置管理員，應用程式介面
- 裝置管理員，應用程式介面
- 桌面應用程式，介面
- 程式設計參考，應用程式介面
- Windows 媒體裝置管理員的參考、應用程式介面
- 外掛程式，介面
- 應用程式介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690b8419a7f04ef2b4eab1db65266027bdf5bcf3a102e59a95030a290e3747ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619951"
---
# <a name="interfaces-for-applications"></a>應用程式的介面

本節說明使用 Windows Media 裝置管理員 SDK 來與裝置通訊的應用程式所使用或執行的介面。 此處使用的「應用程式」一詞是指存在於桌上型電腦上的任何可執行檔、外掛程式或 COM 物件，而且需要與連線的可攜式裝置進行高階通訊。 這可以包括媒體播放機應用程式、Windows Media Player 外掛程式 (是否需要可直接存取可攜式裝置) 或播放次數計量 COM 物件。

這些介面中有些是由應用程式所執行，而有些則是由應用程式呼叫。 每個介面的檔會指出它是實 (，還是在執行時，不論是選擇性或必要) 。

應用程式會使用下列介面或類別。



| 介面或類別                                           | 描述                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelClient 類別](csecurechannelclient-class.md) | Helper 類別，可讓應用程式自行驗證、加密和解密資料，以及建立 Mac。                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | 應用程式的最上層 Windows 媒體裝置管理員介面。                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | 藉由提供先進的列舉方法和其他方法來擴充 **IWMDeviceManager** 。                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | 藉由提供可設定裝置列舉喜好設定的方法，來擴充 **IWMDeviceManager2** 介面。                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | 提供檢查及探索單一可攜式裝置的方法。                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | 藉由讓您能夠取得裝置所支援的影片格式、依名稱尋找儲存體，並使用屬性頁來擴充 **IWMDMDevice** 。                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | 藉由提供方法來查詢裝置的屬性、傳送裝置 i/o controle 碼，以及提供升級的方法來搜尋存放裝置和取得裝置格式功能，藉此擴充 **IWMDMDevice2** 。 |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | 提供控制裝置的方法。                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | 藉由將多個作業組合成一個會話，來改善裝置作業的效率                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | 列舉連接到電腦的可攜式裝置。                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | 列舉裝置上的儲存體。                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | 設定及抓取 (的中繼資料屬性，例如演出者、專輯、內容類型，以及儲存體) 。                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | 取得和設定資訊，控制 **IWMDMDeviceControl** 介面如何處理裝置上可播放的檔案                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | 如果傳送因撤銷錯誤而失敗，則抓取可從中下載更新元件的 URL。                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | 提供方法來檢查和探索裝置上的儲存體 (檔案、資料夾、播放清單) 。                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | 藉由讓您依名稱取得子儲存體，以及取得和設定擴充屬性，來擴充 **IWMDMStorage** 。                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | 藉由公開中繼資料來擴充 **IWMDMStorage2** 。                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | 擴充 **IWMDMStorage3** ，方法是提供方法來抓取儲存區的可用中繼資料子集，以及設定和取得其他儲存體的參考清單。                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | 用來插入、刪除或移動裝置內或裝置與電腦之間的檔案。                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | 擴充 **IWMDMStorageControl** ，讓您可以在將內容插入儲存體時，設定目的地檔案的名稱。                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | 藉由讓您能夠傳入 **IWMDMMetaData** 介面指標，來擴充 **IWMDMStorageControl2** 。                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | 提供方法，以在裝置上取出儲存媒體 (的全域資訊，例如 flash ROM 卡) 。                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | 可讓應用程式執行計量、授權同步處理，以及裝置 DRM 元件的更新。                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | 藉由提供新版本的 **QueryDeviceStatus** 方法來擴充 **IWMDRMDeviceApp** 。                                                                                                                         |



 

回呼介面

下列選用的介面是由應用程式所執行，以便追蹤非同步要求的進度，例如讀取或寫入要求。



| 介面                                      | 描述                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | 可讓應用程式和服務提供者在裝置或記憶體存放裝置 (（例如 RAM 卡) 連線或與電腦中斷連線）時收到通知。 |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | 藉由提供方法來取得和設定擴充屬性，藉以擴充 **IWMDMOperation** 。                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | 藉由提供新的方法來傳輸未加密的資料以提高效率，來擴充 **IWMDMOperation** 。                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | 允許應用程式控制在檔案傳輸期間，從電腦讀取或寫入資料的方式。                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | 藉由提供狀態指標來擴充 **IWMDMProgress：： End** 方法。                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | 藉由提供額外的輸入參數來擴充 **IWMDMProgress2** ，以指定事件識別碼和內容特定資訊。                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | 允許應用程式追蹤作業的進度，例如格式化媒體或檔案傳輸。                                                                  |



 

下圖顯示從根 **IWMDeviceManager** 介面取得大部分重要的應用程式介面的方式。 應用程式會藉由 cocreating MediaDevMgr 物件、要求 **IComponentAuthenticate** 介面、驗證元件，然後要求 **IWMDeviceManager** (這些步驟會在 [驗證應用程式](authenticating-the-application.md)) 中說明，來取得這個根介面。 一旦取得這個根介面，就會呼叫 [**IWMDeviceManager：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) 來建立可執行 [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)的物件。 其他介面則是藉由在介面上依顯示的順序呼叫方法來取得。 衍生介面（例如 [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) ）是藉由在基底介面上呼叫 **QueryInterface** 來取得。

在下圖中，衍生介面會以斜線標示，因此 "IWMDMStorage/2/3" 會指出 **IWMDMStorage**、 **IWMDMStorage2** 和 **IWMDMStorage3**。

![此圖顯示如何在 windows media 裝置管理員中取得主要的應用程式介面。](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 




