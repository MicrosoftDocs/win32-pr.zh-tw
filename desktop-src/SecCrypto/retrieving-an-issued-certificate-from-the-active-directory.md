---
description: 企業憑證授權單位單位 (CA) 將發出的憑證發佈至 Active Directory;獨立憑證授權單位單位也可以將發出的憑證發佈至 Active Directory。
ms.assetid: 6449e116-1671-4120-a012-278ab9ae9925
title: 從 Active Directory 中取出已發行的憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969d9930d24cafee9b7bfdd6532ecdf5b830970a87cb2ae43dcbcbc1b16517cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900563"
---
# <a name="retrieving-an-issued-certificate-from-active-directory"></a>從 Active Directory 中取出已發行的憑證

企業 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 將發出的 [*憑證*](../secgloss/c-gly.md) 發佈至 Active Directory;獨立憑證授權單位單位也可以將發出的憑證發佈至 Active Directory。 下列範例示範如何取得 Active Directory 中儲存之憑證的 [*憑證內容*](../secgloss/c-gly.md) 。 取得憑證內容之後，您可以使用 CryptoAPI 函式取出憑證的內容或執行憑證作業。

下列範例會示範如何從 Active Directory 中取出憑證。


```C++
//  Copyright (C) Microsoft.  All rights reserved.
//  Retrieve a user certificate from Active Directory.
//
//  This example uses CryptoAPI calls to retrieve 
//  a certificate previously published to Active Directory
//  by Microsoft Certificate Services.
//  Ensure Crypt32.lib and Secur32.lib are part of link libraries.
#pragma comment(lib, "crypt32.lib")

#define SECURITY_WIN32 1
#define UNICODE 1

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#include <strsafe.h>
#include <security.h>

#define MAXBUFF 512

void __cdecl main()
{
    HCERTSTORE     hStore=NULL;

    PCCERT_CONTEXT pCertCtx = NULL;

    WCHAR          wszDN[MAXBUFF];
    ULONG          cchDN = MAXBUFF;
    
    WCHAR          wszQuery[MAXBUFF * 2];
    ULONG          cchQuery = MAXBUFF * 2;

    //  Determine the name of the user whose certificate is being
    //  retrieved. This value can be constructed by other means,
    //  but this example will use GetUserNameEx.
    if (!GetUserNameEx(NameFullyQualifiedDN,
                       wszDN,
                       &cchDN))
    {
        printf("Failed GetUserNameEx: %x\n",
               GetLastError());
        exit(1);
    }

    //  Build the LDAP query string.
    if (S_OK != StringCchPrintf(wszQuery,
                    cchQuery,
                    L"ldap:///%s?%s",
                    wszDN,
                    L"userCertificate"))
    {
        printf("Failed StringCchPrintf\n");
        exit(1);

    }

    //  Open the Active Directory certificate store.
    hStore = CertOpenStore(CERT_STORE_PROV_LDAP,
                           0,
                           0,
                           CERT_STORE_READONLY_FLAG,
                           wszQuery);
    if ( NULL == hStore)
    {
        printf("Failed CertOpenStore - %x\n", GetLastError());
        exit(1);
    }

    //  Retrieve a certificate context from this opened store.
    //  Here, retrieve any existing certificate stored for 
    //  the user in Active Directory.
    //  If more than one certificate exists, consult
    //  CertFindCertificateInStore documentation for search 
    //  types and calling instructions.
    pCertCtx = CertFindCertificateInStore(hStore,
                   X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                   0,
                   CERT_FIND_ANY,
                   NULL,
                   NULL);
    if (NULL == pCertCtx)
    {
        DWORD dwErr;
        dwErr = GetLastError();
        if (CRYPT_E_NOT_FOUND == dwErr)
            printf("User does not have certificate"
                   "in Active Directory\n");
        else
            printf("Failed CertFindCertificateInStore - %x\n",
                   dwErr);
    }
    else
    {
        //  Use the certificate context as needed.
        //  Here, display the serial number.
        DWORD dwLen, i;
        dwLen = pCertCtx->pCertInfo->SerialNumber.cbData;
        //  The serial number bytes are stored
        //  least significant byte first.
        printf("Serial number: ");
        for (i = dwLen-1; i != MAXDWORD; i--)
            printf("%02x",
                   *(pCertCtx->pCertInfo->SerialNumber.pbData + i));
        printf("\n");
        //  Free the certificate context.
        CertFreeCertificateContext(pCertCtx);
    }

    //  Close the certificate store.
    CertCloseStore(hStore, 0);

}
```



 

 
