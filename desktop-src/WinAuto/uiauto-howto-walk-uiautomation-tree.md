---
title: 如何逐步進行消費者介面自動化樹狀結構
description: 本主題包含範例程式碼，示範如何使用 IUIAutomationTreeWalker 介面逐步解說和檢查 Microsoft 消費者介面自動化樹狀結構中的元素。
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839876"
---
# <a name="how-to-walk-the-ui-automation-tree"></a>如何逐步進行消費者介面自動化樹狀結構

本主題包含範例程式碼，示範如何使用 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面逐步解說和檢查 Microsoft 消費者介面自動化樹狀結構中的元素。 本主題將討論下列主題：

-   [流覽元素的下階](#walking-through-descendants-of-an-element)
-   [逐步執行上階元素](#walking-through-ancestor-elements)
-   [相關主題](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a>流覽元素的下階

下列程式碼範例是一個遞迴函式，它會逐步解說 UI 元素的所有下階，並在階層式清單中顯示其控制項類型。


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a>逐步執行上階元素

下列程式碼範例是一個函式，它會逐步解說元素的上階以識別父元素。 當您需要識別控制項的父視窗時，這非常有用。 函數會針對最上層元素傳回 **Null** ;亦即，其父系為桌面的元素。


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> <dt>

[消費者介面自動化用戶端的使用說明主題](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




