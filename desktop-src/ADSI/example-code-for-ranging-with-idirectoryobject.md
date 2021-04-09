---
title: 使用 IDirectoryObject 進行範圍的範例程式碼
description: 下列程式碼範例使用範圍，以使用 IDirectoryObject 介面抓取群組的成員。
ms.assetid: 659b4c28-6534-45d2-80ee-14184433390d
ms.tgt_platform: multiple
keywords:
- 使用 IDirectoryObject ADSI 進行範圍的範例程式碼
- 範圍抓取 ADSI，範例程式碼，使用 IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145314fa9c0c44c9b4865ea711e8533a8d1fcc59
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671156"
---
# <a name="example-code-for-ranging-with-idirectoryobject"></a><span data-ttu-id="5c664-105">使用 IDirectoryObject 進行範圍的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="5c664-105">Example Code for Ranging with IDirectoryObject</span></span>

<span data-ttu-id="5c664-106">下列程式碼範例使用範圍，以使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面抓取群組的成員。</span><span class="sxs-lookup"><span data-stu-id="5c664-106">The following code example uses ranging to retrieve the members of a group using the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface.</span></span>


```C++
//***************************************************************************
//
//  EnumGroupWithIDirectoryObject()
//
//***************************************************************************

HRESULT EnumGroupWithIDirectoryObject(LPCWSTR pwszGroupDN, 
                                      LPCWSTR pwszUsername, 
                                      LPCWSTR pwszPassword)
{
    if(NULL == pwszGroupDN)
    {
        return E_POINTER;
    }
    
    HRESULT hr;
    IDirectoryObject *pdo;

    hr = ADsOpenObject( pwszGroupDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IDirectoryObject, 
                        (void**)&pdo);

    if(SUCCEEDED(hr))
    {
        PADS_ATTR_INFO pAttrInfo;
        const DWORD dwStep = 1000;
        DWORD dwLowRange;
        DWORD dwHighRange;
        DWORD dwRetrieved;
        WCHAR wszAttr[MAX_PATH];
        LPWSTR rgAttrs[1];

        rgAttrs[0] = wszAttr;

        dwLowRange = 0;
        dwHighRange = dwLowRange + (dwStep - 1);
         
        do
        {
            swprintf_s(wszAttr, L"member;range=%d-%d", dwLowRange, dwHighRange);
            hr = pdo->GetObjectAttributes(rgAttrs, 1, &pAttrInfo, &dwRetrieved);        
            if(SUCCEEDED(hr))
            {
                DWORD i;
                
                for(i = 0; i < dwRetrieved; i++)
                {
                    DWORD x;

                    for(x = 0; x < pAttrInfo[i].dwNumValues; x++)
                    {
                        wprintf(L"%s\n", pAttrInfo[i].pADsValues[x].CaseIgnoreString);
                    }
                }

                FreeADsMem(pAttrInfo);

                dwLowRange = dwHighRange + 1;
                dwHighRange = dwLowRange + (dwStep - 1);
            }

            if(0 == dwRetrieved)
            {
                break;
            }

        }while(SUCCEEDED(hr));
        
        pdo->Release();
    }

    return hr;
}
```



 

 




