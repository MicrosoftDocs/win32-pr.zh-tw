---
title: IMsRdpClientSecuredSettings 介面
description: 包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。 |IMsRdpClientSecuredSettings 介面
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- IMsRdpClientSecuredSettings 介面遠端桌面服務
- IMsRdpClientSecuredSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991422"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>IMsRdpClientSecuredSettings 介面

包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。

## <a name="members"></a>成員

**IMsRdpClientSecuredSettings** 介面繼承自 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)。 **IMsRdpClientSecuredSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientSecuredSettings** 介面具有這些屬性。



| 屬性                                                                                   | 存取類型           | Description                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | 讀取/寫入<br/> | 音訊重新導向設定。<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | 讀取/寫入<br/> | 鍵盤重新導向設定。<br/> |



 

## <a name="remarks"></a>備註

連接控制項時無法設定這些屬性。

如需此介面之方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





