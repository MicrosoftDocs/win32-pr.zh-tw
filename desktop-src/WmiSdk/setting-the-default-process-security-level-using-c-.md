---
description: 當用戶端應用程式第一次登入 Windows Management Instrumentation (WMI) 時，必須使用 CoInitializeSecurity 的呼叫來設定預設的進程安全性層級。
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: 使用 c + + 設定預設進程安全性層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514084"
---
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="56c26-103">使用 c + + 設定預設進程安全性層級</span><span class="sxs-lookup"><span data-stu-id="56c26-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="56c26-104">當用戶端應用程式第一次登入 Windows Management Instrumentation (WMI) 時，必須使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫來設定預設的進程安全性層級。</span><span class="sxs-lookup"><span data-stu-id="56c26-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="56c26-105">COM 會使用呼叫中的資訊，來判斷另一個進程存取用戶端應用程式處理常式時必須擁有多少安全性。</span><span class="sxs-lookup"><span data-stu-id="56c26-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="56c26-106">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="56c26-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="56c26-107">使用 c + + 變更預設驗證認證</span><span class="sxs-lookup"><span data-stu-id="56c26-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="56c26-108">使用 c + + 變更預設模擬層級</span><span class="sxs-lookup"><span data-stu-id="56c26-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="56c26-109">針對大部分的用戶端應用程式，下列範例中所示的引數會設定 WMI 的預設安全性。</span><span class="sxs-lookup"><span data-stu-id="56c26-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



<span data-ttu-id="56c26-110">程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="56c26-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="56c26-111">將驗證層級設定為 [ **RPC \_ C \_ 驗證 \_ 等級] \_ 預設值** ，可讓 DCOM 協商驗證層級，以符合目的電腦的安全性需求。</span><span class="sxs-lookup"><span data-stu-id="56c26-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="56c26-112">如需詳細資訊，請參閱 [使用 c + + 變更預設驗證認證](#changing-the-default-authentication-credentials-using-c) ，以及 [使用 c + + 變更預設的模擬設定](#changing-the-default-impersonation-levels-using-c)。</span><span class="sxs-lookup"><span data-stu-id="56c26-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="56c26-113">使用 c + + 變更預設驗證認證</span><span class="sxs-lookup"><span data-stu-id="56c26-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="56c26-114">預設驗證認證適用于大部分的情況，但您可能需要在不同的情況下使用不同的驗證認證。</span><span class="sxs-lookup"><span data-stu-id="56c26-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="56c26-115">例如，您可能會想要將加密新增至驗證程式。</span><span class="sxs-lookup"><span data-stu-id="56c26-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="56c26-116">下表列出並描述不同層級的驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="56c26-117">驗證層級</span><span class="sxs-lookup"><span data-stu-id="56c26-117">Authentication level</span></span>                 | <span data-ttu-id="56c26-118">Description</span><span class="sxs-lookup"><span data-stu-id="56c26-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56c26-119">RPC \_ C \_ 驗證 \_ 層級 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="56c26-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="56c26-120">預設安全性驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="56c26-121">RPC \_ C \_ 驗證 \_ 層級 \_ 無</span><span class="sxs-lookup"><span data-stu-id="56c26-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="56c26-122">不需要驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="56c26-123">RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT</span><span class="sxs-lookup"><span data-stu-id="56c26-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="56c26-124">只有當用戶端與伺服器建立關聯性時，才會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="56c26-125">RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫</span><span class="sxs-lookup"><span data-stu-id="56c26-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="56c26-126">每次伺服器接收 RPC 時的驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="56c26-127">RPC \_ C \_ 驗證 \_ 層級 \_ PKT</span><span class="sxs-lookup"><span data-stu-id="56c26-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="56c26-128">每次伺服器從用戶端接收資料時進行驗證。</span><span class="sxs-lookup"><span data-stu-id="56c26-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="56c26-129">RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="56c26-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="56c26-130">驗證未修改封包中的資料。</span><span class="sxs-lookup"><span data-stu-id="56c26-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="56c26-131">RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權</span><span class="sxs-lookup"><span data-stu-id="56c26-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="56c26-132">包含所有先前的驗證層級，並加密每個 RPC 呼叫的值。</span><span class="sxs-lookup"><span data-stu-id="56c26-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="56c26-133">您可以在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的 *pAuthList* 參數中使用 **唯一的 \_ 驗證 \_ 清單** 結構，以指定多個使用者的預設驗證認證。</span><span class="sxs-lookup"><span data-stu-id="56c26-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="56c26-134">下列程式碼範例顯示如何變更驗證認證。</span><span class="sxs-lookup"><span data-stu-id="56c26-134">The following code example shows how to change the authentication credentials.</span></span>


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="56c26-135">使用 c + + 變更預設模擬層級</span><span class="sxs-lookup"><span data-stu-id="56c26-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="56c26-136">COM 提供從系統登錄讀取的預設安全性層級。</span><span class="sxs-lookup"><span data-stu-id="56c26-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="56c26-137">不過，除非特別修改，否則登錄設定會將模擬等級設定為太低，讓 WMI 無法運作。</span><span class="sxs-lookup"><span data-stu-id="56c26-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="56c26-138">一般而言，預設模擬層級是 **rpc \_ c \_ IMP \_ 層級 \_ 識別**，但是 WMI 至少需要 **rpc \_ c \_ IMP \_ 層級 \_** 模擬才能與大部分的提供者搭配運作，而且您可能會遇到需要設定較高層級模擬的情況。</span><span class="sxs-lookup"><span data-stu-id="56c26-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="56c26-139">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="56c26-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="56c26-140">下表列出不同的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="56c26-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="56c26-141">層級</span><span class="sxs-lookup"><span data-stu-id="56c26-141">Level</span></span>                           | <span data-ttu-id="56c26-142">描述</span><span class="sxs-lookup"><span data-stu-id="56c26-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c26-143">RPC \_ C \_ IMP \_ 層級 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="56c26-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="56c26-144">作業系統會選擇模擬的層級。</span><span class="sxs-lookup"><span data-stu-id="56c26-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="56c26-145">RPC \_ C \_ IMP \_ 層級 \_ 匿名</span><span class="sxs-lookup"><span data-stu-id="56c26-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="56c26-146">伺服器可以模擬用戶端，但模擬權杖無法用於任何作業。</span><span class="sxs-lookup"><span data-stu-id="56c26-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="56c26-147">RPC \_ C \_ IMP \_ 層級 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="56c26-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="56c26-148">伺服器可以取得用戶端的身分識別，並模擬用戶端以進行 ACL 檢查。</span><span class="sxs-lookup"><span data-stu-id="56c26-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="56c26-149">RPC \_ C \_ IMP \_ 層級模擬 \_</span><span class="sxs-lookup"><span data-stu-id="56c26-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="56c26-150">伺服器可以跨一個電腦界限來模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="56c26-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="56c26-151">RPC \_ C \_ IMP \_ 層級 \_ 委派</span><span class="sxs-lookup"><span data-stu-id="56c26-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="56c26-152">伺服器可以跨多個界限模擬用戶端，並可代表用戶端進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="56c26-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
