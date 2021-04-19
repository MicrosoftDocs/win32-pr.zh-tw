---
title: 啟用 DRM 支援
description: 啟用 DRM 支援
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows Media Format SDK，啟用 DRM 支援
- Advanced Systems Format (ASF) ，啟用 DRM 支援
- ASF (Advanced Systems Format) ，啟用 DRM 支援
- 數位版權管理 (DRM) ，啟用支援
- DRM (數位版權管理) ，啟用支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106979673"
---
# <a name="enabling-drm-support"></a>啟用 DRM 支援

您可以使用 Microsoft Windows Media Format 軟體發展工具組 (SDK) 來建立應用程式，這些應用程式可以套用數位版權管理 (DRM) 保護，以及播放即時 DRM 串流或受 DRM 保護的檔案。 也提供針對備份和還原播放程式的 DRM 授權，以及 [*individualizing*](wmformat-glossary.md) 播放程式的支援。

本檔假設您對 Microsoft 的數位版權管理技術有基本的熟悉度。 本檔的 [數位 Rights Management 功能](digital-rights-management-features.md) 一節提供 WINDOWS Media DRM 的基本總覽。 如需 DRM 的詳細資訊，請參閱 [Microsoft](https://windows.microsoft.com/windows/products/windows-media)網站上的數位 Rights Management 頁面。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

下列各節說明如何啟用 DRM 支援。



| 區段                                                                                                                        | 描述                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [取得必要的 DRM 程式庫](obtaining-the-required-drm-library.md)                                                   | 描述取得建立啟用 DRM 的應用程式所需的靜態程式庫時所需的步驟。                                                                               |
| [DRM 保護和內容授權發佈](drm-protection-and-content-license-distribution.md)                         | 比較 Windows Media Format SDK 與 Windows Media Rights Manager SDK 的 DRM 功能。                                                                                        |
| [DRM 網路作業](drm-network-operations.md)                                                                           | 描述您的應用程式應該如何處理透過網際網路或其他網路通訊的 DRM 作業。                                                                          |
| [建立受保護的檔案](creating-protected-files.md)                                                                       | 說明如何建立受 DRM 保護的檔案。                                                                                                                                                    |
| [讀取受保護的檔案](reading-protected-files.md)                                                                         | 描述取得內容授權的方法，以及執行無訊息授權取得的優點。                                                                                     |
| [查看受保護檔案的屬性](viewing-attributes-of-protected-files.md)                                             | 描述如何使用 [中繼資料編輯器] 物件上的 [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) 介面來查看受保護檔案的屬性，而不需要 DRM 的必要靜態程式庫。 |
| [使用撤銷清單](working-with-revocation-lists.md)                                                             | 描述撤銷清單及其執行方式。                                                                                                                                        |
| [備份和還原授權](backing-up-and-restoring-licenses.md)                                                     | 描述使用者如何藉由備份和還原到目前的電腦或其他電腦，來管理其內容授權。                                                         |
| [Individualizing DRM 應用程式](individualizing-drm-applications.md)                                                       | 描述 [*如何在 DRM*](wmformat-glossary.md) 系統中提高安全性。                                                           |
| [使用輸出保護層級](working-with-output-protection-levels.md)                                             | 說明如何支援輸出保護層級，這些層級可用來記錄 DRM 版本10授權中的允許動作。                                                                         |
| [使用 Windows Media DRM 10 進行網路裝置通訊協定](using-the-windows-media-drm-10-for-network-devices-protocol.md) | 說明如何使用適用于網路裝置的 Windows Media DRM 10 通訊協定來支援安全裝置串流。                                                                                |
| [執行授權撤銷](implementing-license-revocation.md)                                                         | 描述授權撤銷的程式，以及您的應用程式必須採取才能執行的動作。                                                                                        |
| [燒錄包含安全檔案的播放清單](burning-playlists-that-contain-secure-files.md)                                 | 描述如何在您的應用程式中執行播放清單燒錄。                                                                                                                                |



 

SDK 包含數個範例應用程式，示範如何讀取受保護的檔案;最完整的範例是 DRMShow。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**特性**](features.md)
</dt> </dl>

 

 




