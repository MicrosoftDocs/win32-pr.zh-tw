---
title: 用戶端如何取得子識別碼
description: 用戶端如何取得子識別碼
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682463"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="b58d4-103">用戶端如何取得子識別碼</span><span class="sxs-lookup"><span data-stu-id="b58d4-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="b58d4-104">用戶端開發人員可以利用下列方式取得物件的子識別碼：</span><span class="sxs-lookup"><span data-stu-id="b58d4-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="b58d4-105">呼叫 [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)。</span><span class="sxs-lookup"><span data-stu-id="b58d4-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="b58d4-106">此函數會抓取 [**VARIANT**](variant-structure.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="b58d4-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="b58d4-107">查詢物件以查看它是否支援 [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="b58d4-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="b58d4-108">如果有的話，請使用 [**IEnumVARIANT：： Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) 取得子識別碼。</span><span class="sxs-lookup"><span data-stu-id="b58d4-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="b58d4-109">藉由呼叫父物件的 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 方法來收集子識別碼。</span><span class="sxs-lookup"><span data-stu-id="b58d4-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="b58d4-110">用戶端必須負責釋放用於 [**變異**](variant-structure.md) 結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b58d4-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="b58d4-111">用戶端也必須在傳回的任何 [**IDispatch**](idispatch-interface.md)介面上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。</span><span class="sxs-lookup"><span data-stu-id="b58d4-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 