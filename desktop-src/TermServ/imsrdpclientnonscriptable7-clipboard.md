---
title: IMsRdpClientNonScriptable7 剪貼簿屬性
description: 如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。
ms.tgt_platform: multiple
keywords:
- 剪貼簿屬性遠端桌面服務
- 剪貼簿屬性遠端桌面服務、IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，剪貼簿屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103935597"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a>IMsRdpClientNonScriptable7：：剪貼簿屬性

如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a>屬性值

如果啟用手動剪貼簿同步，則表示用來同步處理本機和遠端寫字板的剪貼簿控制器的 [IMsRdpClipboard](imsrdpclipboard.md) ， (也就是 [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) 屬性值設定為 **True**) 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>