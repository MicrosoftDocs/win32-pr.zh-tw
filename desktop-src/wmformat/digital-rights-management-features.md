---
title: 數位 Rights Management 功能
description: 數位 Rights Management 功能
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows媒體格式 SDK，DRM 功能
- 數位版權管理 (DRM) ，功能
- DRM (數位版權管理) ，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e389efdbfd3edef3f3c881cab8482c8ed03b6bb09eb4a7773caa59b4b9b1ad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704867"
---
# <a name="digital-rights-management-features"></a>數位 Rights Management 功能

\[Windows 媒體 DRM 功能已被取代，不應該使用。 請改用[Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]

數位版權管理 (DRM) 是一種技術，內容擁有者可以使用金鑰來加密數位媒體檔案， (一段資料來鎖定和解除鎖定內容) 。 若要播放受保護的 ASF 檔案，取用者必須取得包含金鑰的個別授權。 每份授權也包含內容擁有者或授權簽發者所決定的許可權，以指定取用者如何使用該檔案。 內容擁有者可以使用 DRM 技術，透過網際網路以受保護的檔案格式傳遞歌曲、影片和其他數位媒體檔案，並控制其數位內容的使用方式。 Windows 媒體版權管理員、Windows 媒體編碼器和 Windows Media Player 也支援 Microsoft DRM 技術。 如需有關 microsoft DRM 技術的詳細背景資訊，請參閱[microsoft Windows 媒體](https://support.microsoft.com/help/17946/windows-media)網站。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

下列各節討論 Windows 媒體格式 SDK 的主要 DRM 相關功能。



| 區段                                                                                            | 描述                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [DRM 基本概念](drm-basics.md)                                                                       | 提供 Windows 媒體格式 SDK 所提供之 DRM 功能的簡短總覽。                                         |
| [DRM 版本](drm-versions.md)                                                                   | 說明可用於應用程式之 DRM 保護版本之間的主要差異。                                     |
| [即時 DRM](live-drm.md)                                                                           | 描述「即時」 DRM 保護所能實現的案例。                                                                |
| [DRM 的個人化](drm-individualization.md)                                                 | 描述 DRM 內容擁有者或授權簽發者所能要求的應用程式安全性升級。                                   |
| [備份與還原 DRM 授權](backing-up-and-restoring-of-drm-licenses.md)           | 說明允許使用者備份和還原其內容授權的優缺點。                                       |
| [在中繼資料編輯器中查看 DRM 屬性](viewing-drm-attributes-in-the-metadata-editor.md) | 描述此 DRM helper 物件的功能，以及其設計來支援的案例。                                   |
| [輸出保護層級](output-protection-levels.md)                                           | 描述輸出保護層級如何讓 DRM 版本10授權更具彈性。                                                   |
| [授權撤銷](license-revocation.md)                                                       | 描述授權撤銷。                                                                                                        |
| [Windows網路裝置的媒體 DRM 10](windows-media-drm-10-for-network-devices.md)           | 導入了 Windows 媒體 DRM 10 用於網路裝置及其在此 SDK 中的執行。                                              |
| [Microsoft 安全音訊路徑](microsoft-secure-audio-path--deprecated.md)                         | 描述 Microsoft 安全音訊路徑架構，它可為受保護的音訊內容提供最高程度的保護。 |
| [播放清單燒錄](playlist-burning.md)                                                           | 描述 DRM 的播放清單燒錄功能，以及 Windows 媒體格式 SDK 的支援方式。                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**特性**](features.md)
</dt> </dl>

 

 