---
title: DRM 保護和內容授權發佈
description: DRM 保護和內容授權發佈
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows媒體格式 SDK，DRM 內容保護
- Windows媒體格式 SDK，DRM 授權
- Advanced Systems Format (ASF) ，DRM 內容保護
- ASF (Advanced Systems Format) ，DRM 內容保護
- Advanced Systems Format (ASF) ，DRM 授權發佈
- ASF (Advanced Systems Format) ，DRM 授權發佈
- 數位版權管理 (DRM) ，內容保護
- DRM (數位版權管理) 、內容保護
- 數位版權管理 (DRM) 、授權發佈
- DRM (數位版權管理) 、授權發佈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704312"
---
# <a name="drm-protection-and-content-license-distribution"></a>DRM 保護和內容授權發佈

在建立端，數位版權管理技術牽涉到兩個主要的程式： (1) 保護內容和 (2) 提供內容的授權。 保護檔案基本上涉及加密內容，並在檔案標頭中包含 URL，以指定可能取得內容授權的位置。 如果您想要使用保護檔案，然後將檔案發佈到其他電腦或裝置，您可以使用 Windows 媒體格式 sdk 或 Windows media Rights Manager sdk 來保護檔案。 針對即時 DRM 案例，您必須使用 Windows 媒體格式 SDK 來保護其編碼的內容。

若要建立併發行受保護內容的授權，您可以使用 Windows Media Rights Manager SDK 的物件來建立自己的自訂解決方案，也可以使用由協力廠商執行的服務。

無論您使用哪種方法，您所建立的受保護檔案都會包含在 DRM 標頭物件中，此 URL 會告知用戶端應用程式在何處取得內容的授權。

> [!Note]  
> Windows 媒體格式 SDK 不提供建立或發行授權的支援。

 

在播放端，啟用 DRM 的應用程式必須能夠取得受保護內容的授權、使用授權中所含的金鑰將該內容解密，以及強制執行授許可權制（例如檔案可能播放的次數），或是否可將檔案複製到其他裝置。 Windows 媒體格式 SDK 提供建立完全啟用的 DRM 播放應用程式所需的所有支援。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




