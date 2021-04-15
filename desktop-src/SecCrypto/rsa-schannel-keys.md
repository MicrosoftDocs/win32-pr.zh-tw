---
description: 如何產生、取出和匯出 RSA/Schannel 金鑰。
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: RSA/Schannel 金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511545"
---
# <a name="rsaschannel-keys"></a>RSA/Schannel 金鑰

## <a name="generating-and-retrieving-rsaschannel-keys"></a>產生和取出 RSA/Schannel 金鑰

[*RSA*](../secgloss/r-gly.md) /您可以藉由呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)函數來產生 [*Schannel*](../secgloss/s-gly.md)金鑰。 呼叫 **CryptGenKey** 需要在 \_ *Algid* 參數中傳遞的 KEYEXCHANGE 演算法識別碼。

**產生 RSA/Schannel 公開/私密金鑰組**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函式，以取得 [Microsoft RSA/Schannel 密碼編譯提供者](microsoft-rsa-schannel-cryptographic-provider.md)的控制碼。
2.  呼叫 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) 函數來產生金鑰。 \_必須針對 *Algid* 參數傳入 KEYEXCHANGE，而且 *dwFlags* 參數的上16位必須設定為所需的金鑰大小 (512 位) 。 *HKey* 參數中會傳回 [**HCRYPTKEY**](hcryptkey.md)結構控制碼。

**取出先前產生的 RSA/Schannel 使用者金鑰的指標**

1.  呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) 函式，以取得 [Microsoft RSA/Schannel 密碼編譯提供者](microsoft-rsa-schannel-cryptographic-provider.md)的控制碼。
2.  呼叫 [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) 函數，並將 *dwKeySpec* 參數設定為 \_ KEYEXCHANGE。

## <a name="exporting-rsaschannel-keys"></a>匯出 RSA/Schannel 金鑰

您可以將 [*主要金鑰*](../secgloss/m-gly.md)匯出至簡單的金鑰 BLOB 結構。 這應該與匯出一般 [*RC4*](../secgloss/r-gly.md) 或 [*資料加密標準*](../secgloss/d-gly.md) (DES) [*大量加密金鑰*](../secgloss/b-gly.md)（如 [簡單金鑰 BLOB](https://www.bing.com/search?q=Simple+Key+BLOB)中所述）的相同方式執行。 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構的 **aiKeyAlg** 成員會設定為主要金鑰 (CALG \_ PCT1 \_ MASTER、CALG \_ SSL2 \_ master、CALG \_ SSL3 \_ master 或 CALG \_ TLS1 \_ master) 的演算法識別碼。

如果 [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) 函式正在匯出 SSL2 主要金鑰，且 \_ \_ 已設定 CRYPT SSL2 FALLBACK 旗標，則為了協助防止版本復原攻擊，請將加密區塊 [*填補*](../secgloss/p-gly.md) 的前八個位元組設定為0x03，而不是亂數據。

如果在 [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**)函式的 *dwFlags* 參數中指定了 **CRYPT \_ DESTROYKEY** 常數，則 CSP 會在匯出金鑰之後終結機碼或金鑰控制碼。 此旗標僅適用于不 [*透明的 blob*](../secgloss/o-gly.md)。

 

 
