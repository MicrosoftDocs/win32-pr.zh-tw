---
description: 密碼編譯 API：新一代 (CNG) 提供可查詢、新增、移除及設定提供者所支援之加密套件優先順序的函式。 使用這些函數所做的變更會立即生效，不需要重新開機使用中的伺服器。
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: 排列 Schannel 加密套件的優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195815"
---
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="9291a-104">排列 Schannel 加密套件的優先順序</span><span class="sxs-lookup"><span data-stu-id="9291a-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="9291a-105">[密碼編譯 API：新一代](../seccng/cng-portal.md) (CNG) 提供可查詢、新增、移除及設定提供者所支援之加密套件優先順序的函式。</span><span class="sxs-lookup"><span data-stu-id="9291a-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="9291a-106">使用這些函數所做的變更會立即生效，不需要重新開機使用中的伺服器。</span><span class="sxs-lookup"><span data-stu-id="9291a-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="9291a-107">您也可以使用 Microsoft Management Console 中的群組原則物件嵌入式管理單元來設定 **SSL 密碼套件順序** 群組原則設定，以修改加密套件清單。</span><span class="sxs-lookup"><span data-stu-id="9291a-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="9291a-108">**設定 **SSL 密碼套件順序** 的群組原則設定**</span><span class="sxs-lookup"><span data-stu-id="9291a-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="9291a-109">在命令提示字元中，輸入 **gpedit.msc**。</span><span class="sxs-lookup"><span data-stu-id="9291a-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="9291a-110">**群組原則物件編輯器** 隨即出現。</span><span class="sxs-lookup"><span data-stu-id="9291a-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="9291a-111">展開 [ **電腦** 設定]、[ **系統管理範本**]、[ **網路**]，然後按一下 [ **SSL 設定**]。</span><span class="sxs-lookup"><span data-stu-id="9291a-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="9291a-112">在 [ **Ssl 設定**] 下，按一下 [ **Ssl 密碼套件順序** ] 設定。</span><span class="sxs-lookup"><span data-stu-id="9291a-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="9291a-113">在 [ **SSL 密碼套件順序** ] 窗格中，滾動至窗格的底部。</span><span class="sxs-lookup"><span data-stu-id="9291a-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="9291a-114">遵循標示 **如何修改此設定** 的指示。</span><span class="sxs-lookup"><span data-stu-id="9291a-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="9291a-115">修改此設定之後必須重新開機電腦，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="9291a-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="9291a-116">密碼套件的清單限制為1023個字元。</span><span class="sxs-lookup"><span data-stu-id="9291a-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="9291a-117">若要設定 Schannel 密碼套件的優先順序，請參閱下列範例。</span><span class="sxs-lookup"><span data-stu-id="9291a-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="9291a-118">列出支援的加密套件</span><span class="sxs-lookup"><span data-stu-id="9291a-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="9291a-119">新增、移除和排列加密套件的優先順序</span><span class="sxs-lookup"><span data-stu-id="9291a-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="9291a-120">列出支援的加密套件</span><span class="sxs-lookup"><span data-stu-id="9291a-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="9291a-121">呼叫 [**BCryptEnumCoNtextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) 函數，以依優先順序列出提供者所支援的加密套件。</span><span class="sxs-lookup"><span data-stu-id="9291a-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="9291a-122">下列範例示範如何使用 [**BCryptEnumCoNtextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) 函式來列出支援的加密套件。</span><span class="sxs-lookup"><span data-stu-id="9291a-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="9291a-123">新增、移除和排列加密套件的優先順序</span><span class="sxs-lookup"><span data-stu-id="9291a-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="9291a-124">呼叫 [**BCryptAddCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) 和 [**BCryptRemoveCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) 函式，以從支援的加密套件清單中新增和移除加密套件。</span><span class="sxs-lookup"><span data-stu-id="9291a-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="9291a-125">新增加密套件時，請將 [**BCryptAddCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction)函式的 *dwPosition* 參數值設定為 **CRYPT \_ PRIORITY \_ top** ，以將其新增至優先順序清單的頂端，或 **CRYPT \_ PRIORITY \_ 下優先順序** 以將其新增至清單底部。</span><span class="sxs-lookup"><span data-stu-id="9291a-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="9291a-126">若要設定加密套件清單的優先順序，請從清單中移除所有加密套件，然後依您想要的順序將加密套件新增至清單中。</span><span class="sxs-lookup"><span data-stu-id="9291a-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="9291a-127">下列範例示範如何將密碼套件新增至預設 Microsoft Schannel 提供者的優先順序清單頂端。</span><span class="sxs-lookup"><span data-stu-id="9291a-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



<span data-ttu-id="9291a-128">下列範例顯示如何從預設 Microsoft Schannel 提供者的優先順序清單中移除加密套件。</span><span class="sxs-lookup"><span data-stu-id="9291a-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
