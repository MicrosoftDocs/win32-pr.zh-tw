---
title: '新功能 (Windows Media Format 11 SDK) '
description: 新功能
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK，新功能
- Windows Media Format SDK，功能
- Windows Media Format SDK，新功能
- Windows Media Format SDK，用戶端擴充 Api
- Windows Media Format SDK，DRM 更新
- Windows Media Format SDK，編解碼器更新
- Windows Media Format SDK，縮圖影像
- 數位版權管理 (DRM) 、新功能
- DRM (數位版權管理) 、新功能
- 縮圖影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685408"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>新功能 (Windows Media Format 11 SDK) 

Windows Media Format 11 SDK 引進新的數位版權管理 (DRM) 功能。 自9.5 版開始，已對 SDK 進行下列變更。

## <a name="windows-media-drm-client-extended-apis"></a>Windows Media DRM 用戶端擴充 Api

Windows Media Format 11 SDK 隨附一組新的 DRM Api。 這些 Api 會在自己的程式庫中執行。 Windows Media DRM 用戶端擴充 Api 也支援 Windows Media 格式 SDK 的物件所支援的許多 DRM 功能。 新 Api 的主要差異在於它們不會依賴有 ASF 檔案可運作。 相反地，新的 Api 會直接處理本機授權存放區，通常會使用金鑰識別碼來識別授權。

如需詳細資訊，請參閱 [Windows MEDIA DRM 用戶端擴充 api](windows-media-drm-client-extended-apis.md) 檔。

## <a name="updated-codecs"></a>已更新編解碼器

已更新 Windows Media 視訊 9 Advanced Profile 編解碼器，以產生符合已發行之 SMPTE VC-1 標準的壓縮位資料流程。

這一版的 SDK 也包含 Windows Media 音訊 10 Professional 編解碼器。 新的音訊編解碼器功能以較低的位元速率提高品質。

## <a name="thumbnail-right"></a>縮圖右邊

應用程式可以要求新的 DRM 動作以從影片讀取，以建立縮圖影像。 這可讓應用程式建立及顯示影片檔案的縮圖影像，而不需要開啟檔案以供播放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




