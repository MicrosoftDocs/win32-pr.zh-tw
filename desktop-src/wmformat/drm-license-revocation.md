---
title: " (Microsoft Windows Media DRM 用戶端) 的授權撤銷"
description: " (Microsoft Windows Media DRM 用戶端) 的授權撤銷"
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK，授權
- Windows Media Format SDK，授權撤銷
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) 、授權撤銷
- DRM (數位版權管理) 、授權撤銷
- DRM 用戶端擴充 Api，授權
- 用戶端擴充 Api，授權
- DRM 用戶端擴充 Api，授權撤銷
- 用戶端擴充 Api，授權撤銷
- 授權，撤銷
- 授權撤銷，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195672"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a> (Microsoft Windows Media DRM 用戶端) 的授權撤銷

授權撤銷是指移除本機授權存放區中的授權。 當服務提供者（例如，音樂訂閱服務）必須停用使用者電腦上的服務時，就會發生授權撤銷的常見案例。

授權撤銷程式是由授權簽發者所提供的服務所起始。 您的應用程式可以裝載此服務，也可以是 Web 應用程式。 無論是哪一種情況，您的應用程式都必須能夠收到服務所建立的授權挑戰。

若要移除授權存放區的授權，請執行下列動作：

1.  收到授權簽發者的授權挑戰時，請使用 [**IWMDRMLicenseManagement：： CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) 方法建立撤銷挑戰。 這個方法會配置包含撤銷挑戰資料的緩衝區，此資料會透過 *ppbChallengeOutput* 參數傳遞至您的應用程式。
2.  將授權撤銷挑戰傳送到授權撤銷服務。 伺服器將會產生 (LRB) 的授權撤銷 BLOB 以回應。
3.  使用 [**IWMDRMLicenseManagement：:P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) 方法來移除本機存放區中的授權，並傳遞授權伺服器所傳回的 LRB。
4.  使用 **CoTaskMemFree** 函數，將 **CreateLicenseRevocationChallenge** 所配置的緩衝區解除配置。

如需有關授權撤銷的運作方式或如何撰寫撤銷服務的詳細資訊，請參閱 [實施授權撤銷](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**本機授權商店**](local-license-store.md)
</dt> <dt>

[**程式設計指南**](drm-programming-guide.md)
</dt> </dl>

 

 