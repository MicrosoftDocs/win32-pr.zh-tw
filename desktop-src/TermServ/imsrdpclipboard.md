---
title: IMsRdpClipboard 介面
description: 代表在啟用手動剪貼簿同步處理的情況下，用來同步處理本機和遠端寫字板的剪貼簿控制器。
ms.tgt_platform: multiple
keywords:
- IMsRdpClipboard 介面遠端桌面服務
- IMsRdpClipboard 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108368"
---
# <a name="imsrdpclipboard-interface"></a>IMsRdpClipboard 介面

代表在啟用手動剪貼簿同步處理的情況下，用來同步處理本機和遠端寫字板的剪貼簿控制器 (也就是說， [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) 屬性值設定為 **True**) 。

## <a name="members"></a>成員

**IMsRdpClipboard** 介面繼承自 **IUnknown**。 **IMsRdpClipboard** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IMsRdpClipboard** 介面具有這些方法。


| 方法        | 描述      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  指出本機剪貼簿是否可以同步到遠端會話。                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  指出遠端剪貼簿是否可同步處理至本機會話。                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  將本機剪貼簿同步到遠端會話。                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   將遠端剪貼簿同步處理至本機會話。                      |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable7：：剪貼簿**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
