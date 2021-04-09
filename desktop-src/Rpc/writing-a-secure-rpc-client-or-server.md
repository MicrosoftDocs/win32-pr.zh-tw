---
title: 撰寫安全的 RPC 用戶端或伺服器
description: 本節提供撰寫安全的 RPC 用戶端或伺服器的最佳作法建議。
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- 遠端程序呼叫 RPC、最佳作法、撰寫安全的用戶端或伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023839"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>撰寫安全的 RPC 用戶端或伺服器

本節提供撰寫安全的 RPC 用戶端或伺服器的最佳作法建議。

本節中的資訊適用于 Windows 2000 和 Windows XP。 本節適用于所有通訊協定序列，包括 [**ncalrpc**](/windows/desktop/Midl/ncalrpc)。 開發人員傾向于將 **ncalrpc** 視為攻擊的可能目標，這在終端機伺服器上可能會有數百位使用者可存取服務，而危及或甚至關閉服務可能會導致取得額外的存取權。

本節分為下列主題：

-   [要使用的安全性提供者](which-security-provider-to-use.md)
-   [控制用戶端驗證](controlling-client-authentication.md)
-   [選擇驗證層級](choosing-an-authentication-level.md)
-   [選擇安全性 QOS 選項](choosing-security-qos-options.md)
-   [常見錯誤：假設 RpcServerRegisterAuthInfo 可防止未經授權的使用者呼叫您的伺服器](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [回撥](callbacks.md)
-   [Null 會話](null-sessions.md)
-   [使用/robust 旗標](use-the-robust-flag.md)
-   [適用于更佳介面和方法設計的 IDL 技術](idl-techniques-for-better-interface-and-method-design.md)
-   [Strict 和 Type Strict 內容控制碼](strict-and-type-strict-context-handles.md)
-   [不要信任您的對等](do-not-trust-your-peer.md)
-   [請勿使用端點安全性](do-not-use-endpoint-security.md)
-   [請小心在相同進程中執行其他 RPC 端點](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [確認伺服器是否為其宣稱的身分](verify-the-server-is-who-it-claims-to-be.md)
-   [使用主流通訊協定序列](use-mainstream-protocol-sequences.md)
-   [我的 RPC 伺服器現在有多安全？](how-secure-is-my-rpc-server-now.md)

 

 