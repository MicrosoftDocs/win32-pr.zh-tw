---
title: IMsRdpClientNonScriptable6 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable5 介面。
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable6 介面遠端桌面服務
- IMsRdpClientNonScriptable6 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104385486"
---
# <a name="imsrdpclientnonscriptable6-interface"></a>IMsRdpClientNonScriptable6 介面

提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) 介面。 這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。

藉由呼叫 [**IMsTscAx**](imstscax-interface.md)物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得這個介面的實例，並傳遞 **IID \_ IMsRdpClientNonScriptable6**。

## <a name="members"></a>成員

**IMsRdpClientNonScriptable6** 介面繼承自 [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)。 **IMsRdpClientNonScriptable6** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**IMsRdpClientNonScriptable6** 介面具有這些方法。


| 方法            | 描述                   |
|:-----------------------------|:-----------------|
| [**SendLocation2D**](imsrdpclientnonscriptable6-sendlocation2d.md)     |  將緯度和經度值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。                   |
| [**SendLocation3D**](imsrdpclientnonscriptable6-sendlocation3d.md)     | 將緯度、經度和海拔值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。                 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1709 版 (組建 16299)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | CLSID \_ MsRdpClient12 定義為0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> CLSID \_ MsRdpClient12NotSafeForScripting 定義為3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> CLSID \_ MsRdpClient11 定義為22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> CLSID \_ MsRdpClient11NotSafeForScripting 定義為1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable6 定義為 05293249-B28B-4DB8-BE64-1B2F496B910E            |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>
