---
title: 如何在消費者介面自動化片段提供者中啟用導覽
description: 本主題包含範例程式碼，示範如何在 Microsoft 消費者介面自動化提供者中為片段中的元素啟用導覽。
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020923"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="15ea1-103">如何在消費者介面自動化片段提供者中啟用導覽</span><span class="sxs-lookup"><span data-stu-id="15ea1-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="15ea1-104">本主題包含範例程式碼，示範如何在 Microsoft 消費者介面自動化提供者中為片段中的元素啟用導覽。</span><span class="sxs-lookup"><span data-stu-id="15ea1-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="15ea1-105">下列範例程式碼會針對自訂清單控制項中的清單專案，執行 [**IRawElementProviderFragment：：流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。</span><span class="sxs-lookup"><span data-stu-id="15ea1-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="15ea1-106">父元素是自訂清單控制項，而同輩元素則是清單中的其他專案。</span><span class="sxs-lookup"><span data-stu-id="15ea1-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="15ea1-107">如果指定的方向沒有任何元素，方法會將 *pRetVal* 參數設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="15ea1-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a><span data-ttu-id="15ea1-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="15ea1-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="15ea1-109">**概念**</span><span class="sxs-lookup"><span data-stu-id="15ea1-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15ea1-110">執行 Server-Side 消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="15ea1-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="15ea1-111">消費者介面自動化提供者的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="15ea1-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




