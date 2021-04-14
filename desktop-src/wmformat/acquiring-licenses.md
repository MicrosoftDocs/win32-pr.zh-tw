---
title: 取得授權
description: 取得授權
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Media Format SDK，DRM 用戶端擴充 Api
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，擴充的 Api
- Windows Media Format SDK，Api
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，取得授權
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、用戶端擴充 Api
- DRM (數位版權管理) 、用戶端擴充 Api
- 數位版權管理 (DRM) 、擴充的 Api
- DRM (數位版權管理) 、擴充的 Api
- 數位版權管理 (DRM) 、Api
- DRM (數位版權管理) ，Api
- 數位版權管理 (DRM) ，取得授權
- DRM (數位版權管理) ，取得授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，取得授權
- 用戶端擴充 Api，取得授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371879"
---
# <a name="acquiring-licenses"></a>取得授權

取得授權的常見案例是當使用者擁有受保護的 Windows Media 檔案，且第一次嘗試存取內容時。 由於 Windows Media DRM 用戶端擴充 Api 與 ASF 檔案處理常式不同，因此在支援時，基本授權取得案例需要的 API 呼叫比使用 Windows Media 格式 SDK 和媒體基礎 SDK 更多。

本節說明如何使用 Windows Media DRM 用戶端擴充 Api 來取得在用戶端電腦上的本機授權存放區中儲存的授權。 其中包含下列主題。



| 主題                                                                | 描述                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [無訊息授權取得](silent-license-acquisition.md)         | 描述如何在不需要使用者介入的情況下取得授權。                                                                               |
| [取得非無訊息授權](non-silent-license-acquisition.md) | 描述如何在使用者介入 (（例如需要支付內容) ）時取得授權。                                     |
| [授權預先傳遞](license-pre-delivery.md)                     | 說明如何從授權伺服器提取授權給用戶端電腦。                                                                 |
| [在本機建立授權](creating-licenses-locally.md)           | 說明如何建立您自己的授權，而不需要從授權伺服器下載，以及如何將它們儲存在本機授權存放區中。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](drm-programming-guide.md)
</dt> </dl>

 

 




