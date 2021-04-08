---
title: IMsRdpClientShell2 介面
description: 公開從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端桌面連線用戶端的屬性。
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell2 介面遠端桌面服務
- IMsRdpClientShell2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685670"
---
# <a name="imsrdpclientshell2-interface"></a>IMsRdpClientShell2 介面

公開從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端桌面連線用戶端的屬性。

此介面是由遠端桌面服務 Web 存取控制項所執行，這是遠端桌面連線用戶端 (MsTscAx.dll) 和 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 周圍的包裝函式。

## <a name="members"></a>成員

**IMsRdpClientShell2** 介面繼承自 **IMsRdpClientShell**。 **IMsRdpClientShell2** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientShell2** 介面具有這些屬性。



| 屬性                                                                               | 存取類型          | Description                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | 唯讀<br/> | 抓取 [**IMsRdpWorkspace**](imsrdpworkspace.md) 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | 唯讀<br/> | 抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。<br/>                                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





