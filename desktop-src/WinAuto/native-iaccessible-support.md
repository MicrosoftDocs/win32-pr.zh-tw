---
title: 原生 IAccessible 支援
description: Oleacc.dll 代表 OBJID \_ CLIENT \ 160 執行 IAccIdentity，IAccessible 介面指標和其直屬簡單元素子系。
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840312"
---
# <a name="native-iaccessible-support"></a><span data-ttu-id="43398-103">原生 IAccessible 支援</span><span class="sxs-lookup"><span data-stu-id="43398-103">Native IAccessible Support</span></span>

<span data-ttu-id="43398-104">Oleacc.dll 代表 [**OBJID \_ 用戶端**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標及其立即的簡單元素子系來執行 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) 。</span><span class="sxs-lookup"><span data-stu-id="43398-104">Oleacc.dll implements [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) on behalf of [**OBJID\_CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers and their immediate simple element children.</span></span> <span data-ttu-id="43398-105">當包含 *lParam*  \*\*\*\* OBJID 用戶端的 [**WM \_ GETOBJECT**](wm-getobject.md)傳送至 HWND （代表視窗的工作區或整個控制項）時，就會傳回 **OBJID \_ 用戶端** IAccessible 介面指標  =  **\_** 。 </span><span class="sxs-lookup"><span data-stu-id="43398-105">An **OBJID\_CLIENT** **IAccessible** interface pointer is returned when [**WM\_GETOBJECT**](wm-getobject.md) with *lParam* = **OBJID\_CLIENT** is sent to an **HWND**, which represents the client area of the window or the control as a whole.</span></span> <span data-ttu-id="43398-106">這類 **IAccessible** 介面指標的父系通常會有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的角色，而且是將包含 *lParam* OBJID 視窗的 **WM \_ GETOBJECT**  =  [**\_**](object-identifiers.md)傳送至 hwnd 時所傳回的 IAccessible 物件。</span><span class="sxs-lookup"><span data-stu-id="43398-106">The parent of such an **IAccessible** interface pointer will typically have a role of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and is the **IAccessible** object returned when **WM\_GETOBJECT** with *lParam* = [**OBJID\_WINDOW**](object-identifiers.md) is sent to an hwnd.</span></span>

<span data-ttu-id="43398-107">這些 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標通常會發生在 Oleacc.dll proxy 子類別化，或簡單自訂控制項 (例如容器 **IAccessible** 加上一層簡單元素子系) 提供原生 IAccessible 實作為原生 。</span><span class="sxs-lookup"><span data-stu-id="43398-107">These [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers typically occur where an Oleacc.dll proxy is subclassed, or where a simple custom control (such as a container **IAccessible** plus one level of simple element children) provides a native **IAccessible** implementation.</span></span>

<span data-ttu-id="43398-108">更複雜的原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行，例如 **IAccessible** 的階層存在或使用自訂物件識別碼時，必須自行執行 [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) 。</span><span class="sxs-lookup"><span data-stu-id="43398-108">More complicated native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementations such as where a hierarchy of **IAccessible** s exists or where custom object IDs are used must implement [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) themselves.</span></span>

 

 




