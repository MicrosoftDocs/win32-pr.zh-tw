---
title: COM 的存取控制清單
description: COM 的存取控制清單
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50e1641691b1a2812e861a95c5bc0f7eac8f0f8af67d41b18287c07253b8d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551352"
---
# <a name="access-control-lists-for-com"></a>COM 的存取控制清單

Windowsserver XP Service pack 2 (sp 2) 和 Windows Server 2003 Service pack 1 (SP 1) 為分散式元件物件模型 (DCOM) 引進安全性增強功能。 這些增強功能的其中一項是更特定的存取權限，可在 (Acl) 的存取控制清單中使用。 存取權限為：

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

為了提供回溯相容性，ACL 可能存在於 Windows XP SP 2 和 Windows Server 2003 SP 1 之前所使用的格式。它只會使用存取權限的許可權 \_ \_ 執行，或可能存在於 Windows XP SP 2 和 Windows Server 2003 SP 1 中使用的新格式，此格式會 \_ \_ 搭配 com 許可權執行 \_ \_ \_ 本機、com \_ rights \_ execute \_ remote、com \_ rights \_ activate \_ local 和 com \_ 許可權 \_ 啟用 \_ 遠端。

> [!Note]  
> \_ \_ 必須一律存在 COM 許可權，否則不存在此許可權會產生不正確安全描述項。

 

您不得在單一 ACL 內混用舊格式和新格式; (Ace 的所有存取控制專案) 必須僅授與 COM \_ 許可權 \_ 執行存取權限，或全部都必須授與 com 許可權執行、com rights \_ \_ execute、 \_ \_ \_ com \_ rights \_ execute \_ remote、com \_ rights \_ activate \_ 本機和 com 許可權 \_ \_ 啟用 \_ 遠端的組合。

以下是格式不正確的 ACL 範例：

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

請注意，第一個存取控制專案 (ACE) 只會授與 COM \_ rights \_ execute (0x1) ，而第二個 ACE 會授 \_ 與 com 許可權執行 \_ 、com \_ 許可權 \_ 執行 \_ 本機和 com 許可權，以啟用本機 (\_ \_ \_ 0xb) ，而第三個授 \_ 與 com 許可權 \_ 執行和 com \_ 許可權會 \_ 啟用 \_ 本機 (0x9) 。

若要修正這個錯誤，應該將第一個 ACE 變更為 \_ \_ 與其他四個存取權限的其中一個結合執行 com 許可權，否則第二個和第三個 ace 應變更為僅授與 com \_ 許可權 \_ 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows XP service pack 2 和 Windows Server 2003 Service pack 1 中的 DCOM 安全性增強功能](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




