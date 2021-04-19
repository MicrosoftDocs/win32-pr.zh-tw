---
description: 範例 C 程式：憑證存放區作業
ms.assetid: cf87791c-b98c-4dd7-b346-336c4b1a88ca
title: 範例 C 程式：憑證存放區作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2f20a56fd04eb79b1ebe2359e3c915d9aad60fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996861"
---
# <a name="example-c-program-certificate-store-operations"></a><span data-ttu-id="609ad-103">範例 C 程式：憑證存放區作業</span><span class="sxs-lookup"><span data-stu-id="609ad-103">Example C Program: Certificate Store Operations</span></span>

<span data-ttu-id="609ad-104">下列範例示範一些常見的 [*憑證存放區*](../secgloss/c-gly.md) 作業，以及下列工作和 [*CryptoAPI*](../secgloss/c-gly.md) 函數：</span><span class="sxs-lookup"><span data-stu-id="609ad-104">The following example demonstrates a number of common [*certificate store*](../secgloss/c-gly.md) operations as well as the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="609ad-105">使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 和 [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)來開啟和關閉記憶體和系統存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-105">Opening and closing memory and system stores using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) and [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>
-   <span data-ttu-id="609ad-106">使用 [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)複製開啟的存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-106">Duplicating an open store using [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore).</span></span>
-   <span data-ttu-id="609ad-107">在中尋找使用 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)來儲存符合某些準則的憑證。</span><span class="sxs-lookup"><span data-stu-id="609ad-107">Finding in stores certificates that meet some criteria using [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore).</span></span>
-   <span data-ttu-id="609ad-108">使用 [**CertCreateCertificateCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)從現有憑證的編碼部分建立新的憑證內容。</span><span class="sxs-lookup"><span data-stu-id="609ad-108">Creating a new certificate context from the encoded portion of an existing certificate using [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext).</span></span>
-   <span data-ttu-id="609ad-109">使用 [**CertAddCertificateCoNtextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)將已取出的憑證新增至記憶體中的存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-109">Adding a retrieved certificate to a store in memory using [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore).</span></span>
-   <span data-ttu-id="609ad-110">使用 [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)將憑證的連結新增至存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-110">Adding a link to a certificate to a store using [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore).</span></span>
-   <span data-ttu-id="609ad-111">將存放區儲存到磁片上的檔案中。</span><span class="sxs-lookup"><span data-stu-id="609ad-111">Saving the store in memory to a file on disk.</span></span>
-   <span data-ttu-id="609ad-112">開啟和關閉以檔案為基礎的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-112">Opening and closing a file-based certificate store.</span></span>

<span data-ttu-id="609ad-113">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="609ad-113">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="609ad-114">這個函式的程式碼會包含在範例中。</span><span class="sxs-lookup"><span data-stu-id="609ad-114">The code for this function is included with the sample.</span></span> <span data-ttu-id="609ad-115">這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="609ad-115">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="609ad-116">這個範例會使用在 [建立 dacl](../secbp/creating-a-dacl.md)主題中定義的 **CreateMyDACL** 函式，以確保使用正確的 dacl 建立開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="609ad-116">This example uses the **CreateMyDACL** function, defined in the [Creating a DACL](../secbp/creating-a-dacl.md) topic, to ensure the open file is created with a proper DACL.</span></span>

<span data-ttu-id="609ad-117">此範例會在記憶體中建立憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-117">This example creates a certificate store in memory.</span></span> <span data-ttu-id="609ad-118">系統存放區會開啟並重複。</span><span class="sxs-lookup"><span data-stu-id="609ad-118">A system store is opened and duplicated.</span></span> <span data-ttu-id="609ad-119">系統會從系統存放區中取出憑證。</span><span class="sxs-lookup"><span data-stu-id="609ad-119">A certificate is retrieved from the system store.</span></span> <span data-ttu-id="609ad-120">從已抓取憑證的編碼部分建立新的憑證。</span><span class="sxs-lookup"><span data-stu-id="609ad-120">A new certificate is created from the encoded portion of the certificate retrieved.</span></span> <span data-ttu-id="609ad-121">抓取的憑證會加入至記憶體存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-121">The certificate retrieved is added to the memory store.</span></span> <span data-ttu-id="609ad-122">從 My store 抓取第二個憑證，並將該憑證的連結新增至記憶體存放區。</span><span class="sxs-lookup"><span data-stu-id="609ad-122">A second certificate is retrieved from the My store and a link to that certificate is added to the memory store.</span></span> <span data-ttu-id="609ad-123">接著會從記憶體存放區取出憑證和連結，然後將記憶體儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="609ad-123">The certificate and the link are then retrieved from the memory store and the memory is saved to disk.</span></span> <span data-ttu-id="609ad-124">所有存放區和檔案都會關閉。</span><span class="sxs-lookup"><span data-stu-id="609ad-124">All of the stores and files are closed.</span></span> <span data-ttu-id="609ad-125">接下來會重新開啟檔案存放區，並針對憑證連結進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="609ad-125">Next, the file store is reopened and a search is done for the certificate link.</span></span> <span data-ttu-id="609ad-126">此計畫的成功與否取決於我的商店是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="609ad-126">The success of this program depends upon a My store being available.</span></span> <span data-ttu-id="609ad-127">該存放區必須包含具有「插入憑證主體 name1」主體的憑證， \_ \_ \_ 以及具有「插入憑證主體」主體的第二個憑證 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="609ad-127">That store must include a certificate with the subject "Insert\_cert\_subject\_name1," and a second certificate with the subject "Insert\_cert\_subject\_name2."</span></span> <span data-ttu-id="609ad-128">主體的名稱必須變更為「我的存放區」中已知的憑證主體名稱。</span><span class="sxs-lookup"><span data-stu-id="609ad-128">The names of the subjects must be changed to the names of certificate subjects known to be in the My store.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HCERTSTORE  hSystemStore;              // System store handle
HCERTSTORE  hMemoryStore;              // Memory store handle
HCERTSTORE  hDuplicateStore;           // Handle for a store to be 
                                       // created
                                       // as a duplicate of an open 
                                       // store
PCCERT_CONTEXT  pDesiredCert = NULL;   // Set to NULL for the first 
                                       // call to
                                       // CertFindCertificateInStore
PCCERT_CONTEXT  pCertContext;
HANDLE  hStoreFileHandle ;             // Output file handle
LPWSTR  pszFileName = L"TestStor.sto";  // Output file name
SECURITY_ATTRIBUTES sa;                // For DACL

//-------------------------------------------------------------------
// Open a new certificate store in memory.

if(hMemoryStore = CertOpenStore(
      CERT_STORE_PROV_MEMORY,    // Memory store
      0,                         // Encoding type
                                 // not used with a memory store
      NULL,                      // Use the default provider
      0,                         // No flags
      NULL))                     // Not needed
{
   printf("Opened a memory store. \n");
}
else
{
   MyHandleError( "Error opening a memory store.");
}
//-------------------------------------------------------------------
// Open the My system store using CertOpenStore.

if(hSystemStore = CertOpenStore(
     CERT_STORE_PROV_SYSTEM, // System store will be a 
                             // virtual store
     0,                      // Encoding type not needed 
                             // with this PROV
     NULL,                   // Accept the default HCRYPTPROV
     CERT_SYSTEM_STORE_CURRENT_USER,
                             // Set the system store location in the
                             // registry
     L"MY"))                 // Could have used other predefined 
                             // system stores
                             // including Trust, CA, or Root
{
   printf("Opened the MY system store. \n");
}
else
{
   MyHandleError( "Could not open the MY system store.");
}
//-------------------------------------------------------------------
// Create a duplicate of the My store.

if(hDuplicateStore = CertDuplicateStore(hSystemStore))
{
  printf("The MY store is duplicated.\n");
}
else
{
  printf("Duplication of the MY store failed.\n.");
}

//-------------------------------------------------------------------
// Close the duplicate store. 

if(hDuplicateStore)
    CertCloseStore(
        hDuplicateStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);


//-------------------------------------------------------------------
// Get a certificate that has the string "Insert_cert_subject_name1" 
// in its subject. 

if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,             // Use X509_ASN_ENCODING
      0,                            // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,        // Find a certificate with a
                                    // subject that matches the 
                                    // string in the next parameter
      L"Insert_cert_subject_name1", // The Unicode string to be found
                                    // in a certificate's subject
      NULL))                        // NULL for the first call to the
                                    // function 
                                    // In all subsequent
                                    // calls, it is the last pointer
                                    // returned by the function
{
  printf("The desired certificate was found. \n");
}
else
{
   MyHandleError("Could not find the desired certificate.");
}
//-------------------------------------------------------------------
// pDesiredCert is a pointer to a certificate with a subject that 
// includes the string "Insert_cert_subject_name1", the string is 
// passed as parameter #5 to the function.

//------------------------------------------------------------------ 
//  Create a new certificate from the encoded part of
//  an available certificate.

if(pCertContext = CertCreateCertificateContext(
    MY_ENCODING_TYPE  ,            // Encoding type
    pDesiredCert->pbCertEncoded,   // Encoded data from
                                   // the certificate retrieved
    pDesiredCert->cbCertEncoded))  // Length of the encoded data
{
  printf("A new certificate has been created.\n");
}
else
{
  MyHandleError("A new certificate could not be created.");
}

//-------------------------------------------------------------------
// Add the certificate from the My store to the new memory store.

if(CertAddCertificateContextToStore(
      hMemoryStore,                // Store handle
      pDesiredCert,                // Pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("Certificate added to the memory store. \n");
}
else
{
   MyHandleError("Could not add the certificate "
       "to the memory store.");
}
//-------------------------------------------------------------------
// Find a different certificate in the My store, and add to it a link
// to the memory store.

//-------------------------------------------------------------------
// Find the certificate context just added to the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // no dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the 
                                   // string in the next parameter
      L"Insert_cert_subject_name2",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function 
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The second certificate was found. \n");
}
else
{
   MyHandleError("Could not find the second certificate.");
}
//-------------------------------------------------------------------
// Add a link to the second certificate from the My store to 
// the new memory store.

if(CertAddCertificateLinkToStore(
      hMemoryStore,           // Store handle
      pDesiredCert,           // Pointer to a certificate
      CERT_STORE_ADD_USE_EXISTING,
      NULL))
{
   printf("Certificate link added to the memory store. \n");
}
else
{
   MyHandleError("Could not add the certificate link to the "
       "memory store.");
}
//--------------------------------------------------------------------
// Find the first certificate in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The desired certificate was found in the "
      "memory store. \n");
}
else
{
   printf("Certificate not in the memory store.\n");
}
//-------------------------------------------------------------------
// Find the certificate link in the memory store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the 
                                   // string in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The certificate link was found in the memory store. \n");
}
else
{
   printf("The certificate link was not in the memory store.\n");
}
//-------------------------------------------------------------------
// Create a file in which to save the new store and certificate.

// Create a DACL for the file.
sa.nLength = sizeof(SECURITY_ATTRIBUTES);
sa.bInheritHandle = FALSE;  

// Call the function to set the DACL. The DACL
// is set in the SECURITY_ATTRIBUTES 
// lpSecurityDescriptor member.
// if !CreateMyDACL(&sa), call MyHandleError("CreateMyDACL failed.");

if(hStoreFileHandle = CreateFile(
      pszFileName,        // File path
      GENERIC_WRITE,      // Access mode
      0,                  // Share mode
      &sa,                // Security 
      CREATE_ALWAYS,      // How to create the file
      FILE_ATTRIBUTE_NORMAL,
                          // File attributes
      NULL))              // Template
{
   printf("Created a new file on disk. \n");
}
else
{
   MyHandleError("Could not create a file on disk.");
}
//-------------------------------------------------------------------
// hStoreFileHandle is the output file handle.
// Save the memory store and its certificate to the output file.

if( CertSaveStore(
      hMemoryStore,        // Store handle
      0,                   // Encoding type not needed here
      CERT_STORE_SAVE_AS_STORE,
      CERT_STORE_SAVE_TO_FILE,
      hStoreFileHandle,    // This is the handle of an open disk file
      0))                  // dwFlags
                           // No flags needed here
{
   printf("Saved the memory store to disk. \n");
}
else
{
   MyHandleError("Could not save the memory store to disk.");
}
//-------------------------------------------------------------------
// Close the stores and the file. Reopen the file store, 
// and check its contents.

if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

if(hStoreFileHandle)
     CloseHandle(hStoreFileHandle);

printf("All of the stores and files are closed. \n");

//-------------------------------------------------------------------
//  Reopen the file store.

if(hMemoryStore = CertOpenStore(
       CERT_STORE_PROV_FILENAME,    // Store provider type
       MY_ENCODING_TYPE,            // If needed, use the usual
                                    // encoding types
       NULL,                        // Use the default HCRYPTPROV
       0,                           // Accept the default for all
                                    // dwFlags
       L"TestStor.sto" ))           // The name of an existing file
                                    // as a Unicode string
{
     printf("The file store has been reopened. \n");
}
else
{
    printf("The file store could not be reopened. \n");
}
//-------------------------------------------------------------------
// Find the certificate link in the reopened file store.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);

if(pDesiredCert=CertFindCertificateInStore(
      hMemoryStore,
      MY_ENCODING_TYPE,            // Use X509_ASN_ENCODING
      0,                           // No dwFlags needed 
      CERT_FIND_SUBJECT_STR,       // Find a certificate with a
                                   // subject that matches the string
                                   // in the next parameter
      L"Insert_cert_subject_name1",// The Unicode string to be found
                                   // in a certificate's subject
      NULL))                       // NULL for the first call to the
                                   // function
                                   // In all subsequent
                                   // calls, it is the last pointer
                                   // returned by the function
{
  printf("The certificate link was found in the file store. \n");
}
else
{
   printf("The certificate link was not in the file store.\n");
}
//-------------------------------------------------------------------
// Clean up memory and end.

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(hMemoryStore)
    CertCloseStore(
        hMemoryStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);
if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);
if(hStoreFileHandle)
     CloseHandle(hStoreFileHandle);
printf("All of the stores and files are closed. \n");
return;
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function, to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
