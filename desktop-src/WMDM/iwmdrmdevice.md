---
title: IWMDRMDevice 介面
description: 這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。IWMDRMDevice 介面可讓安全的內容提供者與針對可攜式裝置使用 Windows Media DRM 10 的裝置進行通訊。
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- IWMDRMDevice 介面 windows Media 裝置管理員
- IWMDRMDevice interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315475"
---
# <a name="iwmdrmdevice-interface"></a>IWMDRMDevice 介面

這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。

**IWMDRMDevice** 介面可讓安全的內容提供者與針對可攜式裝置使用 WINDOWS Media DRM 10 的裝置進行通訊。

## <a name="members"></a>成員

**IWMDRMDevice** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMDevice** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMDevice** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | 開始在裝置上清除 DRM 資料存放區的進程。<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | 抓取裝置憑證。<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | 捕獲計量挑戰。<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | 抓取安全時鐘。<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | 捕獲安全的時鐘挑戰。<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | 抓取授權同步處理清單。<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | 判斷裝置是否支援可攜式裝置的 Windows Media DRM 10。<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | 設定授權回應。<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | 設定計量回應。<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | 設定安全時鐘回應。<br/>                                                   |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**服務提供者的介面**](interfaces-for-service-providers.md)
</dt> </dl>

 

