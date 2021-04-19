---
description: 下列範例顯示用來建立主要金鑰的一般 RSA/Schannel 用戶端程式代碼。
ms.assetid: 9ce4877f-e6e6-4b94-9503-092d2702b31f
title: 用來建立主要金鑰的 RSA 用戶端程式代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df39b3e09af928d60958279ea1edc98e5ae2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974045"
---
# <a name="rsa-client-code-for-creating-the-master-key"></a>用來建立主要金鑰的 RSA 用戶端程式代碼

下列範例顯示用來建立 [*主要金鑰*](../secgloss/m-gly.md)的一般 RSA/Schannel 用戶端程式代碼。


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv      = <protocol engine's key container>;
HCRYPTKEY  hPublicKey = <server's public key>;
HCRYPTKEY  hMasterKey;       // handle for master key to be created.
ALG_ID     Algid;
DWORD      dwGenFlags =CRYPT_EXPORTABLE;
DWORD          dwExportFlags =0;
BYTE       rgbBlob[<max BLOB size>];
DWORD      cbBlob;

//--------------------------------------------------------------------
// The method for creating the master key depends upon the protocol 
// in use. Schannel protocols include:
//           PCT 1.0
//           SSL 2.0
//           SSL 3.0
//           TLS 1.0     

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <PCT 1.0>:
        Algid = CALG_PCT1_MASTER;
        break;

    case <SSL 2.0>:
        Algid = CALG_SSL2_MASTER;
        dwGenFlags |=,key size. << 16;
        if(<SSL3 or TLS is supported>)
            dwExportFlags |= CRYPT_SSL2_FALLBACK;
        break;

    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Generate the master key.

CryptGenKey(
         hProv, 
         Algid, 
         dwGenFlags, 
          &hMasterKey);

//--------------------------------------------------------------------
// Export the master key.

cbBlob = sizeof(rgbBlob);
CryptExportKey(
         hMasterKey, 
         hPublicKey, 
         SIMPLEBLOB,
         dwExportFlags, 
         rgbBlob, 
         &cbBlob);
```



 

 
