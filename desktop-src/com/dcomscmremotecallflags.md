---
title: DCOMSCMRemoteCallFlags
description: 控制從本機 DCOM 服務控制管理員 (DCOMSCM) 至遠端 DCOMSCM 的呼叫行為。
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- DCOMSCMRemoteCallFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024148"
---
# <a name="dcomscmremotecallflags"></a>DCOMSCMRemoteCallFlags

控制從本機 DCOM 服務控制管理員 (DCOMSCM) 至遠端 DCOMSCM 的呼叫行為。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值 | 描述                                       |
|-------|---------------------------------------------------|
| 0x1   | **DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES**  |
| 0x2   | **DCOMSCM \_ 啟用不 \_ 允許不安全的 \_ \_ 呼叫** |
| 0x4   | **DCOMSCM \_ 解決 \_ 使用 \_ 所有 \_ AUTHNSERVICES**     |
| 0x8   | **DCOMSCM \_ RESOLVE 不 \_ 允許不安全的 \_ \_ 呼叫**    |
| 0x10  | **DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE**         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a>DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES 描述

當用戶端發出使用預設安全性設定的啟用要求時，本機 DCOMSCM 會在對遠端 DCOMSCM 進行啟用 RPC 呼叫時使用「協商驗證」服務。 如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的啟用 RPC 呼叫。

**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的啟用 RPC 呼叫失敗，本機 DCOMSCM 會使用 Kerberos、NTLM 或其他已設定的安全性提供者來進行啟用 RPC 呼叫。 如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會使用沒有安全性的啟用 RPC 呼叫。

藉由設定此旗標，您可以在 Windows Vista 或更高版本上執行本機 DCOMSCM，使其行為類似于 Vista 之前的系統。 除非相容性原因需要，否則不建議設定此旗標。

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a>DCOMSCM \_ 啟用不 \_ 允許不安全的 \_ \_ 呼叫描述

如果已設定 **DCOMSCM \_ 啟用不允許不安全的 \_ \_ \_ 呼叫** 旗標，則本機 DCOMSCM 不會進行不安全的啟用 RPC 呼叫。 若要讓用戶端使用非預設安全性設定來提出啟用要求，請在進行啟用要求時指定 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構。 在此情況下， **DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES** 和 DCOMSCM 啟用時，會忽略不 **\_ 安全的 \_ \_ \_ 呼叫** 旗標。

除非網路中的所有用戶端和伺服器都經過完整驗證，否則不建議設定此旗標。

## <a name="dcomscm_resolve_use_all_authnservices-description"></a>DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES Description

當用戶端拆收物件參考時，本機 DCOMSCM 會在對遠端 DCOMSCM 進行 OXID 解析 RPC 呼叫時，使用「協商驗證」服務。 如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的方式來進行 OXID 解析 RPC 呼叫。

**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的 OXID 解析 RPC 呼叫失敗，本機 DCOMSCM 會使用 Kerberos、NTLM 或其他已設定的安全性提供者來進行 OXID 解析 RPC 呼叫。 如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會使用沒有安全性的方式進行 OXID 解析 RPC 呼叫。

藉由設定此旗標，您可以在 Windows Vista 或更高版本上執行本機 DCOMSCM，使其行為類似于 Vista 之前的系統。 除非相容性原因需要，否則不建議設定此旗標。

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a>DCOMSCM \_ RESOLVE 不 \_ 允許不安全的 \_ \_ 通話描述

如果已設定 **DCOMSCM \_ RESOLVE 不允許不安全的 \_ \_ \_ 呼叫** 旗標，則本機 DCOMSCM 不會進行不安全的 OXID 解析 RPC 呼叫。 此外，本機 DCOMSCM 不會進行不安全的垃圾收集 Ping RPC 呼叫。 除非網路中的所有用戶端和伺服器都經過完整驗證，否則不建議設定此旗標。

## <a name="dcomscm_ping_use_mid_authnservice-description"></a>DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE 描述

本機 DCOMSCM 會在對遠端 DCOMSCM 進行垃圾收集 Ping RPC 呼叫時，使用「協商驗證」服務。 如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的進行垃圾收集 Ping RPC 呼叫。

**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的垃圾收集 Ping RPC 呼叫失敗，則本機 DCOMSCM 會使用 Kerberos、NTLM 和其他已設定的安全性提供者，讓垃圾收集 Ping RPC 呼叫。 如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會進行垃圾收集，而不使用安全性來 Ping RPC 呼叫。

藉由設定此旗標，您可以在 Windows Vista 或更新版本上使用本機 DCOMSCM，使其行為類似于 Vista 之前的系統。 除非相容性原因需要，否則不建議將 **DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE** 旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遠端連線的驗證](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[EnableDCOM](enabledcom.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 