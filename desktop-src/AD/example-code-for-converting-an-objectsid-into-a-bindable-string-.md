---
title: 將 objectSid 轉換成可系結字串的範例程式碼
description: 本主題包含將 objectSid 轉換為可系結字串的程式碼範例，以將屬於下層網域的成員加入至上層網域中的群組。
ms.assetid: 8308c2e1-1a6f-4bbe-84fd-03b5fe13f0ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27a6b8d58bdffba73f5b765e0fa6570cbc15bf5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839335"
---
# <a name="example-code-for-converting-an-objectsid-into-a-bindable-string"></a><span data-ttu-id="c8dac-103">將 objectSid 轉換成可系結字串的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c8dac-103">Example Code for Converting an objectSid into a Bindable String</span></span>

<span data-ttu-id="c8dac-104">本主題包含將 **objectSid** 轉換為可系結字串的程式碼範例，以將屬於下層網域的成員加入至上層網域中的群組。</span><span class="sxs-lookup"><span data-stu-id="c8dac-104">This topic contains a code example that converts an **objectSid** to a bindable string to add a member that belongs to a down-level domain to a group in an up-level domain.</span></span>

<span data-ttu-id="c8dac-105">下列 c + + 程式碼範例示範如何將 **objectSid** 轉換為可系結字串。</span><span class="sxs-lookup"><span data-stu-id="c8dac-105">The following C++ code example shows how to convert an **objectSid** into a bindable string.</span></span>


```C++

HRESULT VariantArrayToBytes(VARIANT Variant, 
                            LPBYTE *ppBytes, 
                            DWORD *pdwBytes);

/********************************************************************

    GetLDAPSidBindStringFromVariantSID()

    Converts a SID in VARIANT form, such as an objectSid value,  
    and converts it into a bindale string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must  
    be freed by the caller with FreADsMem.

*******************************************************************/

LPWSTR GetLDAPSidBindStringFromVariantSID(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(vSID.vt != VT_EMPTY) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of 
            // hex characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
              (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                                   sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/******************************************************************

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES.  
    This function allocates the buffer using AllocADsMem. The caller 
    must free this memory with FreeADsMem when it is no longer 
    required.

******************************************************************/

HRESULT VariantArrayToBytes(VARIANT Variant, 
                            LPBYTE *ppBytes,  
                            DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 




