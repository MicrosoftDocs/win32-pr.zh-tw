---
title: IMsRdpClientNonScriptable7 介面
description: 在遠端桌面 ActiveX 控制項上，提供用戶端遠端會話的 nonscriptable 屬性存取。 衍生自 IMsRdpClientNonScriptable6 介面。
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable7 介面遠端桌面服務
- IMsRdpClientNonScriptable7 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941105"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>IMsRdpClientNonScriptable7 介面

在遠端桌面 ActiveX 控制項上，提供用戶端遠端會話的 nonscriptable 屬性存取。 衍生自 [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) 介面。 這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。

藉由呼叫 [**IMsTscAx**](imstscax-interface.md)物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得這個介面的實例，並傳遞 **IID \_ IMsRdpClientNonScriptable7**。

## <a name="members"></a>成員

**IMsRdpClientNonScriptable7** 介面繼承自 [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md)。 **IMsRdpClientNonScriptable7** 也有下列類型的成員：

- [方法](#methods)
- [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClientNonScriptable7** 介面具有這些方法。


| 方法            | 描述              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。                   |

### <a name="properties"></a>屬性

**IMsRdpClientNonScriptable7** 介面具有這些屬性。

| 屬性         | 存取類型           | 描述            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | 唯讀 |  取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。   |
| [**剪貼簿**](imsrdpclientnonscriptable7-clipboard.md)                       | 唯讀 |    如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。    |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 定義為0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting 定義為3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 定義為22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting 定義為1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
