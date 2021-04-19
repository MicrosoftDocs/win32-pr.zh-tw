---
title: 授權預先傳遞
description: 授權預先傳遞
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK，預先傳遞的授權
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、預先傳遞的授權
- DRM (數位版權管理) 、預先傳遞的授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api、預先傳遞的授權
- 用戶端擴充的 Api，預先傳遞的授權
- 預先傳遞的授權
- 授權、預先傳遞的授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968923"
---
# <a name="license-pre-delivery"></a>授權預先傳遞

授權預先傳遞是用來將授權提取至用戶端電腦事先的流程。 使用預先傳遞的常見案例是當使用者訂閱音樂服務時。 若未在需要的情況下傳遞授權，使用者就必須等候每個新歌曲的授權取得。

由於未在嘗試存取的情況下傳遞預先傳遞，因此通常只會由內容擁有者執行。 也就是說，您只能針對您所控制的內容預先提供授權。 預先傳遞程式是用戶端元件與使用 Windows Media 數位 Rights Management SDK 的物件所建立的授權伺服器之間的協調。

授權預先傳遞與 [非無訊息授權](non-silent-license-acquisition.md)取得類似。 遵循相同的步驟，但您沒有要傳遞至 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)的 DRM 標頭。 方法將會產生不是內容特定的挑戰，您可以傳送給授權伺服器。

或者，您可以使用 [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) 來預先傳遞授權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**取得授權**](acquiring-licenses.md)
</dt> <dt>

[**使用媒體基礎事件模型**](using-the-media-foundation-model.md)
</dt> </dl>

 

 