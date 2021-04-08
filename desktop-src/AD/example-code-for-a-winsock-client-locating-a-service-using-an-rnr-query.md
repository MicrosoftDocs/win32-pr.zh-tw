---
title: 使用 RnR 查詢找出服務的範例程式碼
description: 下列程式碼範例會找出範例 Winsock 服務並連接至該服務。
ms.assetid: c05c7f69-d510-4feb-b426-1ae3a3ed5e16
ms.tgt_platform: multiple
keywords:
- 使用 RnR 查詢 AD 尋找服務的範例程式碼
- Windows 通訊端註冊和解析 AD，範例程式碼，使用 RnR 查詢來尋找服務
- 使用 RnR 查詢 AD 尋找服務，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee1202c981de8b4f1e0bd4f4299b1aabf1be520d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671324"
---
# <a name="example-code-for-locating-a-service-using-an-rnr-query"></a><span data-ttu-id="9f7f2-106">使用 RnR 查詢找出服務的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="9f7f2-106">Example Code for Locating a Service Using an RnR Query</span></span>

<span data-ttu-id="9f7f2-107">下列程式碼範例會找出範例 Winsock 服務並連接至該服務。</span><span class="sxs-lookup"><span data-stu-id="9f7f2-107">The following code example locates the example Winsock service and connects to it.</span></span>


```C++
#include "stdafx.h"
#include "shlobj.h"
#include "dsclient.h"


//  The PrintDomain() function displays the domain name.
void PrintDomain(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel)
{
    DWORD i;
    
    // Display the domain name.
    for(i = 0; i < dwIndentLevel; i++)
    {
        wprintf(L"  ");
    }
    wprintf(pDomainDesc->pszName);
    wprintf(L"\n");
}

//  The WalkDomainTree() function prints the current domain name and walks the tree.
void WalkDomainTree(DOMAINDESC *pDomainDesc, DWORD dwIndentLevel = 0)
{
    DOMAINDESC  *pCurrent;

    // Walk through the current item and any siblings it may have.
    for(pCurrent = pDomainDesc; 
        NULL != pCurrent; 
        pCurrent = pCurrent->pdNextSibling)
    {
        // Print the current domain name.
        PrintDomain(pCurrent, dwIndentLevel);
        
        // Walk the child tree, if one exists.
        if(NULL != pCurrent->pdChildList)
        {
            WalkDomainTree(pCurrent->pdChildList, 
                dwIndentLevel + 1);
        }
    }
}

//  Entry point for the application.
int main(void)
{
    HRESULT hr;
    IDsBrowseDomainTree *pBrowseTree;
    CoInitialize(NULL);

    hr = CoCreateInstance(CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pBrowseTree);

    if(SUCCEEDED(hr))
    {
        DOMAINTREE  *pDomTreeStruct;

        hr = pBrowseTree->GetDomains(&pDomTreeStruct, 
                                     DBDTF_RETURNFQDN);
        if(SUCCEEDED(hr))
        {
            WalkDomainTree(&pDomTreeStruct->aDomains[0]);
            hr = pBrowseTree->FreeDomains(&pDomTreeStruct);
        }
        
        pBrowseTree->Release();
    }
    
    CoUninitialize();
}
```



 

 




