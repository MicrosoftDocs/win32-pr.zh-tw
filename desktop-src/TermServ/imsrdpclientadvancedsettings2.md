---
title: IMsRdpClientAdvancedSettings2 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings 介面。
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97584aa3b37adc148672777e95fe0b2c8b101e09989bfa1ab5debbffe489640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001406"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>IMsRdpClientAdvancedSettings2 介面

管理 advanced client 設定。 衍生自 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) 介面。 此介面包含方法，可為遠端桌面 ActiveX 控制項取出並設定 advanced (選用) 屬性。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings2** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings2** 介面繼承自 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)。 **IMsRdpClientAdvancedSettings2** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings2** 介面具有這些屬性。



| 屬性                                                                                      | 存取類型           | 描述                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutoReconnect**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | 唯讀<br/>  | 指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。<br/>    |
| [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | 讀取/寫入<br/> | 指定當網路連線中斷時，是否要讓用戶端控制項自動重新連線到會話。<br/>            |
| [**MaxReconnectAttempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | 讀取/寫入<br/> | 指定在自動重新連接期間嘗試重新連接的次數。 這個屬性的有效值為0到200（含）。<br/> |



 

## <a name="remarks"></a>備註

此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

