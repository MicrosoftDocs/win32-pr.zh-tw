---
title: Windows Media DRM 總覽
description: Windows Media DRM 總覽
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- 'Windows Media 格式 SDK、數位版權管理 (DRM) '
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- 數位版權管理 (DRM) ，關於
- DRM (數位版權管理) ，關於
- 數位版權管理 (DRM) ，封裝 Windows Media 檔案
- DRM (數位版權管理) ，封裝 Windows Media 檔案
- 數位版權管理 (DRM) 、受保護的檔案授權
- DRM (數位版權管理) 、受保護的檔案授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) ，讀取受保護的檔案
- DRM (數位版權管理) ，讀取受保護的檔案
- 'Advanced Systems Format (ASF) 、數位版權管理 (DRM) '
- 'ASF (Advanced Systems Format) 、數位版權管理 (DRM) '
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106983281"
---
# <a name="overview-of-windows-media-drm"></a>Windows Media DRM 總覽

Windows Media 數位 Rights Management (DRM) 是保護 Windows Media 檔案中的內容，讓未經授權的使用者無法存取的系統。 基本 DRM 週期有三個階段：封裝、授權和讀取。

## <a name="packaging-windows-media-files"></a>封裝 Windows Media 檔案

Windows Media DRM 是設計用來處理 Windows Media 檔案。 Windows Media 檔案是符合 Advanced Systems 格式的檔案 (ASF) 規格，而且只包含使用 Windows Media 音訊和影片編解碼器壓縮的音訊和影片。

將 ASF 檔案封裝之後，會在標頭中加入 DRM 特定區段。 DRM 標頭包含金鑰識別碼，可識別授權用途的內容，以及取得授權取得 URL，這是網頁的位址，可發出授權以讀取受保護的內容。 還有更多可放在 DRM 標頭中的資訊，但它是選擇性的。 DRM 標頭已簽署，因此可以驗證封裝程式。

在封裝程式期間會加密 ASF 檔案中的內容。 但是，即使用戶端沒有授權，也可以使用封裝檔案中的下列資訊：

-   儲存在 ASF 標頭中的中繼資料。
-   某些儲存在 DRM 標頭中的中繼資料 (例如，您一律可以) 取得授權取得 URL。

## <a name="licensing-protected-files"></a>授權受保護的檔案

若要讀取封裝的檔案，必須將授權發行至用戶端電腦。 授權是一組資料，其描述可讀取受保護檔案中資料的條件。 最常見的情況是，針對受保護的檔案發出授權，以回應嘗試在檔案上執行某些作業的使用者。 不過，授權簽發者也可以在明確要求之前，將授權傳遞給用戶端。 如需授權的詳細資訊，請參閱 [授權](licenses.md)。

## <a name="reading-data-from-protected-files"></a>從受保護的檔案讀取資料

當使用者嘗試在受保護的檔案上執行作業時 (播放、燒錄至 CD、複製到裝置等) ，應用程式必須檢查用戶端電腦上的內容授權。 如果用戶端電腦上有有效的授權，則可以繼續執行此操作。 如果沒有內容的授權，或用戶端電腦上沒有內容的授權允許要求的動作，則必須取得授權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows Media DRM 用戶端擴充 Api**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




