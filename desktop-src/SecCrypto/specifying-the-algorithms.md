---
description: 建立或匯入主要金鑰之後，RSA/安全通道和 Diffie-hellman/安全通道都會告知 CSP 的大量加密金鑰類型，以及將衍生自主要金鑰的 MAC 金鑰。
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: 指定演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992414"
---
# <a name="specifying-the-algorithms"></a><span data-ttu-id="73387-103">指定演算法</span><span class="sxs-lookup"><span data-stu-id="73387-103">Specifying the Algorithms</span></span>

<span data-ttu-id="73387-104">建立或匯入 [*主要金鑰*](../secgloss/m-gly.md) 之後， [*RSA*](../secgloss/r-gly.md)/Schannel 和 [*diffie-hellman*](../secgloss/d-gly.md)/Schannel 都會告知 [*CSP*](../secgloss/c-gly.md) 類型的 [*大量加密金鑰*](../secgloss/b-gly.md) ，以及將衍生自主要金鑰的 [*MAC 金鑰*](../secgloss/m-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="73387-104">After a [*master key*](../secgloss/m-gly.md) is created or imported, both [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel inform the [*CSP*](../secgloss/c-gly.md) of the type of [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) that will be derived from the master key.</span></span> <span data-ttu-id="73387-105">下列範例會指定這些演算法。</span><span class="sxs-lookup"><span data-stu-id="73387-105">The following example specifies these algorithms.</span></span> <span data-ttu-id="73387-106">用戶端和伺服器都使用相同的程式碼。</span><span class="sxs-lookup"><span data-stu-id="73387-106">The same code is used for both client and server.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> <span data-ttu-id="73387-107">[*Schannel*](../secgloss/s-gly.md)通訊協定引擎不得指定 CSP 不支援的演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="73387-107">An [*Schannel*](../secgloss/s-gly.md) protocol engine must not specify algorithms and key sizes not supported by the CSP.</span></span> <span data-ttu-id="73387-108">如需詳細資訊，請參閱 [列舉支援的通訊協定](enumerating-supported-protocols.md)。</span><span class="sxs-lookup"><span data-stu-id="73387-108">For more information, see [Enumerating Supported Protocols](enumerating-supported-protocols.md).</span></span> <span data-ttu-id="73387-109">如果指定了不支援的演算法或金鑰大小，則 CSP 函式必須失敗，並傳回不相容的 \_ \_ 錯誤資料錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73387-109">If unsupported algorithms or key sizes are specified, the CSP function must fail and return the NTE\_BAD\_DATA error code.</span></span>

 

 

 
