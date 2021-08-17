---
title: IMsRdpClientAdvancedSettings3 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings2 介面。
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df13ccfb0d955714984af82daaf693522ee7d61af9c608107c53dc9f5464b591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001376"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>IMsRdpClientAdvancedSettings3 介面

管理 advanced client 設定。 衍生自 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面。 此介面包含方法，可為遠端桌面 ActiveX 控制項取出並設定 advanced (選用) 屬性。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings3** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings3** 介面繼承自 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)。 **IMsRdpClientAdvancedSettings3** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings3** 介面具有這些屬性。



| 屬性                                                                                                            | 存取類型           | 描述                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**ConnectionBarShowMinimizeButton**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | 讀取/寫入<br/> | 指定是否要在連接列上顯示 [ **最小化** ] 按鈕。<br/> |
| [**ConnectionBarShowRestoreButton**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | 讀取/寫入<br/> | 指定是否要在連接列上顯示 [ **還原** ] 按鈕。<br/>  |



 

## <a name="remarks"></a>備註

此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 定義為19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

