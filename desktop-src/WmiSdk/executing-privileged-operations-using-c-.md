---
description: 特殊用戶端應用程式可能會叫用具有特殊許可權的作業。
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: 使用 c + + 執行特殊許可權作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318943"
---
# <a name="executing-privileged-operations-using-c"></a>使用 c + + 執行特殊許可權作業

特殊用戶端應用程式可能會叫用具有特殊許可權的作業。 例如，應用程式可能會允許管理員將沒有回應的 office 電腦重新開機。 藉由使用 Windows Management Instrumentation (WMI) ，您可以呼叫 WMI 提供者來執行特殊許可權作業，藉此執行特殊許可權的操作。

下列程式描述如何呼叫提供者進行有許可權的作業。

**若要呼叫具有特殊許可權作業的提供者**

1.  取得用戶端進程的許可權，以執行具有特殊許可權的作業。

    通常，系統管理員會在執行處理常式之前，使用系統管理工具來設定許可權。

2.  取得提供者進程的許可權，以啟用具有特殊許可權的作業。

    一般來說，您可以使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數的呼叫來設定提供者許可權。

3.  取得用戶端進程的許可權，以啟用具有特殊許可權的作業。

    只有當提供者是用戶端的本機提供者時，才需要執行此步驟。 如果用戶端和提供者存在於同一部電腦上，用戶端就必須使用下列其中一種技術來明確啟用特殊許可權作業：

    -   如果用戶端擁有此程式，則用戶端可以使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 來調整進程權杖，然後再呼叫 WMI。 在此情況下，您不需要再撰寫任何程式碼。
    -   如果用戶端無法存取用戶端權杖，用戶端就可以使用下列程式建立執行緒權杖，並在該權杖上使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 。

下列程式描述如何建立執行緒權杖，並在該標記上使用 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 。

**若要建立執行緒權杖，並在該權杖上使用 AdjustTokenPrivileges**

1.  藉由呼叫 [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself)來建立進程權杖的複本。
2.  藉由呼叫 [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)來取出新建立的執行緒 token。
3.  使用對新權杖的 [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 呼叫來啟用特殊許可權作業。
4.  取得 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的指標。
5.  使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的呼叫，將指標遮蓋到 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 。
6.  在每次呼叫 WMI 時重複步驟1到5。

    > [!Note]  
    > 您必須重複這些步驟，因為 COM 會不正確地快取權杖。

     

本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式碼範例顯示如何在本機電腦上啟用許可權。


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
