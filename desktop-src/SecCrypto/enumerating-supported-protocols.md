---
description: 您可以呼叫 CryptGetProvParam 搭配 PP \_ ENUMALGS 或 pp ENUMALGS 範例來列出支援的通訊協定和加密套件 \_ \_ 。
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: 列舉支援的通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d7236fe20901e9feb48e844deceea47e8f5936b9685580a653f1480b3b667c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874428"
---
# <a name="enumerating-supported-protocols"></a>列舉支援的通訊協定

您可以呼叫 [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) 搭配 pp \_ ENUMALGS 或 pp ENUMALGS 範例來列出支援的通訊協定和加密套件 \_ \_ 。 PP \_ ENUMALGS \_ ex 值的運作方式類似 PP \_ ENUMALGS，但會傳回 [**>prov \_ ENUMALGS \_ EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) 結構，以保存提供者所支援之演算法的更廣泛資訊。

如需定義的通訊協定旗標及其值的詳細資訊，請參閱 [通訊協定旗標](protocol-flags.md)。

假設 **hCryptProv** 成員是使用 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)取得的開放式密碼編譯 [*內容*](../secgloss/c-gly.md)[*控制碼*](../secgloss/h-gly.md)，並將其 *dwProvType* 參數設定為 >prov \_ RSA \_ SCHANNEL，則下列範例會列出 CSP 中所有可用的演算法名稱。


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



下表列出一般國內 >PROV RSA 安全通道 CSP 所傳回的一些演算法 \_ \_ 。 請注意，此範例中的 CSP 不支援 SSL2 SHA Mac 或 SSL2 DES encryption。



| 演算法識別碼                                                                        | 最小金鑰長度 | 最大金鑰長度 | 通訊協定 | 演算法名稱 |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | MD5          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | SHA          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| CALG \_ DES                                                                                   | 56                 | 56                 | 0x0005    | 演算法          |



 

為了準備傳送 ClientHello 或傳回 serverhello 訊息， [*Schannel*](../secgloss/s-gly.md) 通訊協定引擎會列舉 CSP 所支援的演算法和金鑰大小，並在內部建立支援的加密套件清單。

 

 
