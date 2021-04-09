---
title: 註冊服務的 Spn
description: 下列程式碼範例會針對服務實例註冊或取消註冊一個或多個服務主體名稱 (Spn) 。
ms.assetid: 60c252c7-76d2-4683-bf90-0f3483e6e8e0
ms.tgt_platform: multiple
keywords:
- 註冊服務 AD 的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51e6e40113a76c4a85603aa88fbb2683945330
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933047"
---
# <a name="registering-the-spns-for-a-service"></a>註冊服務的 Spn

下列程式碼範例會針對服務實例註冊或取消註冊一個或多個服務主體名稱 (Spn) 。

此範例會呼叫 [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)函式，此函式會將 Active Directory Domain Services 中的 spn 儲存在 *pszServiceAcctDN* 參數所指定之 account 物件的 [**servicePrincipalName**](/windows/desktop/ADSchema/a-serviceprincipalname)屬性下。 Account 物件會對應到此服務實例的 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 呼叫中所指定的登入帳戶。 如果登入帳戶是網域使用者帳戶，則 *pszServiceAcctDN* 必須是該使用者帳戶 Active Directory 網域 server 中帳戶物件的分辨名稱。 如果服務的登入帳戶是 LocalSystem 帳戶， *pszServiceAcctDN* 必須是安裝服務之主機電腦的電腦帳戶物件的分辨名稱。


```C++
/***************************************************************************

    SpnRegister()

    Register or unregister the SPNs under the service's account.

    If the service runs in LocalSystem account, pszServiceAcctDN is the 
    distinguished name of the local computer account.

    Parameters:

    pszServiceAcctDN - Contains the distinguished name of the logon 
    account for this instance of the service.

    pspn - Contains an array of SPNs to register.

    ulSpn - Contains the number of SPNs in the array.

    Operation - Contains one of the DS_SPN_WRITE_OP values that determines 
    the type of operation to perform on the SPNs.

***************************************************************************/

DWORD SpnRegister(TCHAR *pszServiceAcctDN,
                  TCHAR **pspn,
                  unsigned long ulSpn,
                  DS_SPN_WRITE_OP Operation)
{
    DWORD dwStatus;
    HANDLE hDs;
    TCHAR szSamName[512];
    DWORD dwSize = sizeof(szSamName) / sizeof(szSamName[0]);
    PDOMAIN_CONTROLLER_INFO pDcInfo;

    // Bind to a domain controller. 
    // Get the domain for the current user.
    if(GetUserNameEx(NameSamCompatible, szSamName, &dwSize))
    {
        TCHAR *pWhack = _tcschr(szSamName, '\\');
        if(pWhack)
        {
            *pWhack = '\0';
        }
    } 
    else 
    {
        return GetLastError();
    }
     
    // Get the name of a domain controller in that domain.
    dwStatus = DsGetDcName(NULL,
        szSamName,
        NULL,
        NULL,
        DS_IS_FLAT_NAME |
            DS_RETURN_DNS_NAME |
            DS_DIRECTORY_SERVICE_REQUIRED,
        &pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Bind to the domain controller.
    dwStatus = DsBind(pDcInfo->DomainControllerName, NULL, &hDs);
     
    // Free the DOMAIN_CONTROLLER_INFO buffer.
    NetApiBufferFree(pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Write the SPNs to the service account or computer account.
    dwStatus = DsWriteAccountSpn(
            hDs,                    // Handle to the directory.
            Operation,              // Add or remove SPN from account's existing SPNs.
            pszServiceAcctDN,       // DN of service account or computer account.
            ulSpn,                  // Number of SPNs to add.
            (const TCHAR **)pspn);  // Array of SPNs.

    // Unbind the DS in any case.
    DsUnBind(&hDs);
     
    return dwStatus;
}
```



 

 