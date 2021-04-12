---
description: 本總覽討論視窗屬性。
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: 關於視窗屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192825"
---
# <a name="about-window-properties"></a><span data-ttu-id="895f9-103">關於視窗屬性</span><span class="sxs-lookup"><span data-stu-id="895f9-103">About Window Properties</span></span>

<span data-ttu-id="895f9-104">*視窗屬性* 是指派給視窗的任何資料。</span><span class="sxs-lookup"><span data-stu-id="895f9-104">A *window property* is any data assigned to a window.</span></span> <span data-ttu-id="895f9-105">視窗屬性通常是視窗特定資料的控制碼，但它可能是任何值。</span><span class="sxs-lookup"><span data-stu-id="895f9-105">A window property is usually a handle of the window-specific data, but it may be any value.</span></span> <span data-ttu-id="895f9-106">每個視窗屬性都是由字串名稱所識別。</span><span class="sxs-lookup"><span data-stu-id="895f9-106">Each window property is identified by a string name.</span></span> <span data-ttu-id="895f9-107">有幾個函數可讓應用程式使用視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="895f9-107">There are several functions that enable applications to use window properties.</span></span> <span data-ttu-id="895f9-108">本總覽將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="895f9-108">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="895f9-109">使用視窗屬性的優點</span><span class="sxs-lookup"><span data-stu-id="895f9-109">Advantages of Using Window Properties</span></span>](#advantages-of-using-window-properties)
-   [<span data-ttu-id="895f9-110">指派視窗屬性</span><span class="sxs-lookup"><span data-stu-id="895f9-110">Assigning Window Properties</span></span>](#assigning-window-properties)
-   [<span data-ttu-id="895f9-111">列舉視窗屬性</span><span class="sxs-lookup"><span data-stu-id="895f9-111">Enumerating Window Properties</span></span>](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a><span data-ttu-id="895f9-112">使用視窗屬性的優點</span><span class="sxs-lookup"><span data-stu-id="895f9-112">Advantages of Using Window Properties</span></span>

<span data-ttu-id="895f9-113">視窗屬性通常用來將資料與子類別化視窗或多重文件介面中的視窗產生關聯， (MDI) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="895f9-113">Window properties are typically used to associate data with a subclassed window or a window in a multiple-document interface (MDI) application.</span></span> <span data-ttu-id="895f9-114">在任何一種情況下，使用在 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函數或類別結構中指定的額外位元組並不方便，原因如下：</span><span class="sxs-lookup"><span data-stu-id="895f9-114">In either case, it is not convenient to use the extra bytes specified in the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function or class structure for the following two reasons:</span></span>

-   <span data-ttu-id="895f9-115">應用程式可能不知道有多少額外的位元組可用或空間的使用方式。</span><span class="sxs-lookup"><span data-stu-id="895f9-115">An application might not know how many extra bytes are available or how the space is being used.</span></span> <span data-ttu-id="895f9-116">藉由使用視窗屬性，應用程式可以將資料與視窗建立關聯，而不需要存取額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="895f9-116">By using window properties, the application can associate data with a window without accessing the extra bytes.</span></span>
-   <span data-ttu-id="895f9-117">應用程式必須使用位移來存取額外的位元組。</span><span class="sxs-lookup"><span data-stu-id="895f9-117">An application must access the extra bytes by using offsets.</span></span> <span data-ttu-id="895f9-118">不過，視窗屬性是由其字串識別碼存取，而不是透過位移來存取。</span><span class="sxs-lookup"><span data-stu-id="895f9-118">However, window properties are accessed by their string identifiers, not by offsets.</span></span>

<span data-ttu-id="895f9-119">如需子類別化的詳細資訊，請參閱 [windows](about-window-procedures.md)程式子類別化。</span><span class="sxs-lookup"><span data-stu-id="895f9-119">For more information about subclassing, see [Window Procedure Subclassing](about-window-procedures.md).</span></span> <span data-ttu-id="895f9-120">如需 MDI 視窗的詳細資訊，請參閱 [多個檔介面](multiple-document-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="895f9-120">For more information about MDI windows, see [Multiple Document Interface](multiple-document-interface.md).</span></span>

## <a name="assigning-window-properties"></a><span data-ttu-id="895f9-121">指派視窗屬性</span><span class="sxs-lookup"><span data-stu-id="895f9-121">Assigning Window Properties</span></span>

<span data-ttu-id="895f9-122">[**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)函式會將視窗屬性和其字串識別碼指派給視窗。</span><span class="sxs-lookup"><span data-stu-id="895f9-122">The [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) function assigns a window property and its string identifier to a window.</span></span> <span data-ttu-id="895f9-123">[**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)函式會抓取由指定字串識別的視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="895f9-123">The [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa) function retrieves the window property identified by the specified string.</span></span> <span data-ttu-id="895f9-124">[**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)函式會終結視窗和視窗屬性之間的關聯，但不會摧毀資料本身。</span><span class="sxs-lookup"><span data-stu-id="895f9-124">The [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa) function destroys the association between a window and a window property but does not destroy the data itself.</span></span> <span data-ttu-id="895f9-125">若要終結資料本身，請使用適當的函式來釋放 **RemoveProp** 傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="895f9-125">To destroy the data itself, use the appropriate function to free the handle that is returned by **RemoveProp**.</span></span>

## <a name="enumerating-window-properties"></a><span data-ttu-id="895f9-126">列舉視窗屬性</span><span class="sxs-lookup"><span data-stu-id="895f9-126">Enumerating Window Properties</span></span>

<span data-ttu-id="895f9-127">[**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)和 [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)函式會使用應用程式定義的回呼函式來列舉所有視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="895f9-127">The [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) and [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) functions enumerate all of a window's properties by using an application-defined callback function.</span></span> <span data-ttu-id="895f9-128">如需回呼函數的詳細資訊，請參閱 [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)。</span><span class="sxs-lookup"><span data-stu-id="895f9-128">For more information about the callback function, see [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).</span></span>

<span data-ttu-id="895f9-129">[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) 包含回呼函式所使用之應用程式定義資料的額外參數。</span><span class="sxs-lookup"><span data-stu-id="895f9-129">[**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) includes an extra parameter for application-defined data used by the callback function.</span></span> <span data-ttu-id="895f9-130">如需回呼函數的詳細資訊，請參閱 [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa)。</span><span class="sxs-lookup"><span data-stu-id="895f9-130">For more information about the callback function, see [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).</span></span>

 

 
