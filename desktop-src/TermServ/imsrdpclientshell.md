---
title: IMsRdpClientShell 介面
description: 遠端桌面連線 (RDC) 用戶端設定，這些設定是用來從遠端桌面啟動用戶端 Web 存取 (RD Web 存取) 或從其他入口網站。
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell 介面遠端桌面服務
- IMsRdpClientShell 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466001"
---
# <a name="imsrdpclientshell-interface"></a>IMsRdpClientShell 介面

遠端桌面連線 (RDC) 用戶端設定，這些設定是用來從遠端桌面啟動用戶端 Web 存取 (RD Web 存取) 或從其他入口網站。

## <a name="members"></a>成員

**IMsRdpClientShell** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsRdpClientShell** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClientShell** 介面具有這些方法。



| 方法                                                     | 描述                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | 捕獲單一 RDP 屬性。<br/>                  |
| [**啟動**](imsrdpclientshell-launch.md)                 | 從 web 入口網站啟動遠端檔案內容。<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | 設定單一 RDP 屬性。<br/>                       |



 

### <a name="properties"></a>屬性

**IMsRdpClientShell** 介面具有這些屬性。



| 屬性                                                                                              | 存取類型           | Description                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | 唯讀<br/>  | 抓取遠端桌面連線 (RDC) 用戶端是否支援 RemoteApp 功能。<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | 讀取/寫入<br/> | 抓取是否啟用公用模式。<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | 讀取/寫入<br/> | RDP 設定檔的串流版本。<br/>                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

