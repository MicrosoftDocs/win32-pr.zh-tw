---
title: Microsoft Windows Media DRM 用戶端結構
description: Microsoft Windows Media DRM 用戶端結構
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows Media Format SDK，結構
- 數位版權管理 (DRM) 、結構
- DRM (數位版權管理) 、結構
- DRM 用戶端擴充 Api，結構
- 用戶端擴充 Api，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43264c37ed9830026f87998823017d17c9d75f7e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383578"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Microsoft Windows Media DRM 用戶端結構

Windows Media DRM 用戶端擴充 Api 支援下列結構。



| 結構或列舉                                                                    | Description                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼**](drm-audio-output-protection-ids.md)              | 包含音訊輸出保護識別碼的清單。                                                                                                     |
| [**DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**](drm-audio-output-protection-ids-ex.md)       | 包含音訊輸出保護識別碼的清單。 此結構會藉由新增版本號碼來擴充 **DRM \_ 音訊 \_ 輸出 \_ 保護 \_ 識別碼** 。          |
| [**DRM \_ 複製 \_ OPL**](drmdrm-copy-opl.md)                                                   | 保存有關複製動作授權中所指定輸出保護層級的資訊。                                                               |
| [**DRM \_ 授權 \_ 狀態 \_ 資料**](drmdrm-license-state-data.md)                              | 包含 DRM 許可權之授許可權制的相關資訊。                                                                                        |
| [**DRM \_ 最小 \_ 輸出 \_ 保護 \_ 層級**](drmdrm-minimum-output-protection-levels.md) | 保存 (OPLs) 的最小輸出保護層級，以播放各種類型的內容。                                                                 |
| [**DRM \_ OPL \_ 輸出 \_ 識別碼**](drmdrm-opl-output-ids.md)                                      | 保存一些 OPL 輸出識別碼。                                                                                                                   |
| [**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)                                    | 保存輸出保護技術的相關資訊。                                                                                                    |
| [**DRM \_ 輸出 \_ 保護， \_ 例如**](drm-output-protection-ex.md)                             | 保存輸出保護技術的相關資訊。 此結構會藉由新增版本號碼來擴充 **DRM \_ 輸出 \_ 保護** 。                     |
| [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)                                                   | 保存有關播放動作授權中所指定之 OPLs 的資訊。                                                                                   |
| [**DRM \_ PLAY \_ OPL \_ 例如**](drm-play-opl-ex.md)                                               | 保存有關播放動作授權中所指定之 OPLs 的延伸資訊。                                                                          |
| [**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼**](drmdrm-video-output-protection-ids.md)           | 保存 **DRM \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。                                                                                            |
| [**DRM \_ 影片 \_ 輸出 \_ 保護 \_ 識別碼， \_ 例如**](drm-video-output-protection-ids-ex.md)       | 保存 **DRM \_ 影片 \_ 輸出 \_ 保護** 結構的陣列。 此結構會藉由新增版本號碼來擴充 **DRM \_ VIDEO \_ 輸出 \_ 保護 \_ 識別碼** 。 |
| [**WM \_ 備份 \_ 還原 \_ 狀態**](wm-backup-restore-status.md)                             | 保存有關暫止授權備份或還原作業的資訊。                                                                                      |
| [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md)                             | 保存有關暫止的個人化程式的資訊。                                                                                                |
| [**WMDRM \_ 類比 \_ 影片 \_ 限制**](wmdrm-analog-video-restrictions.md)               | 保存將內容播放為類比影片之限制的相關資訊。                                                                             |
| [**WMDRM \_ 類比 \_ 影片 \_ 限制， \_ 例如**](wmdrm-analog-video-restrictions-ex.md)        | 保存有關將內容播放為類比影片之限制的延伸資訊。                                                                    |
| [**WMDRM \_ 加密 \_ 散佈 \_ 區塊**](wmdrm-encrypt-scatter-block.md)                       | 包含要加密的資料區塊。                                                                                                                   |
| [**WMDRM \_ 加密 \_ 散佈 \_ 資訊**](wmdrm-encrypt-scatter-info.md)                         | 包含設定 [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) 介面以供使用所需的資訊。                                        |
| [**WMDRM \_ 授權 \_ 篩選**](wmdrm-license-filter.md)                                      | 包含用來建立授權列舉的篩選資訊。                                                                                           |
| [**WMDRM \_ 輸出 \_ 保護 \_ 層級**](wmdrm-output-protection-levels.md)                 | 包含授權用來執行各種動作所需的輸出保護層級。                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | 包含用來加密和解密內容之密碼編譯演算法的相關資訊。                                                                 |
| [**WMDRMNET \_ 原則**](wmdrmnet-policy.md)                                                 | 包含用於網路裝置作業之 Windows Media DRM 的原則。                                                                        |
| [**WMDRMNET \_ 原則的 \_ 全域 \_ 需求**](wmdrmnet-policy-global-requirements.md)       | 保留網路裝置的 Windows Media DRM 全域需求。                                                                                        |
| [**WMDRMNET \_ 原則的 \_ 最小 \_ 環境**](wmdrmnet-policy-minimum-environment.md)       | 包含網路裝置的 Windows Media DRM 的最低安全性需求。                                                                       |
| [**WMDRMNET \_ 原則 \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)                  | 保存針對網路裝置使用 Windows Media DRM 播放內容的原則資訊。                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](drm-programming-reference.md)
</dt> </dl>

 

 




