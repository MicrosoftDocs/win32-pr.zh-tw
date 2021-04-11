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
# <a name="domain-browser"></a><span data-ttu-id="34e24-104">網域瀏覽器</span><span class="sxs-lookup"><span data-stu-id="34e24-104">Domain Browser</span></span>

<span data-ttu-id="34e24-105">使用 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) 介面，應用程式可以顯示 [網域瀏覽器] 對話方塊，並取得使用者所選取之網域的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="34e24-105">Using the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface, an application can display a domain browser dialog box and obtain the DNS name of the domain selected by the user.</span></span> <span data-ttu-id="34e24-106">應用程式也可以使用 **IDsBrowseDomainTree** 介面來取得樹系中所有域樹和網域的相關資料。</span><span class="sxs-lookup"><span data-stu-id="34e24-106">An application can also use the **IDsBrowseDomainTree** interface to obtain data about all domain trees and domains within a forest.</span></span>

<span data-ttu-id="34e24-107">使用 **CLSID \_ DsDomainTreeBrowser** 類別識別碼呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree)介面的實例，如下所示。</span><span class="sxs-lookup"><span data-stu-id="34e24-107">An instance of the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface is created by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsDomainTreeBrowser** class identifier as shown below.</span></span>

<span data-ttu-id="34e24-108">[**IDsBrowseDomainTree：： SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer)方法可用來指定要使用哪一台電腦和認證作為抓取定義域資料的基礎。</span><span class="sxs-lookup"><span data-stu-id="34e24-108">The [**IDsBrowseDomainTree::SetComputer**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer) method can be used to specify which computer and credentials are used as the basis for retrieving the domain data.</span></span> <span data-ttu-id="34e24-109">在特定 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree)實例上呼叫 **SetComputer** 時，必須先呼叫 [**IDsBrowseDomainTree：： FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) ，然後再次呼叫 **SetComputer** 。</span><span class="sxs-lookup"><span data-stu-id="34e24-109">When **SetComputer** is called on a particular [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) instance, [**IDsBrowseDomainTree::FlushCachedDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains) must be called before **SetComputer** is called again.</span></span>

<span data-ttu-id="34e24-110">[**IDsBrowseDomainTree：： BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto)方法是用來顯示 [網域瀏覽器] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34e24-110">The [**IDsBrowseDomainTree::BrowseTo**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-browseto) method is used to display the domain browser dialog box.</span></span> <span data-ttu-id="34e24-111">當使用者選取網域，並按一下 [ **確定]** 按鈕時， **IDsBrowseDomainTree：： BrowseTo** 會傳回 **S \_ ok** ，而且 *ppszTargetPath* 參數會包含所選網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="34e24-111">When the user selects a domain and clicks the **OK** button, the **IDsBrowseDomainTree::BrowseTo** returns **S\_OK** and the *ppszTargetPath* parameter contains the name of the selected domain.</span></span> <span data-ttu-id="34e24-112">當不再需要名稱字串時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放字串。</span><span class="sxs-lookup"><span data-stu-id="34e24-112">When the name string is no longer required, the caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

<span data-ttu-id="34e24-113">下列程式碼範例示範如何使用 [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) 介面顯示 [網域瀏覽器] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34e24-113">The following code example shows how to use the [**IDsBrowseDomainTree**](/windows/win32/api/dsclient/nn-dsclient-idsbrowsedomaintree) interface to display the domain browser dialog box.</span></span>


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



<span data-ttu-id="34e24-114">[**IDsBrowseDomainTree：： GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains)方法是用來取得域樹資料。</span><span class="sxs-lookup"><span data-stu-id="34e24-114">The [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method is used to obtain domain tree data.</span></span> <span data-ttu-id="34e24-115">定義域資料會在 [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) 結構中提供。</span><span class="sxs-lookup"><span data-stu-id="34e24-115">The domain data is supplied in a [**DOMAINTREE**](/windows/desktop/api/Dsclient/ns-dsclient-domain_tree) structure.</span></span> <span data-ttu-id="34e24-116">**DOMAINTREE** 結構包含結構的大小，以及樹狀結構中的網域元素數目。</span><span class="sxs-lookup"><span data-stu-id="34e24-116">The **DOMAINTREE** structure contains the size of the structure and the number of domain elements in the tree.</span></span> <span data-ttu-id="34e24-117">**DOMAINTREE** 結構也包含一或多個 [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc)結構。</span><span class="sxs-lookup"><span data-stu-id="34e24-117">The **DOMAINTREE** structure also contains one or more [**DOMAINDESC**](/windows/desktop/api/Dsclient/ns-dsclient-domaindesc) structures.</span></span> <span data-ttu-id="34e24-118">**DOMAINDESC** 包含域樹中單一專案的相關資料，包括子系和同輩資料。</span><span class="sxs-lookup"><span data-stu-id="34e24-118">The **DOMAINDESC** contains data about a single element in the domain tree, including child and sibling data.</span></span> <span data-ttu-id="34e24-119">您可以藉由存取每個後續 **DOMAINDESC** 結構的 **pdNextSibling** 成員來列舉網域的同級。</span><span class="sxs-lookup"><span data-stu-id="34e24-119">The siblings of a domain can be enumerated by accessing the **pdNextSibling** member of each subsequent **DOMAINDESC** structure.</span></span> <span data-ttu-id="34e24-120">您可以存取每個後續 **DOMAINDESC** 結構的 **pdChildList** 成員，以類似的方式抓取網域的子系。</span><span class="sxs-lookup"><span data-stu-id="34e24-120">The children of the domain can be retrieved in a similar manner by accessing the **pdChildList** member of each subsequent **DOMAINDESC** structure.</span></span>

<span data-ttu-id="34e24-121">下列程式碼範例示範如何使用 [**IDsBrowseDomainTree：： GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) 方法來取得和存取網域樹狀結構資料。</span><span class="sxs-lookup"><span data-stu-id="34e24-121">The following code example shows how to obtain and access the domain tree data using the [**IDsBrowseDomainTree::GetDomains**](/windows/win32/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains) method.</span></span>


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



 

 