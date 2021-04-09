---
title: Individualizing DRM 應用程式
description: Individualizing DRM 應用程式
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media 格式 SDK，individualizing DRM 應用程式
- Windows Media Format SDK，應用程式 individualizing
- Advanced Systems Format (ASF) 、individualizing DRM 應用程式
- ASF (Advanced Systems Format) 、individualizing DRM 應用程式
- Advanced Systems Format (ASF) 、application individualizing
- ASF (Advanced Systems Format) 、application individualizing
- 數位版權管理 (DRM) 、individualizing 應用程式
- DRM (數位版權管理) 、individualizing 應用程式
- 數位版權管理 (DRM) 、應用程式 individualizing
- DRM (數位版權管理) 、應用程式 individualizing
- 應用程式 individualizing
- individualizing DRM 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "103933000"
---
# <a name="individualizing-drm-applications"></a>Individualizing DRM 應用程式

為了提高安全性，您可以將應用程式的 DRM 元件 *個人* 化。 個別的應用程式是已收到升級至其 DRM 元件的應用程式，這些元件會將它與相同應用程式的所有其他複本進行區別。 內容擁有者可以要求只能在已個人化的應用程式上播放其受保護的檔案。

當應用程式連線到 Microsoft 的「個人化服務」時（接著在使用者的電腦上安裝安全性升級），就會開始進行個人化程式。 由於「個人」服務會處理來自使用者的資訊，因此您必須在 Microsoft 網站上顯示 Microsoft 隱私權原則或提供該頁面的連結： <https://privacy.microsoft.com/privacystatement> 。

您可以用不同的方式來完成個人化。 例如，當使用者播放受保護的檔案時，就可以進行個人化。 授權要求會傳送至 [*Windows Media 授權服務*](wmformat-glossary.md)，此服務會檢查要求 [*授權*](wmformat-glossary.md)之應用程式的憑證。 如果應用程式的 DRM 元件尚未進行個人化，Windows Media License Service 會拒絕發出授權，因為這是 Windows Media License Service 的原則，只會將授權發行給個別的玩家。 然後，應用程式可以通知使用者必須升級應用程式。 如果使用者同意，則會提供安全性升級，以賦予應用程式的 DRM 元件。

為了獲得更好的使用者體驗，您可以在安裝期間以安全性升級步驟的形式起始您的個人化程式。然後，使用者在嘗試播放受保護的檔案時，不會中斷以取得安全性升級。 您也可以將 **安全性升級** 功能表命令或按鈕新增至應用程式，以主動地鼓勵使用。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




