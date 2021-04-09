---
title: IMsRdpWorkspace 介面
description: 公開管理 RemoteApp 和桌面連線認證和連接的方法。
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- IMsRdpWorkspace 介面遠端桌面服務
- IMsRdpWorkspace 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933998"
---
# <a name="imsrdpworkspace-interface"></a>IMsRdpWorkspace 介面

公開管理 RemoteApp 和桌面連線認證和連接的方法。 這個介面是由遠端桌面服務 Web 存取控制項所執行。 此控制項是遠端桌面連線用戶端 (MsTscAx.dll) 的包裝函式，以及 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 。

## <a name="members"></a>成員

**IMsRdpWorkspace** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsRdpWorkspace** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMsRdpWorkspace** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | 刪除與指定之連接識別碼相關聯的使用者認證。<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | 中斷與指定之連接識別碼相關聯的所有現有連接，並從認證存放區刪除對應的使用者認證。<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | 判斷指定之連接識別碼的使用者認證是否存在。<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | 判斷是否已啟用 RemoteApp 和桌面連線的單一登入 (SSO) 。<br/>                                                                   |
| [**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | 標示連接識別碼的使用者認證驗證，接著在工作列通知區域中顯示 connect 通知。 <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | 將使用者認證和憑證與連接識別碼產生關聯。<br/>                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace 定義為145D0621-04CF-4FC2-A766-A81A9069CDF8<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

