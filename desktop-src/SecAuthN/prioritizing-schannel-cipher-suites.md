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
# <a name="prioritizing-schannel-cipher-suites"></a>排列 Schannel 加密套件的優先順序

[密碼編譯 API：新一代](../seccng/cng-portal.md) (CNG) 提供可查詢、新增、移除及設定提供者所支援之加密套件優先順序的函式。 使用這些函數所做的變更會立即生效，不需要重新開機使用中的伺服器。

> [!Note]
> 您也可以使用 Microsoft Management Console 中的群組原則物件嵌入式管理單元來設定 **SSL 密碼套件順序** 群組原則設定，以修改加密套件清單。
> 
> **設定 **SSL 密碼套件順序** 的群組原則設定**
> 
> 1.  在命令提示字元中，輸入 **gpedit.msc**。 **群組原則物件編輯器** 隨即出現。
> 2.  展開 [ **電腦** 設定]、[ **系統管理範本**]、[ **網路**]，然後按一下 [ **SSL 設定**]。
> 3.  在 [ **Ssl 設定**] 下，按一下 [ **Ssl 密碼套件順序** ] 設定。
> 4.  在 [ **SSL 密碼套件順序** ] 窗格中，滾動至窗格的底部。
> 5.  遵循標示 **如何修改此設定** 的指示。
> 
> 修改此設定之後必須重新開機電腦，變更才會生效。

 

密碼套件的清單限制為1023個字元。

若要設定 Schannel 密碼套件的優先順序，請參閱下列範例。

-   [列出支援的加密套件](#listing-supported-cipher-suites)
-   [新增、移除和排列加密套件的優先順序](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>列出支援的加密套件

呼叫 [**BCryptEnumCoNtextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) 函數，以依優先順序列出提供者所支援的加密套件。

下列範例示範如何使用 [**BCryptEnumCoNtextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) 函式來列出支援的加密套件。


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>新增、移除和排列加密套件的優先順序

呼叫 [**BCryptAddCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) 和 [**BCryptRemoveCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) 函式，以從支援的加密套件清單中新增和移除加密套件。

新增加密套件時，請將 [**BCryptAddCoNtextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction)函式的 *dwPosition* 參數值設定為 **CRYPT \_ PRIORITY \_ top** ，以將其新增至優先順序清單的頂端，或 **CRYPT \_ PRIORITY \_ 下優先順序** 以將其新增至清單底部。

若要設定加密套件清單的優先順序，請從清單中移除所有加密套件，然後依您想要的順序將加密套件新增至清單中。

下列範例示範如何將密碼套件新增至預設 Microsoft Schannel 提供者的優先順序清單頂端。


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



下列範例顯示如何從預設 Microsoft Schannel 提供者的優先順序清單中移除加密套件。


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



 

 
