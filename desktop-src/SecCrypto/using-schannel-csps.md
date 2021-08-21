---
description: SSL 通訊協定引擎 (Schannel) 在執行密碼編譯作業時，會使用 (CSP) 的密碼編譯服務提供者。 密碼編譯應用程式可以使用 >PROV \_ RSA \_ SCHANNEL 和 >prov DH 安全通道 \_ \_ 提供者來呼叫 CryptAcquireCoNtext。
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: 使用 Schannel Csp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0845263d16a74f2b04aa71acb97bf200bf5218ead32e359ccd89df4e8c8f4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971512"
---
# <a name="using-schannel-csps"></a>使用 Schannel Csp

SSL 通訊協定引擎 ([*Schannel*](../secgloss/s-gly.md)) 在執行密碼編譯作業時，會使用 (CSP) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。 密碼編譯應用程式[](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)可以使用 >prov \_ RSA \_ schannel 和 >prov DH 安全通道 \_ \_ 提供者來呼叫 CryptAcquireCoNtext。

本節定義 RSA 和 Diffie-Hellman Schannel [*CSP 類型*](../secgloss/c-gly.md) ，並描述 CSP 必須支援的功能，以與 Schannel.dll 的密碼編譯通訊協定引擎相容。 通訊協定引擎是一種程式，可在用戶端與伺服器應用程式之間建立安全通道。

應用程式不應該嘗試使用本檔中的資訊，直接使用 >PROV \_ RSA \_ SCHANNEL 或 >prov \_ DH \_ schannel。 相反地，本檔說明 CSP 開發人員和廠商必須撰寫與 Microsoft Schannel 提供者相容的安全通道 Csp。

本檔旨在協助 CSP 開發人員執行相容的 RSA 或 Diffie-Hellman Schannel Csp。 開發人員會假設您已熟悉 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定3.0 版、 [*公開金鑰*](../secgloss/p-gly.md) 密碼編譯、 [*數位憑證*](../secgloss/d-gly.md)和 CryptoAPI 函數集。 建議您閱讀這些主題的新開發人員，以閱讀此 SDK 中的 SSL 通訊協定3.0 規格和 [密碼編譯基本](cryptography-essentials.md) 檔。 此外，RSA 和 Diffie-Hellman CSP 開發人員必須知道 [*傳輸層安全性*](../secgloss/t-gly.md) (TLS) 通訊協定規格，以及相關的 RSA 和 [*diffie-hellman 演算法*](../secgloss/d-gly.md)。

如需 Microsoft 通訊協定引擎使用的範例，請參閱 [建立主要金鑰](creating-the-master-key.md)。 在此範例中，對密碼編譯函式的呼叫會導致呼叫由 CSP 必須實行的 CP 函式。 若要撰寫相容的 CSP，開發人員必須瞭解 SSL 3.0 規格，並將該知識與此範例中所使用的通訊協定引擎程式碼的理解進行結合。

由於使用私用通訊技術通訊協定的未來預期會很短，因此新的 Csp 開發人員不需要支援此通訊協定。 安全通道通訊協定引擎為了回溯相容性而完全支援。

 

 
