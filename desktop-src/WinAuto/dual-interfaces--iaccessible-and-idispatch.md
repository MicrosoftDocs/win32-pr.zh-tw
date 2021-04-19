---
title: 雙重介面 IAccessible 和 IDispatch
description: 伺服器開發人員必須提供標準元件物件模型 (COM) 介面 IDispatch 的可存取物件。
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968698"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="8bb40-103">雙重介面： IAccessible 和 IDispatch</span><span class="sxs-lookup"><span data-stu-id="8bb40-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="8bb40-104">伺服器開發人員必須提供標準元件物件模型 (COM) 介面 [**IDispatch**](idispatch-interface.md) 的可存取物件。</span><span class="sxs-lookup"><span data-stu-id="8bb40-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="8bb40-105">IDispatch 介面可讓以 Microsoft Visual Basic 撰寫的用戶端應用程式和各種指令碼語言，來使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)所公開的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="8bb40-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="8bb40-106">因為可存取的物件會透過 [IDispatch：： Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 或直接使用 **IAccessible** 來提供物件的存取權，所以稱為具有雙重介面。</span><span class="sxs-lookup"><span data-stu-id="8bb40-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="8bb40-107">當 C/c + + 用戶端取回 IDispatch 介面指標時，用戶端可以呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來嘗試將 idispatch 介面指標轉換成 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="8bb40-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="8bb40-108">若要間接呼叫 **IAccessible** 方法，C/c + + 用戶端會呼叫 IDispatch：： Invoke。</span><span class="sxs-lookup"><span data-stu-id="8bb40-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="8bb40-109">為了提升效能，請呼叫 **IAccessible** 方法直接使用物件。</span><span class="sxs-lookup"><span data-stu-id="8bb40-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="8bb40-110">如需 **IDispatch** 用來識別 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性 (Dispid) 的分派識別碼清單，請參閱 [附錄 C： IAccessible dispid](appendix-c--iaccessible-dispids.md)。</span><span class="sxs-lookup"><span data-stu-id="8bb40-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="8bb40-111">在 Microsoft Active Accessibility 2.0 版和更新版本下，伺服器不需要完全實作為 [**IDispatch**](idispatch-interface.md) 的方法，但是可以 \_ 在初始化任何 out 參數之後，直接傳回 E >notimpl，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="8bb40-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 