---
title: 網域瀏覽器
description: 使用 IDsBrowseDomainTree 介面，應用程式可以顯示 [網域瀏覽器] 對話方塊，並取得使用者所選取之網域的 DNS 名稱。
ms.assetid: 26793c61-469e-4e99-9056-b9fc04336b69
ms.tgt_platform: multiple
keywords:
- 網域瀏覽器廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16bb932f14544902ab24e8fc1f50daa327bb705
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023249"
---
# <a name="domain-browser"></a>網域瀏覽器

使用 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) 介面，應用程式可以顯示 [網域瀏覽器] 對話方塊，並取得使用者所選取之網域的 DNS 名稱。 應用程式也可以使用 **IDsBrowseDomainTree** 介面來取得樹系中所有域樹和網域的相關資料。

使用 **CLSID \_ DsDomainTreeBrowser** 類別識別碼呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree)介面的實例，如下所示。

[**IDsBrowseDomainTree：： SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer)方法可用來指定要使用哪一台電腦和認證作為抓取定義域資料的基礎。 在特定 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree)實例上呼叫 **SetComputer** 時，必須先呼叫 [**IDsBrowseDomainTree：： FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) ，然後再次呼叫 **SetComputer** 。

[**IDsBrowseDomainTree：： BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto)方法是用來顯示 [網域瀏覽器] 對話方塊。 當使用者選取網域，並按一下 [ **確定]** 按鈕時， **IDsBrowseDomainTree：： BrowseTo** 會傳回 **S \_ ok** ，而且 *ppszTargetPath* 參數會包含所選網域的名稱。 當不再需要名稱字串時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。

下列程式碼範例示範如何使用 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) 介面顯示 [網域瀏覽器] 對話方塊。


```C++
#include <shlobj.h>
#include <dsclient.h>

void main(void)
{
    HRESULT     hr;

    hr = CoInitialize(NULL);
    if(FAILED(hr)) 
    {
        return;
    }

    IDsBrowseDomainTree *pDsDomains = NULL;

    hr = ::CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IDsBrowseDomainTree,
                                (void **)(&pDsDomains));
    
    if(SUCCEEDED(hr))
    {
        LPOLESTR    pstr;        

        hr = pDsDomains->BrowseTo(  GetDesktopWindow(),
                                    &pstr,
                                    0);
        
        if(S_OK == hr)
        {
            wprintf(pstr);
            wprintf(L"\n");
            CoTaskMemFree(pstr);
        }

        pDsDomains->Release();
    }

    CoUninitialize();
}
```



[**IDsBrowseDomainTree：： GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains)方法是用來取得域樹資料。 定義域資料會在 [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) 結構中提供。 **DOMAINTREE** 結構包含結構的大小，以及樹狀結構中的網域元素數目。 **DOMAINTREE** 結構也包含一或多個 [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc)結構。 **DOMAINDESC** 包含域樹中單一專案的相關資料，包括子系和同輩資料。 您可以藉由存取每個後續 **DOMAINDESC** 結構的 **pdNextSibling** 成員來列舉網域的同級。 您可以存取每個後續 **DOMAINDESC** 結構的 **pdChildList** 成員，以類似的方式抓取網域的子系。

下列程式碼範例示範如何使用 [**IDsBrowseDomainTree：： GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) 方法來取得和存取網域樹狀結構資料。


```C++
//  Add dsuiext.lib to the project.

#include "stdafx.h"
#include <shlobj.h>
#include <dsclient.h>

//The PrintDomain() function displays the domain name
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

//The WalkDomainTree() function traverses the domain tree and prints the current domain name
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

//  Entry point for application
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



 

 