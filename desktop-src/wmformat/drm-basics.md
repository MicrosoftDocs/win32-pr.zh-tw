---
title: DRM 基本概念
description: DRM 基本概念
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK，DRM 基本概念
- 數位版權管理 (DRM) ，關於
- DRM (數位版權管理) ，關於
- 數位版權管理 (DRM) ，保護內容
- DRM (數位版權管理) ，保護內容
- 數位版權管理 (DRM) ，封裝內容
- DRM (數位版權管理) ，封裝內容
- 數位版權管理 (DRM) ，讀取受保護的內容
- DRM (數位版權管理) ，讀取受保護的內容
- 保護內容
- 封裝內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372625"
---
# <a name="drm-basics"></a>DRM 基本概念

Windows Media DRM 技術從 Windows Media Format SDK 的觀點來看相當簡單。 SDK 的元件可以用來保護內容，以及播放受保護的內容。

## <a name="protecting-content"></a>保護內容

保護內容 (也稱為封裝內容) 涉及加密檔案的資料區段，並在檔案標頭中包含一些可讓播放程式解密內容的資訊。

若要加密內容，您需要索引鍵，這是用來植入加密演算法的值。 金鑰是由兩個部分所組成：金鑰種子 (或私密金鑰) ，以及 (或公開金鑰) 的金鑰識別碼。 金鑰種子是您用來編碼內容的秘密值。 金鑰識別碼是受保護檔案標頭中包含的公用值。

當檔案受到保護時，就無法在沒有授權的情況下解密。 授權包含指定受保護內容之使用條款的資訊。 授權條款是由內容擁有者決定，而且可以自訂以符合各種需求。 封裝檔案的過程中，有一部分是包含網頁的 URL，使用者可以在其中取得存取內容的授權。

## <a name="reading-protected-content"></a>讀取受保護的內容

若要讀取受保護的內容，內容的授權必須位於用戶端電腦上。 某些授許可權制是由 Windows Media Format SDK 的 DRM 元件在內部檢查，有些則必須由您的應用程式強制執行。

您可以使用 Windows Media Format SDK 的物件來協助使用者取得內容的授權，以及執行其他系統管理工作，例如更新 DRM 元件和備份授權。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




