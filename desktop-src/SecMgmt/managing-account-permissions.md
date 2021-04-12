---
description: LSA 提供數個函數，應用程式可以呼叫這些函式來列舉或設定使用者、群組和本機群組帳戶的許可權。
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: 管理帳戶許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468880"
---
# <a name="managing-account-permissions"></a><span data-ttu-id="08321-103">管理帳戶許可權</span><span class="sxs-lookup"><span data-stu-id="08321-103">Managing Account Permissions</span></span>

<span data-ttu-id="08321-104">LSA 提供數個函數，應用程式可以呼叫這些函式來列舉或設定使用者、群組和本機群組帳戶的 [*許可權*](/windows/desktop/SecGloss/p-gly) 。</span><span class="sxs-lookup"><span data-stu-id="08321-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="08321-105">在您可以管理帳戶資訊之前，您的應用程式必須先取得本機 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)所示範。</span><span class="sxs-lookup"><span data-stu-id="08321-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="08321-106">此外，若要列舉或編輯帳戶的許可權，您必須擁有該帳戶 (SID) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) 。</span><span class="sxs-lookup"><span data-stu-id="08321-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="08321-107">您的應用程式可以找到指定帳戶名稱的 SID，如在 [名稱和 Sid 之間的轉換](translating-between-names-and-sids.md)所述。</span><span class="sxs-lookup"><span data-stu-id="08321-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="08321-108">若要存取具有特定許可權的所有帳戶，請呼叫 [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)。</span><span class="sxs-lookup"><span data-stu-id="08321-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="08321-109">此函式會在陣列中填入具有指定許可權之所有帳戶的 Sid。</span><span class="sxs-lookup"><span data-stu-id="08321-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="08321-110">取得帳戶的 SID 之後，您就可以修改其許可權。</span><span class="sxs-lookup"><span data-stu-id="08321-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="08321-111">呼叫 [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) 以將許可權新增至帳戶。</span><span class="sxs-lookup"><span data-stu-id="08321-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="08321-112">如果指定的帳號不存在， **LsaAddAccountRights** 會加以建立。</span><span class="sxs-lookup"><span data-stu-id="08321-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="08321-113">若要從帳戶移除許可權，請呼叫 [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)。</span><span class="sxs-lookup"><span data-stu-id="08321-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="08321-114">如果您移除帳戶中的擁有權限， **LsaRemoveAccountRights** 也會刪除帳戶。</span><span class="sxs-lookup"><span data-stu-id="08321-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="08321-115">您的應用程式可以藉由呼叫 [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)來檢查目前指派給帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="08321-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="08321-116">此函數會填入 [**LSA \_ UNICODE \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="08321-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="08321-117">每個結構都包含指定帳戶所持有的許可權名稱。</span><span class="sxs-lookup"><span data-stu-id="08321-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="08321-118">下列範例會將 SeServiceLogonRight 許可權新增至帳戶。</span><span class="sxs-lookup"><span data-stu-id="08321-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="08321-119">在此範例中，AccountSID 變數會指定帳戶的 SID。</span><span class="sxs-lookup"><span data-stu-id="08321-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="08321-120">如需有關如何查閱帳戶 SID 的詳細資訊，請參閱 [在名稱和 Sid 之間轉換](translating-between-names-and-sids.md)。</span><span class="sxs-lookup"><span data-stu-id="08321-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


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



<span data-ttu-id="08321-121">在上述範例中，函式 InitLsaString 會將 [*unicode*](/windows/desktop/SecGloss/u-gly) 字串轉換成 [**LSA \_ unicode \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構。</span><span class="sxs-lookup"><span data-stu-id="08321-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="08321-122">這個函式的程式碼會顯示在 [使用 LSA Unicode 字串](using-lsa-unicode-strings.md)中。</span><span class="sxs-lookup"><span data-stu-id="08321-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
