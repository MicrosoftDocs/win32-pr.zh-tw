---
title: 如何處理 WM_GETOBJECT
description: 當它收到 \_ 包含 OBJID 用戶端的 WM GETOBJECT 訊息時 \_ ，伺服器必須將指標傳回至執行 IAccessible 的物件。
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674011"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="218de-103">如何處理 WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="218de-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="218de-104">當它收到包含 [**OBJID \_ 用戶端**](object-identifiers.md)的 [**WM \_ GETOBJECT**](wm-getobject.md)訊息時，伺服器必須將指標傳回至執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的物件。</span><span class="sxs-lookup"><span data-stu-id="218de-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="218de-105">此指標是透過呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)取得的 LRESULT。</span><span class="sxs-lookup"><span data-stu-id="218de-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="218de-106">Microsoft Active Accessibility，結合元件物件模型 (COM) 程式庫時，會執行適當的封送處理，並將 **IAccessible** 介面指標從伺服器傳遞至用戶端。</span><span class="sxs-lookup"><span data-stu-id="218de-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="218de-107">伺服器必須正確處理可存取物件上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="218de-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="218de-108">請記住，當您建立 COM 物件時，參考計數為1。</span><span class="sxs-lookup"><span data-stu-id="218de-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="218de-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 之後，會進一步遞增參考計數數次。</span><span class="sxs-lookup"><span data-stu-id="218de-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="218de-110">當不再需要物件時，會自動釋放 **LresultFromObject** 所建立的所有參考，但是伺服器會負責釋出初始參考，除非它這麼做，否則物件永遠不會被終結。</span><span class="sxs-lookup"><span data-stu-id="218de-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="218de-111">下列各節中的範例示範如何釋放可存取物件的參考。</span><span class="sxs-lookup"><span data-stu-id="218de-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="218de-112">伺服器通常會以下列其中一種方式處理 [**WM \_ GETOBJECT**](wm-getobject.md) ：</span><span class="sxs-lookup"><span data-stu-id="218de-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="218de-113">建立新的可存取物件</span><span class="sxs-lookup"><span data-stu-id="218de-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="218de-114">重複使用物件的現有指標</span><span class="sxs-lookup"><span data-stu-id="218de-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="218de-115">建立相同物件的新介面</span><span class="sxs-lookup"><span data-stu-id="218de-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="218de-116">在本節的其餘部分中，討論到 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標時，此指標實際上可能是包裝 **IAccessible** 介面之 proxy 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="218de-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="218de-117">如需 proxy 物件的詳細資訊，請參閱 [建立 Proxy 物件](creating-proxy-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="218de-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="218de-118">如需有關 [**wm \_ getobject**](wm-getobject.md)的總覽，請參閱 [Wm getobject 的 \_ 運作方式](how-wm-getobject-works.md)。</span><span class="sxs-lookup"><span data-stu-id="218de-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




