---
description: '>PROV RSA 安全通道的 Csp \_ \_ 必須支援 CALG \_ SSL3 \_ SHAMD5 雜湊，此雜湊可與 SSL 3.0 和 TLS 1.0 用戶端驗證中使用的 Microsoft 基礎密碼編譯提供者相容。'
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: SHA/MD5 RSA 簽章類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970752"
---
# <a name="shamd5-rsa-signature-type"></a>SHA/MD5 RSA 簽章類型

>PROV RSA 安全通道的 Csp \_ \_ 必須支援 CALG \_ SSL3 \_ SHAMD5 [*雜湊，此雜湊*](../secgloss/h-gly.md) 可與 SSL 3.0 和 TLS 1.0 用戶端驗證中使用的 Microsoft 基礎密碼編譯提供者相容。 此雜湊包含 [*MD5*](../secgloss/m-gly.md) 雜湊的串連，以及使用 RSA 或 Diffie-Hellman 私密金鑰所簽署的 SHA 雜湊。 使用 [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) 或 [**CPCREATEHASH**](https://www.bing.com/search?q=**CPCreateHash**) 函數搭配 CALG \_ SSL3 \_ SHAMD5 作為 *Algid* 參數，即可建立此類型雜湊值的控制碼。 如需使用雜湊函式的範例，請見 [c 程式：建立和雜湊工作階段金鑰](example-c-program-creating-and-hashing-a-session-key.md) ，以及 [範例 c 程式：簽署雜湊和驗證雜湊簽](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md)章。

 

 
