---
description: 使用任何密碼編譯 Api 的應用程式所呼叫的第一個 CryptoAPI 函式是 CryptAcquireCoNtext 函式。
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: 密碼編譯服務提供者內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ad2e77178ade8cc286dae1ff7334c89d33e46a63af227503f8e163f7d81cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768630"
---
# <a name="cryptographic-service-provider-contexts"></a>密碼編譯服務提供者內容

使用任何密碼編譯 Api 的應用程式所呼叫的第一個 [*CryptoAPI*](../secgloss/c-gly.md) 函式是 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函式。 此函數會傳回特定 CSP 的控制碼，其中包含 CSP 內特定 [*金鑰容器*](../secgloss/k-gly.md) 的規格。 這個金鑰容器可能是特別要求的金鑰容器，也就是目前登入使用者的預設金鑰容器。

[**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 也可以建立新的金鑰容器。 如需詳細資訊，請參閱 [範例 c 程式：建立金鑰容器和產生金鑰](example-c-program-creating-a-key-container-and-generating-keys.md) ，以及 [範例 c 程式：使用 CryptAcquireCoNtext](example-c-program-using-cryptacquirecontext.md)。

[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 都有名稱和類型。 例如，作業系統目前隨附的其中一個 Csp 名稱是 [Microsoft 基底密碼編譯提供者](microsoft-base-cryptographic-provider.md)。 它是 [>prov \_ RSA \_ 完整](prov-rsa-full.md) 型別提供者。 每個提供者的名稱都是唯一的;提供者類型不是。

當應用程式呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 來取得 CSP 控制碼時，它會指定提供者類型，並選擇性地指定提供者名稱。 如果同時指定了型別和名稱，函式就會載入具有相符提供者類型和提供者名稱的 CSP。 此函式會傳回 CSP 的控制碼，以提供 csp 和 csp 內 [*金鑰容器*](../secgloss/k-gly.md) 的存取權。

當應用程式呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 並指定提供者類型，但沒有提供者名稱時，函式會尋找已命名的提供者，先檢查與已登入使用者相關聯之預設名稱提供者的清單，如果失敗，則會從與電腦相關聯的預設名稱提供者清單中檢查。 判斷出提供者名稱之後， **CryptAcquireCoNtext** 函式會搜尋該提供者的 CSP、載入它，並傳回其控制碼。

當您完成使用 CSP 控制碼時，請呼叫 [**CryptReleaseCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) 函式來釋放它。

 

 
