---
title: IDispatch 介面和協助工具
description: IDispatch 介面最初是設計來支援 Automation。
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965648"
---
# <a name="idispatch-interface-and-accessibility"></a><span data-ttu-id="90f90-103">IDispatch 介面和協助工具</span><span class="sxs-lookup"><span data-stu-id="90f90-103">IDispatch Interface and Accessibility</span></span>

<span data-ttu-id="90f90-104">[**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)介面最初是設計來支援 Automation。</span><span class="sxs-lookup"><span data-stu-id="90f90-104">The [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface was initially designed to support Automation.</span></span> <span data-ttu-id="90f90-105">它提供晚期繫結機制，以存取和取得物件之方法和屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="90f90-105">It provides a late-binding mechanism to access and retrieve information about an object's methods and properties.</span></span> <span data-ttu-id="90f90-106">之前，伺服器開發人員必須針對其可存取的物件，同時執行 **IDispatch** 和 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面;也就是說，他們必須提供 [雙重介面](dual-interfaces--iaccessible-and-idispatch.md)。</span><span class="sxs-lookup"><span data-stu-id="90f90-106">Previously, server developers had to implement both the **IDispatch** and [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfaces for their accessible objects; that is, they had to provide a [dual interface](dual-interfaces--iaccessible-and-idispatch.md).</span></span> <span data-ttu-id="90f90-107">在 Microsoft Active Accessibility 2.0 中，伺服器可以從 **IDispatch** 方法傳回 **E \_ >notimpl** ，而 Microsoft Active Accessibility 將會為其執行 **IAccessible** 介面。</span><span class="sxs-lookup"><span data-stu-id="90f90-107">With Microsoft Active Accessibility 2.0, servers can return **E\_NOTIMPL** from **IDispatch** methods and Microsoft Active Accessibility will implement the **IAccessible** interface for them.</span></span>

<span data-ttu-id="90f90-108">除了繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的方法之外，伺服器開發人員必須在公開的每個物件的類別定義中，執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="90f90-108">In addition to the methods inherited from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), server developers must implement the following methods within the class definition of each object that is exposed:</span></span>

-   <span data-ttu-id="90f90-109">[**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) 會傳回物件的類型描述數目。</span><span class="sxs-lookup"><span data-stu-id="90f90-109">[**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) returns the number of type descriptions for the object.</span></span> <span data-ttu-id="90f90-110">針對支援 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)的物件，類型資訊計數一律為1。</span><span class="sxs-lookup"><span data-stu-id="90f90-110">For objects that support [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), the type information count is always one.</span></span>
-   <span data-ttu-id="90f90-111">[**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) 會抓取物件的可程式化介面描述。</span><span class="sxs-lookup"><span data-stu-id="90f90-111">[**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) retrieves a description of the object's programmable interface.</span></span>
-   <span data-ttu-id="90f90-112">[**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) 會將方法或屬性的名稱對應到 **DISPID**，稍後用來叫用方法或屬性。</span><span class="sxs-lookup"><span data-stu-id="90f90-112">[**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) maps the name of a method or property to a **DISPID**, which is later used to invoke the method or property.</span></span>
-   <span data-ttu-id="90f90-113">[**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) 會呼叫其中一個物件的方法，或取得或設定其中一個屬性。</span><span class="sxs-lookup"><span data-stu-id="90f90-113">[**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) calls one of the object's methods, or gets or sets one of its properties.</span></span>

 

 