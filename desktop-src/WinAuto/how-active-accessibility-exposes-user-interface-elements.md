---
title: Active Accessibility 如何公開消費者介面元素
description: Microsoft Active Accessibility 為其公開的每個使用者介面元素建立 proxy 物件。
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183492"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="45289-103">Active Accessibility 如何公開消費者介面元素</span><span class="sxs-lookup"><span data-stu-id="45289-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="45289-104">Microsoft Active Accessibility 為其公開的每個使用者介面元素建立 *proxy* 物件。</span><span class="sxs-lookup"><span data-stu-id="45289-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="45289-105">Proxy 物件可作為用戶端公用程式和 UI 元素之間的媒介。</span><span class="sxs-lookup"><span data-stu-id="45289-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="45289-106">Proxy 物件的目的是要監視 UI 元素的存留期範圍，並代表 UI 元素來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="45289-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="45289-107">建立自訂控制項或其他自訂 UI 元素的伺服器開發人員也應該建立 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="45289-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="45289-108">如需詳細資訊，請參閱 [建立 Proxy 物件](creating-proxy-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="45289-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="45289-109">當 Microsoft Active Accessibility 建立物件來公開預先定義或通用的控制項時，實際上會建立至少兩個物件：一個用於控制項，另一個用於圍繞控制項的視窗。</span><span class="sxs-lookup"><span data-stu-id="45289-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="45289-110">在大部分的情況下，這些父視窗具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的 [role 屬性](role-property.md)，而且具有與控制項相同的 [名稱屬性](name-property.md)和視窗類別名稱。</span><span class="sxs-lookup"><span data-stu-id="45289-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="45289-111">用戶端傳達給使用者之控制項的相關資訊會包含在 Microsoft Active Accessibility 建立來公開控制項的物件中，而不是由公開控制項周圍視窗的父物件所組成。</span><span class="sxs-lookup"><span data-stu-id="45289-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="45289-112">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="45289-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="45289-113">篩選掉不必要的物件</span><span class="sxs-lookup"><span data-stu-id="45289-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="45289-114">提供 Name 屬性</span><span class="sxs-lookup"><span data-stu-id="45289-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="45289-115">確定 UI 元素的命名正確</span><span class="sxs-lookup"><span data-stu-id="45289-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="45289-116">不支援的消費者介面元素</span><span class="sxs-lookup"><span data-stu-id="45289-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




