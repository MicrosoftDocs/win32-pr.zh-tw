---
title: 服務提供者的介面
description: 服務提供者的介面
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Media 裝置管理員、服務提供者介面
- 裝置管理員，服務提供者介面
- 服務提供者，介面
- 程式設計參考，服務提供者介面
- Windows Media 裝置管理員的參考，服務提供者介面
- 服務提供者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019d31f05674f0d9e492f8a73748500bc1d9d514
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673804"
---
# <a name="interfaces-for-service-providers"></a>服務提供者的介面

本節說明 Windows Media 裝置管理員 service 提供者所執行的介面。 服務提供者會執行大部分與裝置通訊的實際工作，因為它們會執行應用程式所呼叫的大部分 Windows Media 裝置管理員 SDK 方法。

服務提供者不需要執行本節所列的所有介面。 例如，沒有機載存放裝置的媒體裝置不會執行用來控制或公開內容的介面。 您是否需要在適當的參考頁面上指出方法或介面。



| 介面或類別                                     | 描述                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | 協助程式類別，可讓服務提供者或安全內容提供者驗證應用程式，並建立安全參數的 MAC 簽章。                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | 提供用戶端 (通常是 Windows Media 裝置管理員) 具有此服務提供者所支援裝置的裝置枚舉器。                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | 藉由提供使用裝置路徑建立裝置的方法來擴充 **IMDServiceProvider** 。                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | 藉由提供設定裝置列舉喜好設定的方法來擴充 **IMDServiceProvider2** 。                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | 提供與媒體裝置的實例型關聯。 用戶端可以使用此介面來列舉裝置的儲存體媒體列舉值、取得裝置的相關資訊，以及將不透明的 (傳遞) 命令傳送至裝置。                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | 擴充 **IMDSPDevice** ，方法是提供取得延伸影片格式的方法、取得隨插即用 (PnP) 裝置名稱、使用屬性頁，以及讓您從其名稱取得儲存媒體的指標。 此介面對服務提供者而言是選擇性的，但建議使用。 |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | 藉由提供查詢物件格式之裝置屬性和功能的能力，來擴充 **IMDSPDevice2** 。                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | 提供控制裝置的方法。                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | 可讓 Windows Media 裝置管理員將內容傳輸委派給服務提供者。 在此情況下，Windows Media 裝置管理員不會在將內容傳送給服務提供者之前，對內容進行任何處理。 服務提供者會取得來源的完全控制權。                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | 列舉此服務提供者所支援的媒體裝置。                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | 列舉裝置上的儲存體媒體和儲存媒體上的內容。                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | 包含儲存物件上資料傳輸作業的方法。                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | 藉由提供更有效率的 DRM 啟用資料傳輸，來擴充 **IMDSPObject** 。                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | 設定或取得存放裝置媒體上的播放長度、播放位置、播放位移或播放物件的總長度。                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | 抓取可從中下載更新元件的 URL。                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | 提供與裝置上儲存媒體的實例型關聯。 此介面會建立儲存物件、抓取其相關資訊，並提供 **IMDSPEnumStorage** 介面的存取權，以列舉在目前儲存體中嵌套的子資料夾。                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | 藉由取得和設定擴充屬性來擴充 **IMDSPStorage** ，並讓您可以從名稱取得儲存體的指標。                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | 藉由支援中繼資料來擴充 **IMDSPStorage2** 。                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | 藉由支援播放清單物件來擴充 **IMDSPStorage3** 。                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | 抓取儲存媒體的全域資訊，例如可用空間量和檔案總數。                                                                                                                                                                                              |



 

下圖顯示如何取得服務提供者所執行的各種介面。 在此圖中，衍生介面會顯示在壓縮度的相同標記中，因此 IMDServiceProvider/2/3 會代表三個介面： **IMDServiceProvider**、 **IMDServiceProvider2** 和 **IMDServiceProvider3**。 所顯示的方法只會由其中一個介面擴充。 衍生介面的取得方式是在所建立物件的基底介面上呼叫 **QueryInterface** 。

![顯示 windows media 裝置管理員如何預期從服務提供者取得介面的圖表。](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> <dt>

[**Windows Media DRM-Implemented 介面**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




