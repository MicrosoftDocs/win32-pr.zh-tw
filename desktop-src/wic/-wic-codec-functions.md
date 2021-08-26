---
title: WIC 函數
description: 本節包含 Windows 影像處理元件 (WIC) 函數的相關資訊。
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f60660780e97831a77101c15646385d62048f005279b388a532ca687a200996
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056798"
---
# <a name="wic-functions"></a>WIC 函數

本節包含 Windows 影像處理元件 (WIC) 函數的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                      | 描述                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | 進行編解碼器元件的進度時，所呼叫的應用程式定義回呼函數。<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | 從給定的 **IWICBitmapSource** 取得所需像素格式的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | 傳回 Windows 圖形裝置介面 (GDI) 區段控制碼的圖元所支援的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | 傳回由 GDI 區段控制碼的圖元所支援的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | 傳回指定之 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)所包含之中繼資料內容的大小。 傳回的大小帳戶，用於標頭和中繼資料的長度。<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | 取得與指定 GUID 相關聯的簡短名稱。<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | 取得與給定架構相關聯的名稱。<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | 取得與指定簡短名稱相關聯的 GUID。<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | 取得指定之容器格式的元資料格式 GUID，以及最符合給定資料流程內內容的廠商。<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | 將中繼資料寫入至指定的資料流程。<br/>                                                                                                                                                                       |
| [WIC Proxy 函式](wic-proxy-functions.md)<br/>                                  | 本節包含 WIC proxy 函數。<br/>                                                                                                                                                             |



 

 

 




