---
title: IMsRdpWorkspace2 介面
description: 公開將 RemoteApp 和桌面連線認證與連接產生關聯的方法。
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125518"
---
# <a name="imsrdpworkspace2-interface"></a>IMsRdpWorkspace2 介面

公開將 RemoteApp 和桌面連線認證與連接產生關聯的方法。 這個介面是由遠端桌面服務 Web 存取控制項所執行。 此控制項是遠端桌面連線用戶端 (MsTscAx.dll) 的包裝函式，以及 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 。

## <a name="members"></a>成員

**IMsRdpWorkspace** 介面繼承自 [**IMsRdpWorkspace**](imsrdpworkspace.md)。 **IMsRdpWorkspace2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMsRdpWorkspace** 介面具有這些方法。



| 方法                                                        | 描述                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | 將使用者認證和憑證與連接識別碼產生關聯。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 定義為145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

