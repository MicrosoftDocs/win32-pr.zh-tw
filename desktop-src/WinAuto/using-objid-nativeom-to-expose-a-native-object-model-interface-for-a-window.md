---
title: 使用 OBJID \_ NATIVEOM 來公開視窗的原生介面
description: 這項技術可讓用戶端取得視窗的自訂物件。 伺服器可以使用這個來公開視窗之自訂檔物件的指標。
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104373658"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="a0d8a-104">使用 OBJID \_ NATIVEOM 來公開視窗的原生介面</span><span class="sxs-lookup"><span data-stu-id="a0d8a-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="a0d8a-105">這項技術可讓用戶端取得視窗的自訂物件。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="a0d8a-106">伺服器可以使用這個來公開視窗之自訂檔物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="a0d8a-107">**若要公開視窗 (伺服器的原生物件模型介面)**</span><span class="sxs-lookup"><span data-stu-id="a0d8a-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="a0d8a-108">處理視窗程式中的 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="a0d8a-109">當 *lParam* 值為 [**OBJID \_ NATIVEOM**](object-identifiers.md)時，會使用 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)將介面指標傳回給自訂物件。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="a0d8a-110">如有需要，請在呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)之後釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="a0d8a-111">如需詳細資訊，請參閱 **LresultFromObject**。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="a0d8a-112">用戶端可以取得這個自訂物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="a0d8a-113">**若要為視窗 (用戶端取得自訂物件的指標)**</span><span class="sxs-lookup"><span data-stu-id="a0d8a-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="a0d8a-114">呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 並傳遞 [**OBJID \_ NATIVEOM**](object-identifiers.md) 做為第二個參數。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="a0d8a-115">請注意這項技術的下列問題：</span><span class="sxs-lookup"><span data-stu-id="a0d8a-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="a0d8a-116">這項技術類似于傳回 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，但所使用的物件識別碼不同，而 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) 會傳回自訂物件，而不是 **IAccessible**。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="a0d8a-117">伺服器開發人員可能需要發佈資訊，讓用戶端能夠唯一識別 **HWND** ，讓它們可以在其視窗控制碼上呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 之前找到。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="a0d8a-118">請勿在傳回的自訂物件上，執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="a0d8a-119">如果您這樣做，OLEACC 會將它視為標準 **IAccessible** ，而且可能會導致無法使用自訂介面。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="a0d8a-120">為了跨進程使用，傳回物件上的介面可能必須向元件物件模型註冊 (COM) 。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="a0d8a-121">許多 Microsoft Office 元件都支援此技術。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="a0d8a-122">如需詳細資訊，請參閱 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)。</span><span class="sxs-lookup"><span data-stu-id="a0d8a-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




