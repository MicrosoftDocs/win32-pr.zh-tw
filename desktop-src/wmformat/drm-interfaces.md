---
title: Microsoft Windows 媒體 DRM 用戶端介面
description: Microsoft Windows 媒體 DRM 用戶端介面
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows媒體格式 SDK，介面
- 數位版權管理 (DRM) ，介面
- DRM (數位版權管理) ，介面
- DRM 用戶端擴充 Api，介面
- 用戶端擴充 Api，介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972224decdad339876e4f72c40cad5b3ba28de98446ff358fd36cb7f86bee0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931098"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Microsoft Windows 媒體 DRM 用戶端介面

下表說明 Windows 媒體 DRM 用戶端 api 所支援的介面。



| 介面                                                                    | 描述                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | 提供狀態回呼的定義，您可以執行此作業來處理非同步 DRM 作業。     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | 提供解密內容的方法。                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | 提供就地加密資料的方法。                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | 加密非連續區塊中的資料。                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | **IMFMediaEventGenerator** 介面的延伸模組，可提供取消非同步作業的方法。 |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | 啟用有關「個人化」進度的 advanced status 資訊。                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | 代表本機授權存放區中的一或多個授權。                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | 啟用有關授權備份或還原作業的詳細狀態資訊。                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | 啟用本機授權存放的管理作業。                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | 提供本機授權存放區的其他管理選項。                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | 可讓應用程式查詢受保護檔案的許可權和授權狀態。                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | 提供所需的方法，為網路裝置接收者應用程式建立 Microsoft Windows 媒體 DRM。          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | 提供所需的方法，為網路裝置發送器應用程式建立 Microsoft Windows 媒體 DRM。       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | 提供可讓使用者介入取得授權的方法。                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | 建立 Microsoft Windows 媒體 DRM 用戶端擴充 api 的其他物件。                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | 管理用戶端電腦和 DRM 子系統的各種安全性相關處理常式。                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | 管理元件撤銷和更新。                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | 啟用緩衝區的加密和解密。                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](drm-programming-reference.md)
</dt> </dl>

 

 




