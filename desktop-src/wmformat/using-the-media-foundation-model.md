---
title: 使用媒體基礎事件模型
description: 使用媒體基礎事件模型
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK，DRM 媒體基礎事件模型
- Windows Media 格式 SDK，媒體基礎事件模型
- Windows Media Format SDK，DRM 事件模型
- 數位版權管理 (DRM) 媒體基礎事件模型
- DRM (數位版權管理) ，媒體基礎事件模型
- 數位版權管理 (DRM) 、事件模型
- DRM (數位版權管理) 、事件模型
- 數位版權管理 (DRM) ，IWMDRMEventGenerator 介面
- DRM (數位版權管理) 、IWMDRMEventGenerator 介面
- 媒體基礎
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023112"
---
# <a name="using-the-media-foundation-event-model"></a>使用媒體基礎事件模型

Windows Media DRM 用戶端擴充 Api 所支援的非同步方法會使用媒體基礎 SDK 所使用的相同事件模型。 每個支援非同步方法的物件都會實 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) 介面，而此介面可用來在非同步作業完成時，用來取得事件。

**IWMDRMEventGenerator** 介面繼承自 **IMFMediaEventGenerator** 介面，此介面記載于媒體基礎 SDK 檔集內。

[DRM 個人化範例](drm-individualization-example.md)中的範例程式碼會使用 **IMFMediaEventGenerator：： GetEvent** 方法，一次從佇列取出事件。 使用 **GetEvent** 比使用 **IMFMediaEventGenerator：： BeginGetEvent** 和 **IMFMediaEventGenerator：： EndGetEvent** 搭配回呼更簡單，讓程式碼範例更容易瞭解。 無論您是在程式碼中使用 **GetEvent** ，還是要執行 **IMFAsyncCallback** 並使用 **BeginGetEvent** 和 **EndGetEvent**，在收到事件之後處理事件的邏輯都是一樣的。

數個非同步方法會產生事件，其中包含可用於取得更詳細狀態資訊之物件的參考。 在這些情況下，產生的事件會有 **IUnknown** 指標做為其值，您可以查詢該指標以取得狀態介面。 下列清單摘要說明非同步呼叫、產生的事件和其他介面之間的關聯性。

-   [**IWMDRMLicenseManagement：： BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)方法會產生具有相關 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的 **MEWMDRMLicenseBackupProgress** 事件。
-   [**IWMDRMLicenseManagement：： RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)方法會產生具有相關 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的 **MEWMDRMLicenseRestoreProgress** 事件。
-   [**IWMDRMSecurity：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md)方法是在用來執行個人化時，會產生具有相關 [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)介面的 **MEWMDRMIndividualizationProgress** 事件。
-   [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)方法用於準備非無訊息授權取得的資料時，會產生具有相關 [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)介面的 **MEWMDRMLicenseAcquisitionCompleted** 事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 的個人化範例**](drm-individualization-example.md)
</dt> <dt>

[**開始使用**](drm-getting-started.md)
</dt> <dt>

[媒體基礎 SDK 檔](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




