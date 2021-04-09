---
title: 透過 IPropertyNotifySink 的資料系結
description: 透過 IPropertyNotifySink 的資料系結
ms.assetid: 275a84b3-65d8-43de-bfba-72e3e5ee59fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d39c7277d27f0df6c185fc35a926aa98b77b91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675708"
---
# <a name="data-binding-through-ipropertynotifysink"></a><span data-ttu-id="88e6c-103">透過 IPropertyNotifySink 的資料系結</span><span class="sxs-lookup"><span data-stu-id="88e6c-103">Data Binding through IPropertyNotifySink</span></span>

<span data-ttu-id="88e6c-104">支援屬性的物件（例如透過 OLE Automation 和 **IDispatch** 介面）可能會想要允許在某些屬性變更值時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="88e6c-104">Objects that support properties, for example, through OLE Automation and the **IDispatch** interface, may want to allow clients to be notified when certain properties change value.</span></span> <span data-ttu-id="88e6c-105">這類屬性稱為可系結屬性，因為通知可讓用戶端同步處理它自己的物件目前屬性值的顯示。</span><span class="sxs-lookup"><span data-stu-id="88e6c-105">Such a property is called a bindable property because the notifications allow a client to synchronize its own display of the object's current property values.</span></span> <span data-ttu-id="88e6c-106">此外，相同的物件可能會想要允許用戶端控制何時允許變更特定屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-106">In addition, the same objects may wish to allow a client to control when certain properties are allowed to change.</span></span> <span data-ttu-id="88e6c-107">這類屬性稱為「要求編輯屬性」。</span><span class="sxs-lookup"><span data-stu-id="88e6c-107">Such properties are called request edit properties.</span></span>

<span data-ttu-id="88e6c-108">[**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)是一種標準的通知介面，可支援可系結和要求編輯的屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-108">The [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) is a standard notification interface that supports bindable and request-edit properties.</span></span> <span data-ttu-id="88e6c-109">從具有屬性（property）輸出介面的物件，支援 **IPropertyNotifySink** 。</span><span class="sxs-lookup"><span data-stu-id="88e6c-109">**IPropertyNotifySink** is supported from an object with properties as an outgoing interface.</span></span> <span data-ttu-id="88e6c-110">也就是說，介面本身是由用戶端的接收物件所執行，而且用戶端會透過稍早所述的連接點機制，將接收器連接至支援的物件。</span><span class="sxs-lookup"><span data-stu-id="88e6c-110">That is, the interface itself is implemented by a client's sink object, and the client connects the sink to the supporting object through the connection point mechanism described earlier.</span></span> <span data-ttu-id="88e6c-111">**IPropertyNotifySink** 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="88e6c-111">The **IPropertyNotifySink** is defined as follows:</span></span>

``` syntax
interface IPropertyNotifySink : IUnknown 
  { 
    HRESULT OnChanged([in] DISPID dispID); 
    HRESULT OnRequestEdit([in] DISPID dispID); 
  } 
 
```

<span data-ttu-id="88e6c-112">當物件希望通知其連接的接收時，以指定的 DISPID 識別的可系結屬性已變更時，它會呼叫 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)。</span><span class="sxs-lookup"><span data-stu-id="88e6c-112">When an object wishes to notify its connected sinks that a bindable property identified with a given DISPID has changed, it calls [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged).</span></span> <span data-ttu-id="88e6c-113">如果物件一次變更多個屬性，則會將 DISPID \_ 未知傳遞給 **OnChanged** ，在此情況下，用戶端會重新整理其所有相關屬性值的快取。</span><span class="sxs-lookup"><span data-stu-id="88e6c-113">If an object changes multiple properties at once, it can pass DISPID\_UNKNOWN to **OnChanged** in which case a client refreshes its cache of all property values of interest.</span></span>

<span data-ttu-id="88e6c-114">當要求編輯屬性即將變更時，物件會要求用戶端是否允許發生變更。</span><span class="sxs-lookup"><span data-stu-id="88e6c-114">When a request edit property is about to change, an object can ask the client whether it will allow that change to occur.</span></span> <span data-ttu-id="88e6c-115">物件會呼叫 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) ，並將有問題的 dispid 屬性 (或 dispid \_ 未知，以找出) 的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-115">The object calls [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) passing the DISPID of the property in question (or DISPID\_UNKNOWN to identify all properties).</span></span> <span data-ttu-id="88e6c-116">用戶端的接收會傳回「 \_ 確定」，表示允許變更或 \_ (的錯誤，或) 指出不允許變更。</span><span class="sxs-lookup"><span data-stu-id="88e6c-116">The client's sink returns S\_OK to indicate that the change is allowed, or S\_FALSE (or an error) to indicate that change is not allowed.</span></span> <span data-ttu-id="88e6c-117">當物件呼叫 **OnRequestEdit** 時，必須遵循「確定」和「FALSE」傳回值的確切語義來遵守用戶端的願望 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="88e6c-117">When an object calls **OnRequestEdit**, it is required to obey the client's wishes by following the exact semantics of S\_OK and S\_FALSE return values.</span></span>

<span data-ttu-id="88e6c-118">請注意， [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) 無法用於資料驗證，因為在呼叫時，屬性的新值還無法使用。</span><span class="sxs-lookup"><span data-stu-id="88e6c-118">Note that [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) cannot be used for data validation because at the time of the call, the new value of the property is not yet available.</span></span> <span data-ttu-id="88e6c-119">通知只能用來控制屬性的唯讀狀態。</span><span class="sxs-lookup"><span data-stu-id="88e6c-119">The notification can only be used to control a read-only state for a property.</span></span>

<span data-ttu-id="88e6c-120">物件可控制哪些屬性是可系結的，並且要求編輯並在物件的型別資訊中標記這類屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-120">Objects control which properties are bindable and request edit and mark such properties in the object's type information.</span></span> <span data-ttu-id="88e6c-121">在類型資訊中，屬性可系結將屬性標示為支援 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged)。</span><span class="sxs-lookup"><span data-stu-id="88e6c-121">In the type information, the attribute bindable marks a property as supporting [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged).</span></span> <span data-ttu-id="88e6c-122">屬性 requestedit 會將屬性標示為支援 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit)。</span><span class="sxs-lookup"><span data-stu-id="88e6c-122">The attribute requestedit marks a property as supporting [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit).</span></span>

<span data-ttu-id="88e6c-123">其中一個屬性可支援這兩種行為，在這種情況下，會先呼叫 [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) ，而且只有在允許變更時才會呼叫 [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) 。</span><span class="sxs-lookup"><span data-stu-id="88e6c-123">One property can support both behaviors in which case [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) is called first, and only if change is allowed is [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) called.</span></span>

<span data-ttu-id="88e6c-124">這類屬性行為的唯一例外狀況是，由於物件的初始化或載入程式，不會傳送任何通知。</span><span class="sxs-lookup"><span data-stu-id="88e6c-124">The one exception to the behavior of such properties is that no notifications are sent as a result of an object's initialization or loading procedures.</span></span> <span data-ttu-id="88e6c-125">在這種情況下，會假設所有屬性都有變更，而且必須允許全部變更。</span><span class="sxs-lookup"><span data-stu-id="88e6c-125">At such times, it is assumed that all properties change and that all must be allowed to change.</span></span> <span data-ttu-id="88e6c-126">因此，只有在完全初始化/已載入物件的內容中，此介面的通知才有意義。</span><span class="sxs-lookup"><span data-stu-id="88e6c-126">Notifications to this interface are therefore only meaningful in the context of a fully initialized/loaded object.</span></span>

<span data-ttu-id="88e6c-127">您可以將其他兩個屬性套用至物件類型資訊中的屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-127">Two other attributes can be applied to properties in an object's type information.</span></span> <span data-ttu-id="88e6c-128">Defaultbind 屬性會將可系結屬性標示為最能表示整體物件狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="88e6c-128">The defaultbind attribute marks a bindable property as being the one that best represents the state of the object as a whole.</span></span> <span data-ttu-id="88e6c-129">Displaybind 屬性會將可系結的屬性標示為適合在用戶端自己的使用者介面中顯示。</span><span class="sxs-lookup"><span data-stu-id="88e6c-129">The displaybind attribute marks a bindable property as suitable for display in a client's own user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e6c-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="88e6c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e6c-131">屬性頁和屬性工作表</span><span class="sxs-lookup"><span data-stu-id="88e6c-131">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




