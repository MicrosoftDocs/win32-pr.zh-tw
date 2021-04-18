---
title: Microsoft Windows Media DRM 用戶端介面
description: Microsoft Windows Media DRM 用戶端介面
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK，介面
- 數位版權管理 (DRM) ，介面
- DRM (數位版權管理) ，介面
- DRM 用戶端擴充 Api，介面
- 用戶端擴充 Api，介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383581"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Microsoft Windows Media DRM 用戶端介面

下表說明 Windows Media DRM 用戶端 Api 所支援的介面。



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
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | 提供所需的方法來建立網路裝置接收者應用程式的 Microsoft Windows Media DRM。          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | 提供所需的方法，為網路裝置發送器應用程式建立 Microsoft Windows Media DRM。       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | 提供可讓使用者介入取得授權的方法。                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | 建立 Microsoft Windows Media DRM 用戶端擴充 Api 的其他物件。                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | 管理用戶端電腦和 DRM 子系統的各種安全性相關處理常式。                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | 管理元件撤銷和更新。                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | 啟用緩衝區的加密和解密。                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](drm-programming-reference.md)
</dt> </dl>

 

 




