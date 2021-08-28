---
title: " (Ssp 的安全性支援提供者) "
description: 從 Windows 2000 開始，RPC 支援各種不同的安全性提供者和套件。
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e71f088a9366f76b499203997ffdf635a27c3aca7af5c7fc4314453fe1fa79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017988"
---
# <a name="security-support-providers-ssps"></a> (Ssp 的安全性支援提供者) 

從 Windows 2000 開始，RPC 支援各種不同的安全性提供者和套件。 其中包含：

-   **Kerberos 通訊協定安全性封裝。** Kerberos v5 通訊協定是業界標準的安全性套件。 它會使用 fullsic 主體名稱。
-   **SCHANNEL SSP。** 這個 SSP 會執行 Microsoft 統一通訊協定提供者安全性封裝，以統一 SSL、私用通訊技術 (PCT) ，以及將傳輸層級安全性 (TLS) 成一個安全性封裝。 它會辨識 msstd 和 fullsic 主體名稱。
-   **NTLM 安全性封裝。** 這是 Windows 2000 之前 NTLM 網路的主要安全性封裝。

此外，Microsoft RPC 提供的 *虛擬 ssp* 可讓應用程式在使用真正的 ssp 之間進行協調。 這個稱為簡單 GSS-API 協商機制 (Snego) SSP 的虛擬 SSP 不提供任何實際的驗證功能。 其唯一用途是協助應用程式選取真實的 SSP。 目前，用戶端和伺服器程式可以使用 Snego SSP，在使用 NTLM 安全性封裝和 Kerberos 通訊協定安全性封裝之間進行協調。 如需有關選取 Ssp 的詳細資訊，請參閱 [驗證-服務常數](authentication-service-constants.md)。

Microsoft 提供的所有 Ssp （SCHANNEL 除外）都是以 [**每秒的 \_ WINNT \_ AUTH \_ IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) 結構所提供的格式來辨識驗證認證。 如需詳細資訊，請參閱 [用戶端驗證認證](client-authentication-credentials.md)。 如需有關如何使用特定 Ssp 的詳細資訊，請參閱「平臺軟體發展工具組 (SDK) 的安全性檔案中的 [SSPI](/windows/desktop/SecMgmt/management-functions) 函式和 [使用 Schannel 安全性提供者](/windows/desktop/SecAuthN/secure-channel) 。

 

 