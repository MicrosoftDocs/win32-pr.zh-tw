---
description: 下列標頭檔應該包含在用戶端和伺服器 SSPI 範例中，以 SspiExample。 它會宣告處理與安全性封裝通訊的函式。
ms.assetid: 358c2cd6-674b-4d70-9657-800b0d1b2fe7
title: SSPI 用戶端和伺服器的標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba76283b2686ecde8a6e453c5c376f8589a78dccf9e740b381f89fc5ef4db21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101278"
---
# <a name="header-file-for-sspi-client-and-server"></a>SSPI 用戶端和伺服器的標頭檔

下列標頭檔應該包含在用戶端和伺服器 SSPI 範例中，以 SspiExample。 它會宣告處理與安全性封裝通訊的函式。


```C++
//  SspiExample.h
#include <sspi.h>
#include <windows.h>

BOOL SendMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
BOOL SendBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
void cleanup();

BOOL GenClientContext (
    BYTE *pIn,
    DWORD cbIn,
    BYTE *pOut,
    DWORD *pcbOut,
    BOOL *pfDone,
    CHAR *pszTarget,
    CredHandle *hCred,
    struct _SecHandle *hcText
);

BOOL GenServerContext (
   BYTE *pIn,
   DWORD cbIn,
   BYTE *pOut,
   DWORD *pcbOut,
   BOOL *pfDone,
   BOOL  fNewCredential
);

BOOL EncryptThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput,
         ULONG securityTrailer
    );

PBYTE DecryptThis(
         PBYTE achData, 
         LPDWORD pcbMessage,
         struct _SecHandle *hCtxt,
         ULONG   cbSecurityTrailer
);

BOOL 
SignThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput
);

PBYTE VerifyThis(
          PBYTE pBuffer, 
          LPDWORD pcbMessage,
          struct _SecHandle *hCtxt,
          ULONG   cbMaxSignature
);

void PrintHexDump(DWORD length, PBYTE buffer);

BOOL ConnectAuthSocket (
   SOCKET *s, 
   CredHandle *hCred, 
   struct _SecHandle *hcText
);

BOOL CloseAuthSocket (SOCKET s);

BOOL DoAuthentication (SOCKET s);

void MyHandleError(char *s);

```



 

 



