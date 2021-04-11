---
description: 列出系統憑證存放區中的所有憑證，以及這些憑證的主體名稱和所有憑證內容屬性。
ms.assetid: 4b5361f5-79b1-4b05-a133-1a394da7d6ee
title: 範例 C 程式：列出存放區中的憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504fe54bea81663957274844c4896b53a25217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850540"
---
# <a name="example-c-program-listing-the-certificates-in-a-store"></a><span data-ttu-id="2b07c-103">範例 C 程式：列出存放區中的憑證</span><span class="sxs-lookup"><span data-stu-id="2b07c-103">Example C Program: Listing the Certificates in a Store</span></span>

<span data-ttu-id="2b07c-104">下列範例程式碼會列出系統 [*憑證存放區*](../secgloss/c-gly.md) 中的所有憑證，以及這些憑證的主體名稱和所有 [*憑證上下文*](../secgloss/c-gly.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b07c-104">The following example code lists all of the certificates in a system [*certificate store*](../secgloss/c-gly.md) and the name of the subject and all of the [*certificate context*](../secgloss/c-gly.md) properties of each of those certificates.</span></span> <span data-ttu-id="2b07c-105">此範例會取得使用者的憑證存放區名稱，因此可以用來列出任何系統憑證存放區的內容。</span><span class="sxs-lookup"><span data-stu-id="2b07c-105">The example gets the name of the certificate store from the user and thus can be used to list the contents of any system certificate store.</span></span> <span data-ttu-id="2b07c-106">此外，此範例示範如何使用兩個新的 UI 函式，其中一個會顯示憑證，另一個則是可讓使用者從存放區中的憑證清單中選取憑證的 UI。</span><span class="sxs-lookup"><span data-stu-id="2b07c-106">In addition, this example shows the use of two new UI functions, one that displays a certificate and the other, UI that allows the user to select a certificate from a list of the certificates in a store.</span></span>

<span data-ttu-id="2b07c-107">此範例程式碼說明下列工作和 [*CryptoAPI*](../secgloss/c-gly.md) 函數：</span><span class="sxs-lookup"><span data-stu-id="2b07c-107">This example code illustrates the following tasks and [*CryptoAPI*](../secgloss/c-gly.md) functions:</span></span>

-   <span data-ttu-id="2b07c-108">使用 [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)開啟系統存放區。</span><span class="sxs-lookup"><span data-stu-id="2b07c-108">Opening a system store using [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).</span></span>
-   <span data-ttu-id="2b07c-109">在迴圈中，使用 [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)來列舉開啟存放區中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="2b07c-109">In a loop, enumerating all of the certificates in the open store using [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span></span>
-   <span data-ttu-id="2b07c-110">使用 [**CryptUIDlgViewCoNtext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)顯示憑證。</span><span class="sxs-lookup"><span data-stu-id="2b07c-110">Displaying a certificate using [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext).</span></span>
-   <span data-ttu-id="2b07c-111">使用 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)取得憑證主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b07c-111">Getting the name of the certificate's subject using [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>
-   <span data-ttu-id="2b07c-112">在迴圈中，使用 [**CertEnumCertificateCoNtextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) 取得與憑證相關聯之所有屬性的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b07c-112">In a loop, using [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) to get the property identifiers of all of the properties associated with the certificate.</span></span>
-   <span data-ttu-id="2b07c-113">使用 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 取得每個屬性。</span><span class="sxs-lookup"><span data-stu-id="2b07c-113">Using [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) to get each of the properties.</span></span>
-   <span data-ttu-id="2b07c-114">顯示存放區中的憑證清單，並允許使用者使用 [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore)選取其中一個憑證。</span><span class="sxs-lookup"><span data-stu-id="2b07c-114">Displaying a list of certificates in a store and allowing a user to select one of them using [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore).</span></span>
-   <span data-ttu-id="2b07c-115">使用 [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)關閉憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="2b07c-115">Closing the certificate store using [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore).</span></span>

<span data-ttu-id="2b07c-116">這個範例會使用 [**MyHandleError**](myhandleerror.md)函數。</span><span class="sxs-lookup"><span data-stu-id="2b07c-116">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="2b07c-117">此範例包含此函式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2b07c-117">Code for this function is included with the sample.</span></span>

<span data-ttu-id="2b07c-118">這項功能和其他輔助函式的程式碼也會列在 [一般用途](general-purpose-functions.md)的函式底下。</span><span class="sxs-lookup"><span data-stu-id="2b07c-118">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>

<span data-ttu-id="2b07c-119">下列範例示範如何列舉和顯示存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="2b07c-119">The following example shows enumerating and displaying the certificates in a store.</span></span> <span data-ttu-id="2b07c-120">若要編譯此範例，您必須將編譯器設定為使用多位元組字元集。</span><span class="sxs-lookup"><span data-stu-id="2b07c-120">To compile this example, you must configure your compiler to use a multiple-byte character set.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <wincrypt.h>
#include <cryptuiapi.h>

#include <tchar.h>

#pragma comment (lib, "crypt32.lib")
#pragma comment (lib, "cryptui.lib")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This program lists all of the certificates in a system certificate
// store and all of the property identifier numbers of those 
// certificates. It also demonstrates the use of two
// UI functions. One, CryptUIDlgSelectCertificateFromStore, 
// displays the certificates in a store
// and allows the user to select one of them, 
// The other, CryptUIDlgViewContext,
// displays the contents of a single certificate.

//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE       hCertStore;        
PCCERT_CONTEXT   pCertContext=NULL;      
char pszNameString[256];
char pszStoreName[256];
void*            pvData;
DWORD            cbData;
DWORD            dwPropId = 0; 
            // Zero must be used on the first
            // call to the function. After that,
            // the last returned property identifier is passed.

//-------------------------------------------------------------------
//  Begin processing and Get the name of the system certificate store 
//  to be enumerated. Output here is to stderr so that the program  
//  can be run from the command line and stdout can be redirected  
//  to a file.

fprintf(stderr,"Please enter the store name:");
gets_s(pszStoreName, sizeof(pszStoreName));
fprintf(stderr,"The store name is %s.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hCertStore = CertOpenSystemStore(
     NULL,
     pszStoreName))
{
     fprintf(stderr,"The %s store has been opened. \n", 
          pszStoreName);
}
else
{
// If the store was not opened, exit to an error routine.
     MyHandleError("The store was not opened.");
}

//-------------------------------------------------------------------
// Use CertEnumCertificatesInStore to get the certificates 
// from the open store. pCertContext must be reset to
// NULL to retrieve the first certificate in the store.
 
// pCertContext = NULL;

while(pCertContext= CertEnumCertificatesInStore(
     hCertStore,
     pCertContext))
{
//-------------------------------------------------------------------
// A certificate was retrieved. Continue.
//-------------------------------------------------------------------
//  Display the certificate.

if ( CryptUIDlgViewContext(
  CERT_STORE_CERTIFICATE_CONTEXT,
  pCertContext,
  NULL,
  NULL,
  0,
  NULL))
{
//     printf("OK\n");
}
else
{
    MyHandleError("UI failed.");
}

if(CertGetNameString(
   pCertContext,
   CERT_NAME_SIMPLE_DISPLAY_TYPE,
   0,
   NULL,
   pszNameString,
   128))
{
   printf("\nCertificate for %s \n",pszNameString);
}
else
   fprintf(stderr,"CertGetName failed. \n");

//-------------------------------------------------------------------
// Loop to find all of the property identifiers for the specified  
// certificate. The loop continues until 
// CertEnumCertificateContextProperties returns zero.

while(dwPropId = CertEnumCertificateContextProperties(
       pCertContext, // The context whose properties are to be listed.
       dwPropId))    // Number of the last property found.  
                     // This must be zero to find the first 
                     // property identifier.
{
//-------------------------------------------------------------------
// When the loop is executed, a property identifier has been found.
// Print the property number.

   printf("Property # %d found->", dwPropId);

//-------------------------------------------------------------------
// Indicate the kind of property found.

   switch(dwPropId)
   {
     case CERT_FRIENDLY_NAME_PROP_ID:
     {
       printf("Display name: ");
       break;
     }
     case CERT_SIGNATURE_HASH_PROP_ID:
     {
       printf("Signature hash identifier ");
       break;
     }
     case CERT_KEY_PROV_HANDLE_PROP_ID:
     {
       printf("KEY PROVE HANDLE");
       break;
     }
     case CERT_KEY_PROV_INFO_PROP_ID:
     {
       printf("KEY PROV INFO PROP ID ");
       break;
     }
     case CERT_SHA1_HASH_PROP_ID:
     {
        printf("SHA1 HASH identifier");
        break;
     }
     case CERT_MD5_HASH_PROP_ID:
     {
        printf("md5 hash identifier ");
        break;
     }
     case CERT_KEY_CONTEXT_PROP_ID:
     {
        printf("KEY CONTEXT PROP identifier");
        break;
     }
     case CERT_KEY_SPEC_PROP_ID:
     {
        printf("KEY SPEC PROP identifier");
        break;
      }
      case CERT_ENHKEY_USAGE_PROP_ID:
      {
        printf("ENHKEY USAGE PROP identifier");
        break;
      }
      case CERT_NEXT_UPDATE_LOCATION_PROP_ID:
      {
        printf("NEXT UPDATE LOCATION PROP identifier");
        break;
      }
      case CERT_PVK_FILE_PROP_ID:
      {
         printf("PVK FILE PROP identifier ");
         break;
      }
      case CERT_DESCRIPTION_PROP_ID:
      {
        printf("DESCRIPTION PROP identifier ");
        break;
      }
      case CERT_ACCESS_STATE_PROP_ID:
      {
        printf("ACCESS STATE PROP identifier ");
        break;
      }
      case CERT_SMART_CARD_DATA_PROP_ID:
      {
         printf("SMART_CARD DATA PROP identifier ");
         break;
      }
      case CERT_EFS_PROP_ID:
      {
        printf("EFS PROP identifier ");
        break;
      }
      case CERT_FORTEZZA_DATA_PROP_ID:
      {
        printf("FORTEZZA DATA PROP identifier ");
        break;
      }
      case CERT_ARCHIVED_PROP_ID:
      {
        printf("ARCHIVED PROP identifier ");
        break;
      }
      case CERT_KEY_IDENTIFIER_PROP_ID:
      {
        printf("KEY IDENTIFIER PROP identifier ");
        break;
      }
      case CERT_AUTO_ENROLL_PROP_ID:
      {
        printf("AUTO ENROLL identifier. ");
        break;
      }
   } // End switch.

//-------------------------------------------------------------------
// Retrieve information on the property by first getting the 
// property size. 
// For more information, see CertGetCertificateContextProperty.

   if(CertGetCertificateContextProperty(
         pCertContext, 
         dwPropId , 
         NULL, 
         &cbData))
    {
    //  Continue.
    }
    else
    {  
    // If the first call to the function failed,
    // exit to an error routine.
        MyHandleError("Call #1 to GetCertContextProperty failed.");
    }
//-------------------------------------------------------------------
// The call succeeded. Use the size to allocate memory 
// for the property.
   
   if(pvData = (void*)malloc(cbData))
   {
   // Memory is allocated. Continue.
   }
   else
   {
   // If memory allocation failed, exit to an error routine.
      MyHandleError("Memory allocation failed.");
   }
   //----------------------------------------------------------------
   // Allocation succeeded. Retrieve the property data.
   
   if(CertGetCertificateContextProperty(
      pCertContext,
      dwPropId,
      pvData, 
      &cbData))
    {
    // The data has been retrieved. Continue.
    }
    else
    {
    // If an error occurred in the second call, 
    // exit to an error routine.
      MyHandleError("Call #2 failed.");
    }
    //---------------------------------------------------------------
    // Show the results.

   printf("The Property Content is %d \n", pvData);
     
   //----------------------------------------------------------------
   // Free the certificate context property memory.
    
   free(pvData);
  }  // End inner while.
} // End outer while.

//-------------------------------------------------------------------
// Select a new certificate by using the user interface.

if(!(pCertContext = CryptUIDlgSelectCertificateFromStore(
  hCertStore,
  NULL,
  NULL,
  NULL,
  CRYPTUI_SELECT_LOCATION_COLUMN,
  0,
  NULL)))
{
    MyHandleError("Select UI failed." );
}


//-------------------------------------------------------------------
// Clean up.

CertFreeCertificateContext(pCertContext);
CertCloseStore(hCertStore,0);
printf("The function completed successfully. \n");
} // End of main.


void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.
```



 

 
