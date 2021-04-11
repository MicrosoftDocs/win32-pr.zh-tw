---
title: IMsRdpCameraRedirConfigCollection 介面
description: 代表 (的相機集合，以及可用於重新導向的相關聯設定) 。
ms.tgt_platform: multiple
keywords:
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108356"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>IMsRdpCameraRedirConfigCollection 介面

 代表 (的相機集合，以及可用於重新導向的相關聯設定) 。

## <a name="members"></a>成員

**IMsRdpCameraRedirConfigCollection** 介面繼承自 **IUnknown**。 **IMsRdpCameraRedirConfigCollection** 也有下列類型的成員：

- [方法](#methods)
- [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpCameraRedirConfigCollection** 介面具有這些方法。

| 方法            | 描述              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  將 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件新增至集合 (對應的相機不需要連線) 。                   |
| [**重新掃描**](imsrdpcameraredirconfigcollection-rescan.md)       |  列舉連線的相機裝置。                   |

### <a name="properties"></a>屬性

**IMsRdpCameraRedirConfigCollection** 介面具有這些屬性。

| 屬性         | 存取類型           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | 唯讀 |  依物件在集合中的索引傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | 唯讀 |    從集合中傳回對應至指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | 唯讀 |  從集合中傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。  |
| [**計數**](imsrdpcameraredirconfigcollection-count.md)                       | 唯讀 |    傳回集合中的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件數目。   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | 讀取/寫入 |  指定影片資料流程是否為 h.264 編碼。  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | 讀取/寫入 |    指定編碼品質 (位速率) 。   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | 讀取/寫入 |   指定是否根據預設，將任何新的相機重新導向。    |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A            |

## <a name="see-also"></a>另請參閱

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
