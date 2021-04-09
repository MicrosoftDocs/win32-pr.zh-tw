---
description: GetSignerCert 函式會進行 (列舉) 憑證存放區中的憑證，直到找到簽章金鑰的憑證為止。
ms.assetid: a3279492-a154-418d-ab25-45ec458ad483
title: GetSignerCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beff3e220fc8f0c95992c4a14a3dc8b5f5d19fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945405"
---
# <a name="getsignercert"></a>GetSignerCert

**GetSignerCert** 函式會進行 (列舉) [*憑證存放區*](../secgloss/c-gly.md)中的憑證，直到找到簽章金鑰的憑證為止。 如果找到憑證，則會傳回憑證的指標。 這段程式碼示範：

-   尋找具有憑證屬性的憑證。
-   正在檢查該屬性。
-   傳回找到屬性的憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 指標。

此程式碼會使用名為 **MyHandleError** 的錯誤處理常式。 若要查看此錯誤處理常式的執行，請參閱 [**MyHandleError**](myhandleerror.md) 主題。


```C++
#include <windows.h>

PCCERT_CONTEXT GetSignerCert(
        HCERTSTORE hCertStore)
//--------------------------------------------------------------------
//   Parameter passed in:
//      hCertStore, the handle of the store to be searched.
{
//--------------------------------------------------------------------
//   Declare and initialize local variables.

PCCERT_CONTEXT       pCertContext = NULL;
BOOL                 fMore = TRUE;
DWORD                dwSize = NULL;
CRYPT_KEY_PROV_INFO* pKeyInfo = NULL;
DWORD                PropId = CERT_KEY_PROV_INFO_PROP_ID;

//--------------------------------------------------------------------
//  Find certificates in the store until the end of the store
//  is reached or a certificate with an AT_SIGNATURE key is found.

while(fMore && 
  (pCertContext= CertFindCertificateInStore(
     hCertStore,           // Handle of the store to be searched.
     0,                    // Encoding type. Not used for this search.
     0,                    // dwFindFlags. Special find criteria.
                           // Not used in this search.
     CERT_FIND_PROPERTY,   // Find type that determines the kind of 
                           // search to do. In this case, search for 
                           // certificates that have a specific 
                           // extended property.
     &PropId,              // pvFindPara. Gives the specific 
                           // value searched for, here the identifier 
                           // of an extended property.
     pCertContext)))       // pCertContext is NULL for the 
                           // first call to the function. 
                           // If the function is called
                           // in a loop, after the first call
                           // pCertContext is the certificate
                           // returned by the previous call.
{
//-------------------------------------------------------------
// For simplicity, this code only searches 
// for the first occurrence of an AT_SIGNATURE key. 
// In many situations, a search would also look for a 
// specific subject name as well as the key type.

//-------------------------------------------------------------
// Call CertGetCertificateContextProperty once to get the
// returned structure size.

   if(!(CertGetCertificateContextProperty(
                 pCertContext,
                 CERT_KEY_PROV_INFO_PROP_ID,
                 NULL,
                 &dwSize)))
   {
      MyHandleError("Error Getting Key Property");
   }

//--------------------------------------------------------------
// Allocate memory for the returned structure.
    
   if(pKeyInfo)
        free(pKeyInfo);
   if(!(pKeyInfo = (CRYPT_KEY_PROV_INFO*)malloc(dwSize)))
   {
       MyHandleError("Error Allocating Memory for pKeyInfo");
   }
 
   //--------------------------------------------------------------
   // Get the key information structure.

   if(!(CertGetCertificateContextProperty(
       pCertContext,
       CERT_KEY_PROV_INFO_PROP_ID,
       pKeyInfo,
       &dwSize)))
   {
       MyHandleError("The second call to the function failed.");
   }
   
   //-------------------------------------------     
   // Check the dwKeySpec member for a signature key.
   if(pKeyInfo->dwKeySpec == AT_SIGNATURE)
   {
        fMore  = FALSE;
    }
}  // End of while loop

if(pKeyInfo)
   free(pKeyInfo);
return (pCertContext);
}  // End of GetSignerCert
```



 

 
