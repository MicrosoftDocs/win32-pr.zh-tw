---
description: 「本地安全機構」 (LSA) 提供在使用者、群組和本機群組名稱之間轉譯的函式，以及其對應的安全識別碼 (SID) 值。
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: 在名稱和 Sid 之間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973035"
---
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="70ab3-103">在名稱和 Sid 之間轉換</span><span class="sxs-lookup"><span data-stu-id="70ab3-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="70ab3-104">「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」 (LSA) 提供在使用者、群組和本機群組名稱之間轉譯的函式，以及其對應的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 值。</span><span class="sxs-lookup"><span data-stu-id="70ab3-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="70ab3-105">若要找出帳戶名稱，請呼叫 [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) 函數。</span><span class="sxs-lookup"><span data-stu-id="70ab3-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="70ab3-106">此函數會傳回 SID 做為 RID/網域索引組。</span><span class="sxs-lookup"><span data-stu-id="70ab3-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="70ab3-107">若要以單一元素的形式取得 SID，請呼叫 [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) 函式。</span><span class="sxs-lookup"><span data-stu-id="70ab3-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="70ab3-108">若要找出 Sid，請呼叫 [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)。</span><span class="sxs-lookup"><span data-stu-id="70ab3-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="70ab3-109">這些函式可以從本機系統信任的任何網域轉譯名稱和 SID 資訊。</span><span class="sxs-lookup"><span data-stu-id="70ab3-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="70ab3-110">您的應用程式必須先取得本機 [**原則**](policy-object.md) 物件的控制碼，才能在帳戶名稱和 sid 之間進行轉換，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)所示。</span><span class="sxs-lookup"><span data-stu-id="70ab3-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="70ab3-111">下列範例會在指定帳戶名稱的情況下查閱帳戶的 SID。</span><span class="sxs-lookup"><span data-stu-id="70ab3-111">The following example looks up the SID for an account, given the account name.</span></span>


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



<span data-ttu-id="70ab3-112">在上述範例中，函式 **InitLsaString** 會將 unicode 字串轉換成 [**LSA \_ unicode \_ 字串**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) 結構。</span><span class="sxs-lookup"><span data-stu-id="70ab3-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="70ab3-113">這個函式的程式碼會顯示在 [使用 LSA Unicode 字串](using-lsa-unicode-strings.md)中。</span><span class="sxs-lookup"><span data-stu-id="70ab3-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="70ab3-114">這些轉譯函數主要是提供給許可權編輯器使用，以顯示 (ACL) 資訊的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 。</span><span class="sxs-lookup"><span data-stu-id="70ab3-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="70ab3-115">許可權編輯器應該一律使用名稱或 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)SID 所在系統的 [**原則**](policy-object.md)物件來呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="70ab3-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="70ab3-116">這可確保在轉譯期間參考適當的受信任網域集。</span><span class="sxs-lookup"><span data-stu-id="70ab3-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="70ab3-117">Windows 存取控制也提供在 Sid 與帳戶名稱之間執行翻譯的功能： [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) 和 [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida)。</span><span class="sxs-lookup"><span data-stu-id="70ab3-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="70ab3-118">如果您的應用程式需要查閱帳戶名稱或 SID，而不使用額外的 LSA 原則功能，請使用 Windows 存取控制功能，而不是使用 LSA 原則功能。</span><span class="sxs-lookup"><span data-stu-id="70ab3-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="70ab3-119">如需這些函式的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="70ab3-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 
