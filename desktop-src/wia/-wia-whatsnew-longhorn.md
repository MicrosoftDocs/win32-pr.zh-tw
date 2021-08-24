---
description: 許多新的 Windows 映像取得 (wia) API 都包含在 Windows 影像取得 (wia) 2.0 中。
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Windows 映像取得的新功能 (WIA) 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef5fdc2f70c7b0a7c25e3e9df68b82d05b7fd1a53eb7ec3613962f975e5c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592948"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Windows 映像取得的新功能 (WIA) 2。0

許多新的 Windows 映像取得 (wia) API 都包含在 Windows 影像取得 (wia) 2.0 中。 此外，Windows 影像取得之間有一些向前及向後不相容 (WIA) 1.0 和 Windows Vista 隨附的 WIA 2.0 服務。 不支援 WIA 1.0 的某些介面、結構、屬性和屬性值，而且使用它們的應用程式不會在 Windows Vista 和更新版本上執行。 同樣地，使用 WIA 2.0 所引進之新介面、結構、屬性和屬性值的應用程式， (見下面) 將無法在 Windows Vista 之前的 OS 版本上執行。

## <a name="new-api-for-wia-20"></a>適用于 WIA 2.0 的新 API

### <a name="constants-lists-updated-for-wia-20"></a>常數：已更新 WIA 2.0 的清單

-   [**常見的 WIA 專案屬性常數**](-wia-wiaitempropcommonitem.md)
-   [**裝置資訊屬性常數**](-wia-wiadeviceinfoprop.md)
-   [**掃描器裝置屬性常數**](-wia-wiaitempropscannerdevice.md)
-   [**掃描器 WIA 專案屬性常數**](-wia-wiaitempropscanneritem.md)
-   [**WIA 2.0 專案類別目錄 Guid**](-wia-wia2-itemcategoryguids.md)
-   [**WIA 2.0 頁面大小常數**](-wia-wia2-pagesizeconstants.md)
-   [**WIA 專案類型旗標**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>WIA 2.0 中的新結構



| 主題                                               | 目錄                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | 定義呼叫裝置對話方塊所需的資料。<br/>                                                                                                                                                                                                       |
| [**WIA \_ 原始 \_ 標頭**](-wia-wia-raw-header.md)     | [**Wia \_ raw \_ 標頭**](-wia-wia-raw-header.md)結構會以裝置的原始資料格式來定義影像，並讓應用程式在 WIA 傳輸中使用原始格式。<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | 當 WIA 執行時間系統將資料傳輸至 [**IWiaTransferCallback：： TransferCallback**](-wia-iwiatransfercallback-transfercallback.md)方法時，會將 [**WiaTransferParams**](-wia-wiatransferparams.md)傳送至應用程式。<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>WIA 2.0 中的新介面



| 主題                                                         | 目錄                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | 由應用程式用來列舉專案樹狀結構目前資料夾中的 [**IWiaItem2**](-wia-iwiaitem2.md) 物件。<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | [**IScanProfile**](-wia-iscanprofile.md)介面代表單一掃描設定檔，可讓應用程式設定和取得設定檔的屬性。 <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | [**IScanProfileMgr**](-wia-iscanprofilemgr.md)介面提供建立、開啟、刪除及管理掃描設定檔的方法。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | [**IScanProfileUI**](-wia-iscanprofileui.md)介面可讓應用程式顯示對話方塊，讓使用者可以建立、修改和刪除掃描設定檔。<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)介面可讓應用程式在資料傳輸期間顯示錯誤的 windows () 使用者可以從中選擇是否要繼續、取消或中止傳送。<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)介面是用來建立及管理影像取得裝置，並註冊以接收裝置事件。<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)介面會提供方法來處理應用程式要求影像資料時可能發生的錯誤（不論是預覽或最終位）。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | [**IWiaImageFilter**](-wia-iwiaimagefilter.md)介面是一個擴充介面，由影像處理篩選器開發人員所執行，並由 WIA 2.0 呼叫。 <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | [**IWiaItem2**](-wia-iwiaitem2.md)介面提供與 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面相同功能的應用程式 (能夠查詢裝置以探索其功能、存取資料傳輸介面和專案屬性，以及控制裝置) 。 它也提供應用程式動態建立和使用影像處理篩選的能力，而這些篩選器可作為 Windows Vista 中提供的 WIA 2.0 設備磁碟機的延伸模組。<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | [**IWiaPreview**](-wia-iwiapreview.md)介面會在內部快取未篩選的影像，並透過影像處理篩選器來傳遞它們。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)介面會偵測影像資料流程的子領域，並為每個區域建立個別的 [**IWiaItem2**](-wia-iwiaitem2.md)專案。 <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | [**IWiaTransfer**](-wia-iwiatransfer.md)介面會提供資料流程傳輸的資料。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)介面會在資料傳輸期間接收回呼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | IWiaUIExtension2 介面提供的方法會將預設的系統提供的使用者介面取代為自訂的使用者介面，並提供自訂裝置圖示。 裝置廠商可以執行此介面，為其裝置提供自訂使用者介面。<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>WIA 2.0 的新增和變更總覽



| 主題                                                                          | 目錄 |
|--------------------------------------------------------------------------------|----------|
| [常數](-wia-constants.md)                                                |          |
| [函式](-wia-functions.md)                                                |          |
| [介面](-wia-interfaces.md)                                              |          |
| [掃描設定檔架構](-wia-scan-profile-schema.md)                            |          |
| [結構](-wia-structures.md)                                              |          |
| [在 WIA 2.0 中傳送影像資料](-wia-transferring-image-data-in-wia2.md) |          |
| [WIA 裝置類型規範](-wia-wia-device-type-specifiers.md)              |          |
| [WIA 屬性常數](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>留下意見反應

透過電子郵件將 **sdkfdbk@microsoft.com** 錯誤報表和功能要求直接傳送給 Microsoft。

 

 




