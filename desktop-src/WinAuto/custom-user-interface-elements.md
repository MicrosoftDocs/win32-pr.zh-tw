---
title: 自訂消費者介面元素
description: 伺服器開發人員會根據應用程式的 UI 來設計可存取的物件。
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839532"
---
# <a name="custom-user-interface-elements"></a><span data-ttu-id="d8be6-103">自訂消費者介面元素</span><span class="sxs-lookup"><span data-stu-id="d8be6-103">Custom User Interface Elements</span></span>

<span data-ttu-id="d8be6-104">伺服器開發人員會根據應用程式的 UI 來設計可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="d8be6-104">Server developers design accessible objects based on an application's UI.</span></span> <span data-ttu-id="d8be6-105">由於 [Active Accessibility 代表系統提供的使用者介面](appendix-a--supported-user-interface-elements-reference.md) 專案（例如清單方塊、功能表和列數控制項）來執行 IAccessible 介面，因此您只需要針對下列種類的自訂 UI 元素來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面：</span><span class="sxs-lookup"><span data-stu-id="d8be6-105">Because [Active Accessibility implements the IAccessible interface on behalf of system-provided user interface elements](appendix-a--supported-user-interface-elements-reference.md) such as list boxes, menus, and trackbar controls, you need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface only for the following kinds of custom UI elements:</span></span>

-   <span data-ttu-id="d8be6-106">藉由註冊應用程式定義的視窗類別所建立的自訂控制項</span><span class="sxs-lookup"><span data-stu-id="d8be6-106">Custom controls created by registering an application-defined window class</span></span>
-   <span data-ttu-id="d8be6-107">直接在螢幕上繪製沒有相關 **HWND** 的自訂控制項</span><span class="sxs-lookup"><span data-stu-id="d8be6-107">Custom controls drawn directly on the screen that do not have an associated **HWND**</span></span>
-   <span data-ttu-id="d8be6-108">自訂控制項，例如 Microsoft ActiveX 和 JAVA 控制項</span><span class="sxs-lookup"><span data-stu-id="d8be6-108">Custom controls such as Microsoft ActiveX and Java controls</span></span>
-   <span data-ttu-id="d8be6-109">應用程式用戶端視窗中尚未公開的控制項或物件</span><span class="sxs-lookup"><span data-stu-id="d8be6-109">Controls or objects in the application's client window that aren't already exposed</span></span>

<span data-ttu-id="d8be6-110">只要您遵循用 [來公開自訂消費者介面元素的快捷方式](shortcuts-for-exposing-custom-user-interface-elements.md)中所討論的指導方針，就可以存取主控描繪控制項和功能表。</span><span class="sxs-lookup"><span data-stu-id="d8be6-110">Owner-drawn controls and menus are accessible as long as you follow the guidelines discussed in [Shortcuts for Exposing Custom User Interface Elements](shortcuts-for-exposing-custom-user-interface-elements.md).</span></span> <span data-ttu-id="d8be6-111">如果您遵循這些指導方針，就不需要針對主控描繪的控制項和功能表，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="d8be6-111">If you follow these guidelines, then you do not need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for owner-drawn controls and menus.</span></span>

<span data-ttu-id="d8be6-112">在大部分的情況下，可以存取 superclass 和子類別化控制項，因為系統會處理控制項的基本功能。</span><span class="sxs-lookup"><span data-stu-id="d8be6-112">In most cases, superclassed and subclassed controls are accessible because the system handles the basic functionality of the control.</span></span> <span data-ttu-id="d8be6-113">但是，如果 superclass 或子類別控制項大幅修改系統提供之控制項的行為，則您必須執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="d8be6-113">However, if a superclassed or subclassed control significantly modifies the behavior of the system-provided control on which it is based, then you must implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="d8be6-114">如需詳細資訊，請參閱 [根據系統控制項公開控制項](exposing-controls-based-on-system-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="d8be6-114">For more information, see [Exposing Controls Based on System Controls](exposing-controls-based-on-system-controls.md).</span></span>

<span data-ttu-id="d8be6-115">如果應用程式只使用系統提供的使用者介面元素，則不需要執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，除了其用戶端視窗以外。</span><span class="sxs-lookup"><span data-stu-id="d8be6-115">If an application uses only system-provided user interface elements, then it does not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), except for its client window.</span></span> <span data-ttu-id="d8be6-116">例如，包含文字編輯器（不是使用編輯控制項來執行）的應用程式，會將文字行公開為可存取的物件。</span><span class="sxs-lookup"><span data-stu-id="d8be6-116">For example, an application that includes a text editor, not implemented using an edit control, exposes lines of text as accessible objects.</span></span> <span data-ttu-id="d8be6-117">請注意，Microsoft Active Accessibility 會自動將 [編輯] 和 [rich edit] 控制項中的文字公開為控制項之 [ [**值**](value-property.md) ] 屬性中的單一文字字串。</span><span class="sxs-lookup"><span data-stu-id="d8be6-117">Note that Microsoft Active Accessibility automatically exposes the text in edit and rich edit controls as a single string of text in the [**Value**](value-property.md) property of the control.</span></span>

 

 




