---
title: IMsRdpClientAdvancedSettings6 介面
description: 公開管理 advanced ActiveX control 設定的屬性。
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966936"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a>IMsRdpClientAdvancedSettings6 介面

公開管理 advanced ActiveX control 設定的屬性。 **IMsRdpClientAdvancedSettings6** 介面衍生自 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)介面。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings6** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings6** 介面繼承自 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)。 **IMsRdpClientAdvancedSettings6** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings6** 介面具有這些屬性。



| 屬性                                                                                                  | 存取類型           | Description                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationServiceClass**](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | 讀取/寫入<br/> | 指定服務主體名稱 (SPN) 用來向伺服器進行驗證。<br/>                                     |
| [**AuthenticationType**](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | 唯讀<br/>  | 指定用於此連接的驗證類型。<br/>                                                          |
| [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | 讀取/寫入<br/> | 取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。<br/> |
| [**EnableCredSspSupport**](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | 讀取/寫入<br/> | 指定是否為此連線啟用 (CredSSP) 的認證安全性服務提供者。<br/>                    |
| [**HotKeyFocusReleaseLeft**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | 讀取/寫入<br/> | 指定要新增至 CTRL + ALT 的虛擬按鍵程式碼，以決定 CTRL + ALT + 向左鍵的替換熱鍵。<br/>          |
| [**HotKeyFocusReleaseRight**](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | 讀取/寫入<br/> | 指定要新增至 CTRL + ALT 的虛擬按鍵程式碼，以決定 CTRL + ALT + 向右鍵的熱鍵取代。<br/>         |
| [**Pcb**](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | 讀取/寫入<br/> | 指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。<br/>               |
| [**RelativeMouseMode**](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | 讀取/寫入<br/> | 指定滑鼠是否應使用相對模式。<br/>                                                                   |



 

## <a name="remarks"></a>備註

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)介面已擴充這個介面，繼承了先前介面的所有方法和屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

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

 

