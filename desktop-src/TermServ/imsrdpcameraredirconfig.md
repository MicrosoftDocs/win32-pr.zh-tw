---
title: IMsRdpCameraRedirConfig 介面
description: 表示可用來重新導向的相機設定。
ms.tgt_platform: multiple
keywords:
- IMsRdpCameraRedirConfig 介面遠端桌面服務
- IMsRdpCameraRedirConfig 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104509738"
---
# <a name="imsrdpcameraredirconfig-interface"></a>IMsRdpCameraRedirConfig 介面

表示可用來重新導向的相機設定。

## <a name="members"></a>成員

**IMsRdpCameraRedirConfig** 介面繼承自 **IUnknown**。 **IMsRdpCameraRedirConfig** 也有下列類型的成員：

- [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpCameraRedirConfig** 介面具有這些屬性。

| 屬性         | 存取類型           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | 唯讀 | 指定相機裝置目前是否存在 (也就是相機連線) 。   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | 唯讀 |    取得相機的易記名稱。    |
| [**Id**](imsrdpcameraredirconfig-instanceid.md)      | 唯讀 |  取得相機的實例識別碼。  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | 唯讀 |    取得相機的父裝置實例識別碼。   |
| [**已重新導向**](imsrdpcameraredirconfig-redirected.md)      | 讀取/寫入 |  指定是否將相機重新導向。  |
| [**>symboliclink**](imsrdpcameraredirconfig-symboliclink.md)                       | 唯讀 |   取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。   |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>另請參閱

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)