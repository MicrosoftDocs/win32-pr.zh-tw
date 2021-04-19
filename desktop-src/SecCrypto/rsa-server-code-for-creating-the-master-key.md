---
description: 下列範例顯示用來建立主要金鑰的一般 RSA/Schannel 伺服器端程式碼。
ms.assetid: 617cda1e-0619-4162-85eb-d1f5aa35fd1c
title: 用來建立主要金鑰的 RSA 伺服器程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337ef8093dc2dead96e55e481781ff902ee2485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993167"
---
# <a name="rsa-server-code-for-creating-the-master-key"></a>用來建立主要金鑰的 RSA 伺服器程式碼

下列範例顯示用來建立 [*主要金鑰*](../secgloss/m-gly.md)的一般 RSA/Schannel 伺服器端程式碼。


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv         = <server's key container>;
PBYTE      pbKeyExchange = <pointer to RSA envelope>;
DWORD      dwKeyExchange = <size of RSA envelope>;
HCRYPTKEY  hPublicKey;
HCRYPTKEY  hMasterKey;
ALG_ID     Algid;
DWORD      dwFlags =0 ;
BYTE       rgbBlob[<max BLOB size>];
DWORD      cbBlob;

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <PCT 1.0>:
        Algid = CALG_PCT1_MASTER;
        break;

    case <SSL 2.0>:
        Algid = CALG_SSL2_MASTER;
        if(<we support SSL3>)
            dwFlags = CRYPT_SSL2_FALLBACK;
        break;

    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Build a SIMPLEBLOB around the RSA envelope.
{
     BLOBHEADER *pBlobHeader = (BLOBHEADER *)rgbBlob;
     ALG_ID     *pAlgid      = (ALG_ID *)(pBlobHeader + 1);
     BYTE       *pData       = (BYTE *)(pAlgid + 1);

     pBlobHeader->bType    = SIMPLEBLOB;
     pBlobHeader->bVersion = CUR_BLOB_VERSION;
     pBlobHeader->reserved = 0;
     pBlobHeader->aiKeyAlg = Algid;

     *pAlgid = CALG_RSA_KEYX;

     ReverseMemCopy(
         pData, 
         pbKeyExchange, 
         cbKeyExchange);
}

//--------------------------------------------------------------------
// Decrypt the master key.

CryptGetUserKey(
         hProv, 
         AT_KEYEXCHANGE, 
         &hPublicKey);

CryptImportKey(
          hProv, 
          rgbBlob, 
          cbBlob, 
          hPublicKey, 
          dwFlags, 
          &hMasterKey);

CryptDestroyKey(hPublicKey);
```



 

 
