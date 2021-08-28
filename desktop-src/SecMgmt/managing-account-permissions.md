---
description: LSA 提供數個函數，應用程式可以呼叫這些函式來列舉或設定使用者、群組和本機群組帳戶的許可權。
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: 管理帳戶許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5424d43424b067bc4771bd687c287e05e195f3e807a2db64bebaed4ece049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894067"
---
# <a name="managing-account-permissions"></a>管理帳戶許可權

LSA 提供數個函數，應用程式可以呼叫這些函式來列舉或設定使用者、群組和本機群組帳戶的 [*許可權*](/windows/desktop/SecGloss/p-gly) 。

在您可以管理帳戶資訊之前，您的應用程式必須先取得本機 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)所示範。 此外，若要列舉或編輯帳戶的許可權，您必須擁有該帳戶 (SID) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) 。 您的應用程式可以找到指定帳戶名稱的 SID，如在 [名稱和 Sid 之間的轉換](translating-between-names-and-sids.md)所述。

若要存取具有特定許可權的所有帳戶，請呼叫 [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)。 此函式會在陣列中填入具有指定許可權之所有帳戶的 Sid。

取得帳戶的 SID 之後，您就可以修改其許可權。 呼叫 [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) 以將許可權新增至帳戶。 如果指定的帳號不存在， **LsaAddAccountRights** 會加以建立。 若要從帳戶移除許可權，請呼叫 [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)。 如果您移除帳戶中的擁有權限， **LsaRemoveAccountRights** 也會刪除帳戶。

您的應用程式可以藉由呼叫 [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)來檢查目前指派給帳戶的許可權。 此函數會填入 [**LSA \_ UNICODE \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構的陣列。 每個結構都包含指定帳戶所持有的許可權名稱。

下列範例會將 SeServiceLogonRight 許可權新增至帳戶。 在此範例中，AccountSID 變數會指定帳戶的 SID。 如需有關如何查閱帳戶 SID 的詳細資訊，請參閱 [在名稱和 Sid 之間轉換](translating-between-names-and-sids.md)。


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



在上述範例中，函式 InitLsaString 會將 [*unicode*](/windows/desktop/SecGloss/u-gly) 字串轉換成 [**LSA \_ unicode \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構。 這個函式的程式碼會顯示在 [使用 LSA Unicode 字串](using-lsa-unicode-strings.md)中。

 

 
