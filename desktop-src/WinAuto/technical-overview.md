---
title: 技術概觀
description: Microsoft Active Accessibility 改善協助工具輔助的方式 (特殊程式，協助殘障人士更有效地使用電腦) 使用在 Microsoft Windows 上執行的應用程式。
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674831"
---
# <a name="technical-overview"></a><span data-ttu-id="b4be3-103">技術概觀</span><span class="sxs-lookup"><span data-stu-id="b4be3-103">Technical Overview</span></span>

<span data-ttu-id="b4be3-104">Microsoft Active Accessibility 改善協助工具輔助的方式 (特殊程式，協助殘障人士更有效地使用電腦) 使用在 Microsoft Windows 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4be3-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="b4be3-105">Microsoft Active Accessibility 是以元件物件模型為基礎， (COM) （由 Microsoft 開發），它是一種業界標準，可定義應用程式和作業系統進行通訊的常見方式。</span><span class="sxs-lookup"><span data-stu-id="b4be3-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="b4be3-106">Microsoft Active Accessibility 是由下列元件所組成：</span><span class="sxs-lookup"><span data-stu-id="b4be3-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="b4be3-107">COM 介面 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)，它會公開 UI 元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b4be3-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="b4be3-108">**IAccessible** 也有屬性和方法，可取得和操作該 UI 元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b4be3-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="b4be3-109">WinEvents，可讓伺服器在可存取的物件變更時通知用戶端的事件系統。</span><span class="sxs-lookup"><span data-stu-id="b4be3-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="b4be3-110">Oleacc.dll，支援或執行時間 DLL。</span><span class="sxs-lookup"><span data-stu-id="b4be3-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="b4be3-111">Oleacc.dll Microsoft Active Accessibility DLL 包含下列元件：</span><span class="sxs-lookup"><span data-stu-id="b4be3-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="b4be3-112">允許用戶端要求 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標的函式 (例如 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)) 。</span><span class="sxs-lookup"><span data-stu-id="b4be3-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="b4be3-113">允許伺服器將 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標傳回給用戶端的函式 (例如 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)) 。</span><span class="sxs-lookup"><span data-stu-id="b4be3-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="b4be3-114">用來取得角色和狀態碼之當地語系化文字的函式 (例如 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 和 [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)) 。</span><span class="sxs-lookup"><span data-stu-id="b4be3-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="b4be3-115">某些 helper 函數 ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)) 。</span><span class="sxs-lookup"><span data-stu-id="b4be3-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="b4be3-116">為標準使用者和 COMCTL 控制項提供 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 預設執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b4be3-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="b4be3-117">因為這些會代表系統控制項來執行 **IAccessible** ，*所以稱為 proxy。*</span><span class="sxs-lookup"><span data-stu-id="b4be3-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4be3-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="b4be3-118">In this section</span></span>

-   [<span data-ttu-id="b4be3-119">Active Accessibility 的運作方式</span><span class="sxs-lookup"><span data-stu-id="b4be3-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="b4be3-120">Active Accessibility 基本概念</span><span class="sxs-lookup"><span data-stu-id="b4be3-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="b4be3-121">伺服器指導方針</span><span class="sxs-lookup"><span data-stu-id="b4be3-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="b4be3-122">用戶端指導方針</span><span class="sxs-lookup"><span data-stu-id="b4be3-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="b4be3-123">COM 和 Unicode 指導方針</span><span class="sxs-lookup"><span data-stu-id="b4be3-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




