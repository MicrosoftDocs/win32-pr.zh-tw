---
title: AppIDFlags
description: 一組旗標，可控制 COM 伺服器的啟用行為。
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- AppIDFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966062"
---
# <a name="appidflags"></a>AppIDFlags

一組旗標，可控制 COM 伺服器的啟用行為。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 旗標值 | 常數                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ 啟用 \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND |
| 0x4        | APPIDREGFLAGS \_ \_ \_ \_ 在識別時發出啟用 RPC \_   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ 啟用 \_ IUSERVER \_ INDESKTOP 描述

如果 **AppIDFlags** 中的 **APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標已清除，或如果沒有 **AppIDFlags** ，則在終端機伺服器會話中的用戶端會對 [互動式使用者](interactive-user.md)COM 伺服器進行啟用要求，將會系結至或啟動並系結至啟用要求中會話之 "winsta0"[視窗工作站](/windows/desktop/winstation/window-stations)的「預設」桌上型電腦中的 COM 伺服器。 例如，如果用戶端執行 \\ 的是會話3的 "winsta0 desktop1"，則會話3的啟用要求會系結至或啟動並系結至會話3的 "winsta0 default" 中的 com 伺服器， \\ 即使 com 伺服器的實例已經在會話3的 "winsta0 desktop1" 中執行也是如此 \\ 。

如果 **AppIDFlags** 值中設定了 **APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標，COM 將會系結至或啟動並系結至用戶端桌面上執行的伺服器進程，以及啟用要求中的會話。 例如，如果用戶端 \\ 在會話3中執行 "winsta0 desktop1"，則會話3的啟用要求會系結至或啟動並系結至會話3中 "winsta0 desktop1" 的 com 伺服器， \\ 即使 com 伺服器的實例已經在會話3的 "winsta0 default" 中執行也是如此 \\ 。

用戶端可以使用會話的「 [標記](/windows/desktop/TermServ/session-monikers) 」來指定與用戶端會話進行啟用要求時不同的會話。

**APPIDREGFLAGS \_ ACTI加值稅E \_ IUSERVER \_ INDESKTOP** 旗標只適用于設定為 RunAs 「[互動式使用者](interactive-user.md)」的 COM 伺服器。

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND Description

如果在 **AppIDFlags** 中設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標，則會啟動設定為 RunAs 為 "Activator" 的 COM 伺服器，並提供進程安全描述項，以允許處理處理常式權杖的 LogonID SID 的 [ \_ 所有 \_ 存取](/windows/desktop/ProcThread/process-security-and-access-rights)。 此外，安全描述項的擁有者將會設定為進程權杖的 LogonID SID。

如果在 **AppIDFlags** 中設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標，則設定為 RunAs 「此使用者」的 COM 伺服器將會以進程安全描述項啟動，以允許處理常式權杖的 LogonID SID 中的 [ \_ 所有 \_ 存取](/windows/desktop/ProcThread/process-security-and-access-rights)。 此外，安全描述項的擁有者將會設定為進程權杖的 LogonID SID。 此外，COM 服務控制管理員 (SCM) 修改 COM 伺服器進程的權杖，如下所示：

-   它會將 APPID SID 新增至權杖。 它會在權杖預設任意存取控制清單 (DACL) 中，授與 APPID SID 的完整存取權。 在 Windows Vista 和更新版本的 Windows 中，它會授與 \_ 權杖預設 DACL 中的 OWNERRIGHTS SID 讀取控制許可權。 在 windows Vista 之前版本的 Windows 中，它會將權杖擁有者設定為 APPID SID。

使用 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，必須考慮下列安全性考慮：

-   **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標的設計目的，是由在其中一個內建服務安全性內容（NETWORKSERVICE 或 LocalService 帳戶）下啟動的 COM 伺服器設定。 如果伺服器模擬具有特殊許可權的用戶端，而且未設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ and \_ BIND** 旗標，則在其他具有相同安全性內容的進程中執行的惡意程式碼，可以藉由從 COM 伺服器進程劫持具特殊許可權之用戶端的模擬權杖來提高許可權。
-   設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，com 會在 RunAs "Activator" COM 伺服器的情況下強化進程物件的安全描述項。 針對這類伺服器，COM 用戶端必須強化它用於 COM 啟用的權杖。
-   設定 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標時，COM 會在 RunAs 「此使用者」 COM 伺服器的情況下強化處理常式物件的安全描述項。 它也會強化 COM 伺服器的進程 token，因為 COM SCM 是建立權杖的實體。

只有在套用 MSRC8322 patch (資訊 [安全佈告欄 MS09-012](https://support.microsoft.com/kb/959454)) 時，windows XP、windows server 2003、windows Vista 和 windows SERVER 2008 才支援 **APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND** 旗標。 Windows 7 和更新版本的 Windows 原本就支援此功能。

**APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ 和 \_ BIND** 旗標只適用于設定為 RunAs "ACTI加值稅OR" 或 "This User" 的 COM 伺服器。 它並不適用于 NT 服務的 COM 伺服器。

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ \_ \_ \_ 在 \_ 識別描述時發出啟用 RPC

如果在 **AppIDFlags** 中設定了 **APPIDREGFLAGS \_ ISSUE \_ 啟用 \_ RPC \_ AT \_ 識別** 旗標，com SCM 將會使用 [RPC \_ C \_ IMP \_ 層級 \_ 識別](impersonation-levels.md)的模擬層級，將物件啟動要求發出至 COM 伺服器進程。

如果未 **設定 \_ APPIDREGFLAGS \_ ISSUE \_ \_ 在 \_ 識別旗標上的啟用 RPC** ，則 com SCM 會將物件啟動要求發出至使用 [RPC \_ C \_ IMP \_ 層級 \_](impersonation-levels.md)模擬之模擬層級的 COM 伺服器處理常式。

在識別旗標 **上使用 APPIDREGFLAGS \_ ISSUE \_ 啟用 \_ RPC \_ \_** 時，必須考慮下列安全性考慮：

-   **APPIDREGFLAGS \_ ISSUE \_ \_ \_ 在 \_ 識別** 旗標上的啟動 RPC 是為了讓未代表用戶端在物件啟動要求中執行工作的 COM 伺服器使用。 針對這類伺服器，在 [RPC \_ C \_ IMP \_ 層級 \_](impersonation-levels.md) 使用 COM SCM 發出物件啟動要求，可讓程式中出現具有 [**SE \_ 模擬 \_ 名稱**](/windows/desktop/SecAuthZ/privilege-constants) 層級的特殊許可權權杖機率降到最低。

在 Windows 7 和更新版本的 Windows 中，支援 **在識別旗標上的 APPIDREGFLAGS \_ 問題 \_ 啟用 \_ RPC \_ \_** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[桌上型電腦](/windows/desktop/winstation/desktops)
</dt> <dt>

[模擬層級](impersonation-levels.md)
</dt> <dt>

[互動式使用者](interactive-user.md)
</dt> <dt>

[會話的名字](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[視窗工作站](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 