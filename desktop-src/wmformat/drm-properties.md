---
title: DRM 屬性
description: DRM 屬性
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows媒體格式 SDK，DRM 屬性
- Advanced Systems Format (ASF) ，DRM 屬性
- ASF (Advanced Systems Format) ，DRM 屬性
- 數位版權管理 (DRM) ，屬性
- DRM (數位版權管理) ，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d553d644a6f3ec7130262d0e8567a4aa6ceab53286b24248607b1928991f51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848264"
---
# <a name="drm-properties"></a>DRM 屬性

下表列出應用程式在寫入或讀取受保護的檔案時可以取得或設定的 DRM 屬性。 這些屬性不是檔案屬性;它們不會寫入至 ASF 檔案標頭。



| DRM 屬性                                                                             | 全域識別碼                               | 資料類型             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**DRM \_ ActionAllowed**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ 備份**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ 備份              | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ 複製**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ 播放**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ 播放            | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ ActionAllowed \_ PlaylistBurn**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn        | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ BaseLicenseAcqURL**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **WMT \_ 類型 \_ 字串** |
| [**DRM \_ 旗標**](drm-flags.md)                                                          | g \_ wszWMDRM \_ 旗標                              | **WMT \_ 類型 \_ DWORD**  |
| [**DRM \_ HeaderSignPrivKey**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **WMT \_ 類型 \_ 字串** |
| [**DRM \_ IsDRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ IsDRMCached**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **WMT \_ 類型 \_ BOOL**   |
| [**DRM \_ KeySeed**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **WMT \_ 類型 \_ 字串** |
| [**DRM \_ 層級**](drm-level.md)                                                          | g \_ wszWMDRM \_ 層級                              | **WMT \_ 類型 \_ DWORD**  |
| [**DRM \_ LicenseID**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **WMT \_ 類型 \_ 字串** |
| [**DRM \_ LicenseState**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **WMT \_ 類型 \_ DWORD**  |
| [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ 複製**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ 播放**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ 播放             | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ LicenseState \_ PlaylistBurn**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | **WMT \_ 類型 \_ 二進位** |
| [**DRM \_ 許可權**](drm-rights.md)                                                        | g \_ wszWMDRM \_ 許可權                             | **WMT \_ 類型 \_ 字串** |
| [**DRM \_ SAPLEVEL**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **WMT \_ 類型 \_ 字串** |
| [**使用 \_ Advanced \_ DRM**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **WMT \_ 類型 \_ BOOL**   |
| [**使用 \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **WMT \_ 類型 \_ BOOL**   |
| [**WMDRMNET \_ 撤銷**](wmdrmnet-revocation.md)                                      | g \_ wszWMDRMNET \_ 撤銷                      | **WMT \_ 類型 \_ 字串** |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> </dl>

 

 




