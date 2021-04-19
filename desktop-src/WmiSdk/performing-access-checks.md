---
description: 存取檢查會判斷安全描述項是否授與存取權杖所識別之用戶端或執行緒的指定存取權限集。
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: 執行存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984617"
---
# <a name="performing-access-checks"></a><span data-ttu-id="7099e-103">執行存取檢查</span><span class="sxs-lookup"><span data-stu-id="7099e-103">Performing Access Checks</span></span>

<span data-ttu-id="7099e-104">存取檢查會判斷安全描述項是否授與存取權杖所識別之用戶端或執行緒的指定存取權限集。</span><span class="sxs-lookup"><span data-stu-id="7099e-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="7099e-105">您可以從 WMI 用戶端應用程式或以 c + + 或 c # 撰寫的提供者呼叫安全性函式 [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) 。</span><span class="sxs-lookup"><span data-stu-id="7099e-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="7099e-106">腳本和 Visual Basic 應用程式無法使用此處所述的方法來執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="7099e-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="7099e-107">用戶端應用程式應該在將結果傳回給用戶端非同步呼叫所提供的接收時，進行存取檢查，以判斷回呼的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7099e-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="7099e-108">當提供者無法模擬正在要求資料的用戶端應用程式或腳本時，他們應該在下列情況下執行存取檢查：</span><span class="sxs-lookup"><span data-stu-id="7099e-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="7099e-109">存取不受存取控制清單保護的資源時 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="7099e-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="7099e-110">當用戶端已連線到 **RPC \_ C \_ 層級 \_** 時，識別模擬層級。</span><span class="sxs-lookup"><span data-stu-id="7099e-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="7099e-111">C + + 和 c # 應用程式可以控制是否以個別進程執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="7099e-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="7099e-112">腳本和 Visual Basic 應用程式可以讀取或變更登錄機碼，以確保 WMI 執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="7099e-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="7099e-113">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="7099e-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="7099e-114">本主題中的程式碼範例需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="7099e-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



<span data-ttu-id="7099e-115">下列程式碼範例示範如何檢查用戶端應用程式執行緒的安全性權杖是否包含適當的許可權給指定的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7099e-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="7099e-116">此函式會使用字串 "domain \\ user" 並傳回 SID。</span><span class="sxs-lookup"><span data-stu-id="7099e-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="7099e-117">如果呼叫失敗，函數會傳回 **Null**，否則呼叫端必須釋放傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="7099e-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="7099e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="7099e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7099e-119">選擇正確的註冊</span><span class="sxs-lookup"><span data-stu-id="7099e-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="7099e-120">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="7099e-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="7099e-121">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="7099e-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="7099e-122">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="7099e-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
