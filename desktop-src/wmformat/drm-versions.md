---
title: DRM 版本
description: DRM 版本
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK，DRM 版本
- 數位版權管理 (DRM) ，版本
- DRM (數位版權管理) ，版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932071"
---
# <a name="drm-versions"></a>DRM 版本

有數種版本的 Windows Media 數位版權管理 (DRM) 。 DRM 第1版通常會與本檔中的其他版本分開設定，因為它是使用與較新版本不同的技術來實行。 第二次產生的 Windows Media DRM 稱為 DRM 第7版，因為它是 Windows Media Format 7 SDK 的一部分引進的。 有時也稱為 DRM 第2版。 較新版本的 Windows Media DRM （DRM 第9版和新的 Windows Media DRM 10）是 DRM 版本7的延伸模組，並使用相同的程式來執行。 所有版本的 Windows Media DRM 都使用相同的加密常式;版本之間的差異與授權功能有關。

當您使用 Windows Media Format SDK 的物件建立受保護的檔案時，您應該同時支援第1版與最新版本。 受 DRM 第1版保護的檔案，與受較新版的檔案（僅限於標頭的內容）所保護的檔案不同。 包含額外標頭資訊的較新檔案仍可在只轉譯第1版內容的用戶端上使用。 在較新版本的 DRM 提供較高層級的安全性和其他功能時，仍有許多使用第1版的播放機。

如需 DRM 版本的詳細資訊，請參閱 Windows Media Rights Manager SDK 檔。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




