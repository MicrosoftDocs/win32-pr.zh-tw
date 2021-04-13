---
title: DRM 的個人化
description: DRM 的個人化
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK，DRM 的個人化
- 數位版權管理 (DRM) 、個人化
- DRM (數位版權管理) 、個人化
- DRM 的個人化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300452"
---
# <a name="drm-individualization"></a>DRM 的個人化

受保護內容的擁有者可能會要求使用者在存取其內容之前，先升級 Windows Media Format SDK 中包含的一些數位版權管理 (DRM) 元件。 如果使用者接受升級，則會從 Microsoft 網站下載安全性檔案的個人化版本 (唯一的電腦) 。 如果使用者拒絕升級，則不能存取內容;不過，他們仍然可以存取未受保護的內容，以及不需要升級的受保護內容。 執行安全性升級有助於提高 DRM 所提供的保護層級。

在安裝期間，或是當應用程式第一次遇到需要的 protected ASF 檔案時，就可以進行個人化。 因為此程式會修改使用者的系統元件，所以在執行升級之前，應用程式必須通知使用者並取得其告知同意。 例如，Microsoft Windows Media Player 會顯示具有下列文字的對話方塊：

**需要安全性升級**

**您嘗試存取的受保護內容的擁有者，必須先在電腦上升級部分 Microsoft 數位版權管理 (DRM) 元件。**

**按一下 [確定] 升級 DRM 元件。**

**細節：**

**當您按一下 [確定] 時，會將唯一識別碼和 DRM 安全性檔案傳送至網際網路上的 Microsoft 服務。檔案會取代為包含唯一識別碼的自訂版本。這會增加 DRM 所提供的保護層級。**

任何支援個人化的應用程式都應該使用相同或類似的用語。 如需 Microsoft 隱私權原則的詳細資訊，請參閱本檔的 [隱私權聲明](privacy-statement.md) 一節。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**Individualizing DRM 應用程式**](individualizing-drm-applications.md)
</dt> </dl>

 

 




