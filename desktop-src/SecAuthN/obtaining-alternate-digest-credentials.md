---
description: 若要取得與目前登入會話相關聯的認證，請將 \_ 替代安全性主體的資訊填入 SEC 的 WINNT \_ AUTH 身分 \_ 識別結構中。
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: 取得替代的摘要認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194061"
---
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="cc8b1-103">取得替代的摘要認證</span><span class="sxs-lookup"><span data-stu-id="cc8b1-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="cc8b1-104">若要取得與目前登入 [*會話*](../secgloss/s-gly.md)相關聯的 [*認證*](../secgloss/c-gly.md)，請將替代 [*安全性主體*](../secgloss/s-gly.md)的資訊填入 [**SEC 的 \_ WINNT \_ AUTH 身分 \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a)結構中。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc8b1-105">使用 *pAuthData* 參數將結構傳遞至 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="cc8b1-106">下表說明 [**SEC \_ 驗證身分 \_ \_ 識別**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="cc8b1-107">member</span><span class="sxs-lookup"><span data-stu-id="cc8b1-107">Member</span></span>             | <span data-ttu-id="cc8b1-108">描述</span><span class="sxs-lookup"><span data-stu-id="cc8b1-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8b1-109">**使用者**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-109">**User**</span></span>           | <span data-ttu-id="cc8b1-110">以 Null 終止的字串，包含其認證將用來建立安全性內容的安全性主體名稱。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="cc8b1-111">**UserLength**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-111">**UserLength**</span></span>     | <span data-ttu-id="cc8b1-112">**使用者** 成員的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="cc8b1-113">省略終止的 null。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="cc8b1-114">**網域**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-114">**Domain**</span></span>         | <span data-ttu-id="cc8b1-115">以 Null 終止的字串，識別包含安全性主體帳戶的網域。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="cc8b1-116">**DomainLength**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-116">**DomainLength**</span></span>   | <span data-ttu-id="cc8b1-117">**網域** 成員的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="cc8b1-118">省略終止的 null。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="cc8b1-119">**密碼**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-119">**Password**</span></span>       | <span data-ttu-id="cc8b1-120">以 Null 終止的字串，其中包含安全性主體的密碼。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="cc8b1-121">**密碼長度**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-121">**PasswordLength**</span></span> | <span data-ttu-id="cc8b1-122">**密碼** 成員的長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="cc8b1-123">省略終止的 null。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="cc8b1-124">**旗標**</span><span class="sxs-lookup"><span data-stu-id="cc8b1-124">**Flags**</span></span>          | <span data-ttu-id="cc8b1-125">指出字串成員是否為 ANSI 或 [*Unicode*](../secgloss/u-gly.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="cc8b1-126">下表列出結構 **旗標** 成員的有效值。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="cc8b1-127">常數</span><span class="sxs-lookup"><span data-stu-id="cc8b1-127">Constant</span></span>                            | <span data-ttu-id="cc8b1-128">描述</span><span class="sxs-lookup"><span data-stu-id="cc8b1-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8b1-129">SEC 的 \_ WINNT \_ 驗證身分 \_ 識別 \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="cc8b1-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="cc8b1-130">此結構中的字串為 ANSI 格式。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="cc8b1-131">SEC 的 \_ WINNT \_ 驗證身分 \_ 識別 \_ UNICODE</span><span class="sxs-lookup"><span data-stu-id="cc8b1-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="cc8b1-132">此結構中的字串採用 [*Unicode*](../secgloss/u-gly.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="cc8b1-133">結構和常數是在使用平臺軟體發展工具組 (SDK) 所散發的 Rpcdce .h 標頭檔中宣告的。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="cc8b1-134">下列範例示範用戶端呼叫，以取得特定使用者帳戶的摘要認證。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



<span data-ttu-id="cc8b1-135">**\_ Tcslen** 函式會傳回字串長度（以字元為單位），不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="cc8b1-136">如果您的應用程式可以使用在登入時建立的認證，請參閱 [取得預設摘要認證](obtaining-default-digest-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="cc8b1-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
