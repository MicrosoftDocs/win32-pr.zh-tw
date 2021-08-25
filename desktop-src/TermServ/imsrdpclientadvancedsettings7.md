---
title: IMsRdpClientAdvancedSettings7 介面
description: 公開管理 ActiveX 控制項之 advanced 設定的方法和屬性。
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5df2990a257d8f7fa544c24e33dba6a2422d2db8bea878f2487ca131e5bd607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866558"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>IMsRdpClientAdvancedSettings7 介面

公開管理 ActiveX 控制項之 advanced 設定的方法和屬性。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings7** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings7** 介面繼承自 **IMsRdpClientAdvancedSettings6**。 **IMsRdpClientAdvancedSettings7** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings7** 介面具有這些屬性。



| 屬性                                                                                                    | 存取類型           | 描述                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | 讀取/寫入<br/> | 指定或抓取值，指出是否將預設音訊輸入裝置從用戶端重新導向至遠端會話。<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | 讀取/寫入<br/> | 指定或抓取值，指出重新導向音訊的音訊品質模式設定。<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | 讀取/寫入<br/> | 指定或抓取值，指出 SuperPan 是否已啟用或停用。<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | 讀取/寫入<br/> | 指定或抓取表示網路連接類型的值。<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | 讀取/寫入<br/> | 不會使用此屬性。<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | 讀取/寫入<br/> | 指定或抓取表示 SuperPan 加速因素的值。<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | 讀取/寫入<br/> | 指定或抓取表示影片播放模式的值。<br/>                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

