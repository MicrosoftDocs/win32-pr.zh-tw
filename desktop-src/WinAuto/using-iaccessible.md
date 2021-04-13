---
title: 使用 IAccessible 介面
description: IAccessible 介面是一組方法的集合，這些方法會公開範圍廣泛的 UI 元素最常見的屬性和行為。
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301092"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="7c553-103">使用 IAccessible 介面</span><span class="sxs-lookup"><span data-stu-id="7c553-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="7c553-104">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面是一組方法的集合，這些方法會公開範圍廣泛的 UI 元素最常見的屬性和行為。</span><span class="sxs-lookup"><span data-stu-id="7c553-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="7c553-105">UI 元素是使用者介面一部分的控制項，例如功能表或按鈕。</span><span class="sxs-lookup"><span data-stu-id="7c553-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="7c553-106">可存取的物件是具有有意義 **IAccessible** 介面的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="7c553-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="7c553-107">某些 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性不適用於每種使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="7c553-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="7c553-108">此外， **IAccessible** 的執行會因應用程式而異。</span><span class="sxs-lookup"><span data-stu-id="7c553-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="7c553-109">雖然已完整指定 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的參數和傳回值，但用戶端應該如何使用屬性或伺服器應該如何執行屬性，有時可能會受到解讀。</span><span class="sxs-lookup"><span data-stu-id="7c553-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="7c553-110">本節提供協助用戶端應用程式取得 UI 元素相關資訊，以及協助伺服器應用程式提供適當資訊的建議、指導方針和範例。</span><span class="sxs-lookup"><span data-stu-id="7c553-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c553-111">本節內容</span><span class="sxs-lookup"><span data-stu-id="7c553-111">In this section</span></span>

-   [<span data-ttu-id="7c553-112">描述性屬性的內容</span><span class="sxs-lookup"><span data-stu-id="7c553-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="7c553-113">選取範圍和焦點屬性和方法</span><span class="sxs-lookup"><span data-stu-id="7c553-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="7c553-114">物件導覽屬性和方法</span><span class="sxs-lookup"><span data-stu-id="7c553-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




