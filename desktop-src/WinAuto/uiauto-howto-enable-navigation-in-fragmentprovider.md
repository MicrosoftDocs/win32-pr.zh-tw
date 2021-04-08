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
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>如何在消費者介面自動化片段提供者中啟用導覽

本主題包含範例程式碼，示範如何在 Microsoft 消費者介面自動化提供者中為片段中的元素啟用導覽。

下列範例程式碼會針對自訂清單控制項中的清單專案，執行 [**IRawElementProviderFragment：：流覽**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) 方法。 父元素是自訂清單控制項，而同輩元素則是清單中的其他專案。 如果指定的方向沒有任何元素，方法會將 *pRetVal* 參數設定為 **Null** 。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 Server-Side 消費者介面自動化提供者](uiauto-serversideprovider.md)
</dt> <dt>

[消費者介面自動化提供者的使用說明主題](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




