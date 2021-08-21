---
description: " (CredSSP) 的認證安全性支援提供者通訊協定是安全性支援提供者，它是使用安全性支援提供者介面 (SSPI) 所執行。"
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: 認證安全性支援提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4059da0dcc1e6c963ab011ad03415175849191374732f3d1df395914aebe49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008736"
---
# <a name="credential-security-support-provider"></a>認證安全性支援提供者

 (CredSSP) 的認證安全性支援提供者通訊協定是安全性支援提供者，它是使用安全性支援提供者介面 ([SSPI](sspi.md)) 所執行。 CredSSP 可讓應用程式將使用者的認證從用戶端委派給目標伺服器，以進行遠端驗證。 CredSSP 提供加密的 [傳輸層安全性通訊協定](transport-layer-security-protocol.md) 通道。 用戶端會使用簡單且受保護的協商 (SPNEGO) 通訊協定（使用 [Microsoft Kerberos](microsoft-kerberos.md) 或 [microsoft NTLM](microsoft-ntlm.md)），透過加密通道進行驗證。

> [!Caution]  
> 這不是限制委派。 CredSSP 會將使用者的完整認證傳遞給沒有任何條件約束的伺服器。

 

如需 SPNEGO 的詳細資訊，請參閱 [Microsoft Negotiate](microsoft-negotiate.md)。

用戶端和伺服器經過驗證之後，用戶端就會將使用者的認證傳遞給伺服器。 認證會在 SPNEGO 和 TLS 工作階段金鑰下雙向加密。 CredSSP 支援以密碼為基礎的登入，以及根據 [*x.509*](/windows/desktop/SecGloss/x-gly) 和 PKINIT 的智慧卡登入。

> [!IMPORTANT]
> CredSSP 不支援 Wow64 用戶端。

 

如需 CredSSP 的詳細資訊，請參閱下列主題。



| 主題                                                                         | 描述                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [CredSSP 群組原則設定](credssp-group-policy-settings.md)<br/> | 您可以使用群組原則設定來控制 CredSSP 的認證委派。<br/> |



 

 

