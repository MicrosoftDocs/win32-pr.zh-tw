---
description: 安全物件是可以有安全描述項的物件。
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: 安全物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93af0153082a5e94577e96e3b3f85c30ced8775aa8617bff84db37c96904d814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780503"
---
# <a name="securable-objects"></a>安全物件

安全物件是可以有 [安全描述項](security-descriptors.md)的物件。 所有命名 Windows 物件都是安全的。 某些未命名的物件（例如 [*處理*](/windows/desktop/SecGloss/p-gly) 程式和執行緒物件）也可以有安全描述項。 對於大部分的安全物件而言，您可以在建立物件的函式呼叫中指定物件的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 。 例如，您可以在 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 和 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數中指定安全描述項。

此外，Windows 安全性函式可讓您取得及設定在非 Windows 的作業系統上建立之安全物件的安全性資訊。 Windows 安全性函式也支援使用安全描述項搭配私用應用程式定義的物件。 如需私用安全物件的詳細資訊，請參閱 [用戶端/伺服器存取控制](client-server-access-control.md)。

每種安全物件類型都會定義自己的一組特定 [存取權限](access-rights-and-access-masks.md) ，以及自己 [的一般存取權限對應](generic-access-rights.md)。 如需每一種安全物件類型的特定和一般存取權限的相關資訊，請參閱該物件類型的總覽。

下表顯示用來操作一些常見安全物件安全性資訊的函式。



| 物件型別                                                                                                                                           | 安全描述項函式                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NTFS 檔案系統上的檔案[或目錄](/windows/desktop/FileIO/file-security-and-access-rights)                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [具名管道](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [匿名管道](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [處理序](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [執行緒](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [檔案對應物件](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [存取權杖](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)、 [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| 視窗管理物件 ([視窗工作站](/windows/desktop/winstation/window-station-security-and-access-rights) 和 [桌上型電腦](/windows/desktop/winstation/desktop-security-and-access-rights))  | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [登錄機碼](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Windows 服務](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| 本機或遠端印表機                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| 網路共用                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [進程間同步處理物件](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (事件、mutex、信號和可等候計時器)      | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [工作物件](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)、 [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| 目錄服務物件                                                                                                                             | 這些物件是由 Active Directory 物件處理。 如需詳細資訊，請參閱 [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)。                             |



 

 

