---
description: 下列範例顯示用來建立主要金鑰的一般 Diffie-hellman/Schannel 伺服器端程式碼。
ms.assetid: 1ef0a2ea-8684-425c-abfe-9f65d8df7bbd
title: 用來建立主要金鑰的 Diffie-Hellman 伺服器程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31dd93f06e4675123e3bb1a6981c0135cc229513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982416"
---
# <a name="diffie-hellman-server-code-for-creating-the-master-key"></a><span data-ttu-id="763a1-103">用來建立主要金鑰的 Diffie-Hellman 伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="763a1-103">Diffie-Hellman Server Code for Creating the Master Key</span></span>

<span data-ttu-id="763a1-104">下列範例顯示用來建立 [*主要金鑰*](../secgloss/m-gly.md)的一般 [*diffie-hellman*](../secgloss/d-gly.md)/Schannel 伺服器端程式碼。</span><span class="sxs-lookup"><span data-stu-id="763a1-104">The following example shows typical [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel server-side code for creating a [*master key*](../secgloss/m-gly.md).</span></span>


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv      = <protocol engine's key container>;
HCRYPTKEY  hServerDHKey;  // handle to the client's DH key
HCRYPTKEY  hMasterKey;    // handle for the master key to be created.
ALG_ID     Algid;
PBYTE      pbClientPub = <pointer to client public key>;
DWORD      cbServerPub = <size of client public key>;
BYTE       rgbClientBlob[<max BLOB size>];
DWORD      cbClientBlob = <size of the client key BLOB>;
CRYPT_DATA_BLOB Data;

//--------------------------------------------------------------------
// Build a PUBLICKEYBLOB around the client's public key
{
     BLOBHEADER *pBlobHeader = (BLOBHEADER *)rgbClientBlob;
     DHPUBKEY   *pDHPubKey   = (DHPUBKEY *)(pBlobHeader + 1);
     BYTE       *pData       = (BYTE *)(pDHPubKey + 1);

     pBlobHeader->bType    = PUBLICKEYBLOB;
     pBlobHeader->bVersion = CUR_BLOB_VERSION;
     pBlobHeader->reserved = 0;
     pBlobHeader->aiKeyAlg = CALG_DH_EPHEM;

     pDHPubKey->magic = 0x31484400;
     pDHPubKey->bitlen = dwClientPub * 8;

     ReverseMemCopy(pData, pbClientPub, cbClientPub);
     cbClientBlob = sizeof(BLOBHEADER) + sizeof(DHPUBKEY) + 
        cbClientPub;
}

//--------------------------------------------------------------------
// Import the client's public key and get an agreed key

CryptImportKey(
      hProv, 
      rgbClientBlob, 
      cbClientBlob, 
      hServerDHKey, 
      0, 
      &hMasterKey);

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Convert the agreed key to the appropriate master key

CryptSetKeyParam(
         hMasterKey, 
         KP_ALGID, 
         (BYTE*)&Algid, 
         0);
```



 

 
