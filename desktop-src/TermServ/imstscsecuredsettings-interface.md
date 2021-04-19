---
title: IMsTscSecuredSettings 介面
description: 包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。 |IMsTscSecuredSettings 介面
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- IMsTscSecuredSettings 介面遠端桌面服務
- IMsTscSecuredSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997342"
---
# <a name="imstscsecuredsettings-interface"></a>IMsTscSecuredSettings 介面

包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。 屬性包括指定用戶端控制項模式 (全螢幕模式或視窗模式) ，以及在連接至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時啟動的程式。 您也可以透過 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面使用這些方法。

## <a name="members"></a>成員

**IMsTscSecuredSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsTscSecuredSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsTscSecuredSettings** 介面具有這些屬性。



| 屬性                                                              | 存取類型           | Description                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**FullScreen**](imstscsecuredsettings-fullscreen.md)<br/>     | 讀取/寫入<br/> | 用戶端控制項的全螢幕狀態。<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | 讀取/寫入<br/> | 連接時要在遠端伺服器上啟動的程式。<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | 讀取/寫入<br/> | 啟動程式的工作目錄。<br/>                     |



 

## <a name="remarks"></a>備註

如需此介面之方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

