---
title: 屬性工作表和屬性頁
description: 屬性工作表和屬性頁
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cc61d1e1ed0cb833632b6b627a0c683a3cb0e4
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103853203"
---
# <a name="property-sheets-and-property-pages"></a><span data-ttu-id="33c8f-103">屬性工作表和屬性頁</span><span class="sxs-lookup"><span data-stu-id="33c8f-103">Property Sheets and Property Pages</span></span>

<span data-ttu-id="33c8f-104">物件的屬性會透過 COM 介面或物件的 **IDispatch** 實作為方法公開給用戶端，讓呼叫這些方法的程式可變更屬性。</span><span class="sxs-lookup"><span data-stu-id="33c8f-104">An object's properties are exposed to clients the same as methods through either COM interfaces or the object's **IDispatch** implementation, allowing properties to be changed by programs calling these methods.</span></span> <span data-ttu-id="33c8f-105">屬性頁的 OLE 技術提供方法，讓您根據 Windows 使用者介面標準來建立物件屬性的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-105">The OLE technology of property pages provides the means to build a user interface for an object's properties according to Windows user interface standards.</span></span> <span data-ttu-id="33c8f-106">因此，這些屬性會公開給終端使用者。</span><span class="sxs-lookup"><span data-stu-id="33c8f-106">Thus, the properties are exposed to end users.</span></span> <span data-ttu-id="33c8f-107">物件的屬性工作表是索引標籤式對話方塊，其中每個索引標籤都對應至特定的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="33c8f-107">An object's property sheet is a tabbed-dialog where each tab corresponds to a specific property page.</span></span> <span data-ttu-id="33c8f-108">使用屬性頁的 OLE 模型包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="33c8f-108">The OLE model for working with property pages consists of these features:</span></span>

-   <span data-ttu-id="33c8f-109">每個屬性頁都是由執行 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 或 [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)的同進程物件所管理。</span><span class="sxs-lookup"><span data-stu-id="33c8f-109">Each property page is managed by an in-process object that implements either [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) or [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2).</span></span> <span data-ttu-id="33c8f-110">每一頁都是使用它自己的唯一 CLSID 來識別。</span><span class="sxs-lookup"><span data-stu-id="33c8f-110">Each page is identified with its own unique CLSID.</span></span>
-   <span data-ttu-id="33c8f-111">物件會藉由執行 [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages)，指定其對屬性頁的支援。</span><span class="sxs-lookup"><span data-stu-id="33c8f-111">An object specifies its support for property pages by implementing [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="33c8f-112">透過這個介面，呼叫端可以取得用來識別物件所支援之特定屬性頁的 Clsid 清單。</span><span class="sxs-lookup"><span data-stu-id="33c8f-112">Through this interface the caller can obtain a list of CLSIDs identifying the specific property pages that the object supports.</span></span> <span data-ttu-id="33c8f-113">如果物件指定屬性頁 CLSID，則物件必須能夠從屬性頁接收屬性變更。</span><span class="sxs-lookup"><span data-stu-id="33c8f-113">If the object specifies a property page CLSID, the object must be able to receive property changes from the property page.</span></span>
-   <span data-ttu-id="33c8f-114">任何程式碼 (用戶端或物件) 如果想要顯示物件的屬性工作表，則會傳遞物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標 (或陣列（如果有多個物件會受到影響）) 以及 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) 或 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)的分頁 clsid 陣列，以建立索引標籤式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="33c8f-114">Any piece of code (client or object) that wants to display an object's property sheet passes the object's [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointer (or an array if multiple objects are to be affected) along with an array of page CLSIDs to [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) or [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), which creates the tabbed-dialog box.</span></span>
-   <span data-ttu-id="33c8f-115">屬性框架對話方塊會將每個屬性頁的單一實例具現化，並在每個 CLSID 上使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 。</span><span class="sxs-lookup"><span data-stu-id="33c8f-115">The property frame dialog instantiates a single instance of each property page, using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on each CLSID.</span></span> <span data-ttu-id="33c8f-116">屬性框架至少取得每個頁面的 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 指標。</span><span class="sxs-lookup"><span data-stu-id="33c8f-116">The property frame obtains at least an [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) pointer for each page.</span></span> <span data-ttu-id="33c8f-117">此外，框架會在每個頁面本身建立一個屬性頁面網站物件。</span><span class="sxs-lookup"><span data-stu-id="33c8f-117">In addition, the frame creates a property page site object in itself for each page.</span></span> <span data-ttu-id="33c8f-118">每個網站會執行 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) ，並將此指標傳遞至每個頁面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-118">Each site implements [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) and this pointer is passed to each page.</span></span> <span data-ttu-id="33c8f-119">頁面接著會透過此介面指標與網站通訊。</span><span class="sxs-lookup"><span data-stu-id="33c8f-119">The page then communicates with the site through this interface pointer.</span></span>
-   <span data-ttu-id="33c8f-120">每個頁面也會知道已叫用物件的物件或物件;也就是說，屬性框架會將物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)指標傳遞至每個頁面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-120">Each page is also made aware of the object or objects for which it has been invoked; that is, the property frame passes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)pointers of the objects to each page.</span></span> <span data-ttu-id="33c8f-121">當指示將變更套用至物件時，每個頁面都會查詢適當的介面指標，並以任何想要的方式將新的屬性值傳遞給物件。</span><span class="sxs-lookup"><span data-stu-id="33c8f-121">When instructed to apply changes to the objects, each page queries for the appropriate interface pointer and passes new property values to the objects in whatever way is desired.</span></span> <span data-ttu-id="33c8f-122">這種通訊的發生方式不條文。</span><span class="sxs-lookup"><span data-stu-id="33c8f-122">There are no stipulations on how such communication has to happen.</span></span>
-   <span data-ttu-id="33c8f-123">物件也可以透過 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) 介面支援每個屬性流覽，讓物件指定在顯示內容頁時應接收初始焦點的屬性，以及指定用戶端在其自己的使用者介面中可顯示的字串和值。</span><span class="sxs-lookup"><span data-stu-id="33c8f-123">An object can also support per property browsing through the [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) interface permitting the object to specify which property should receive initial focus when the property page is displayed and to specify strings and values that can be displayed by the client in its own user interface.</span></span>

<span data-ttu-id="33c8f-124">下圖說明這些功能：</span><span class="sxs-lookup"><span data-stu-id="33c8f-124">These features are illustrated in the following diagram:</span></span>

![顯示內容表和屬性頁功能的圖表。](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

<span data-ttu-id="33c8f-126">這些介面的定義如下：</span><span class="sxs-lookup"><span data-stu-id="33c8f-126">These interfaces are defined as follows:</span></span>

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

<span data-ttu-id="33c8f-127">[**ISpecifyPropertyPages：： GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages)方法會傳回 (GUID) 值的計數陣列，其中每一個都描述物件所要顯示之屬性頁的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="33c8f-127">The [**ISpecifyPropertyPages::GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) method returns a counted array of UUID (GUID) values each of which describe the CLSID of a property page that the object would like displayed.</span></span> <span data-ttu-id="33c8f-128">使用 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) 或 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) 叫用屬性工作表的人員會將此陣列傳遞給函數。</span><span class="sxs-lookup"><span data-stu-id="33c8f-128">Whoever invokes the property sheet with [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) or [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) passes this array to the function.</span></span> <span data-ttu-id="33c8f-129">請注意，如果呼叫端想要顯示多個物件的屬性頁，它只能將所有物件之 CLSID 清單的交集傳遞給這些函數。</span><span class="sxs-lookup"><span data-stu-id="33c8f-129">Note that if the caller wishes to display property pages for multiple objects, it must only pass the intersection of the CLSID lists of all the objects to these functions.</span></span> <span data-ttu-id="33c8f-130">換句話說，呼叫端必須只叫用所有物件通用的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="33c8f-130">In other words, the caller must only invoke property pages that are common to all objects.</span></span>

<span data-ttu-id="33c8f-131">此外，呼叫端也會將受影響物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 指標傳遞給 API 函式。</span><span class="sxs-lookup"><span data-stu-id="33c8f-131">In addition, the caller passes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) pointers to the affected objects to the API functions as well.</span></span> <span data-ttu-id="33c8f-132">這兩個 API 函式都會建立一個屬性框架對話方塊，並使用其所載入之每個頁面的 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) 來具現化頁面網站。</span><span class="sxs-lookup"><span data-stu-id="33c8f-132">Both API functions create a property frame dialog and instantiate a page site with [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) for each page it will load.</span></span> <span data-ttu-id="33c8f-133">透過這個介面，屬性頁可以：</span><span class="sxs-lookup"><span data-stu-id="33c8f-133">Through this interface a property page can:</span></span>

-   <span data-ttu-id="33c8f-134">透過 [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid)，在屬性工作表中取出目前使用的語言。</span><span class="sxs-lookup"><span data-stu-id="33c8f-134">Retrieve the current language used in the property sheet through [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).</span></span>
-   <span data-ttu-id="33c8f-135">要求框架透過 [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator)處理按鍵。</span><span class="sxs-lookup"><span data-stu-id="33c8f-135">Ask the frame to process keystrokes through [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).</span></span>
-   <span data-ttu-id="33c8f-136">透過 [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange)通知頁面中有變更的畫面格。</span><span class="sxs-lookup"><span data-stu-id="33c8f-136">Notify the frame of changes in the page through [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).</span></span>
-   <span data-ttu-id="33c8f-137">透過 [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer)取得框架本身的介面指標，雖然目前沒有針對此框架定義的介面，但此函式一律會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="33c8f-137">Obtain an interface pointer for the frame itself through [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), although there are no interfaces defined for the frame at this time for this function always returns E\_NOTIMPL.</span></span>

<span data-ttu-id="33c8f-138">屬性框架會將每個屬性頁物件具現化，並取得每個頁面的 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 介面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-138">The property frame instantiates each property page object and obtain each page's [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span> <span data-ttu-id="33c8f-139">透過這個介面，框架會通知頁面網站 ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)) 、 [**) 的**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo) 頁面維度和 (字串，將介面指標傳遞給受影響的物件 ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)) 、告知頁面建立和終結其控制項的時機 ([**啟動**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) 和 [**停用**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)) 、指示頁面顯示或重新放置其本身 ([**顯示**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) 和 [**移動**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)) 、指示頁面將其目前的值套用到受影響的 [**物件 (套用) 、**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply) 在頁面的變更狀態 ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)) 、叫用 [說明 [**] ([**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help) 說明]) ，以及將按鍵傳送至頁面 ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)) 。</span><span class="sxs-lookup"><span data-stu-id="33c8f-139">Through this interface the frame informs the page of its page site ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), retrieves page dimensions and strings ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), passes the interface pointers to the affected objects ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), tells the page when to create and destroy its controls ([**Activate**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) and [**Deactivate**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)), instructs the page to show or reposition itself ([**Show**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) and [**Move**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), instructs the page to apply its current values to the affected objects ([**Apply**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), checks on the page's dirty status ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), invokes help ([**Help**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)), and passes keystrokes to the page ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).</span></span>

<span data-ttu-id="33c8f-140">物件也可以支援每個屬性的流覽，其提供：</span><span class="sxs-lookup"><span data-stu-id="33c8f-140">An object can also support per-property browsing, which provides:</span></span>

1.  <span data-ttu-id="33c8f-141">透過 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) 和) [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) 的方式 (，以指定在第一次顯示內容表時，應在哪個屬性頁面上取得初始焦點</span><span class="sxs-lookup"><span data-stu-id="33c8f-141">A way (through [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) and [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) to specify which property on which property page should be given the initial focus when a property sheet is first displayed</span></span>
2.  <span data-ttu-id="33c8f-142">一種方法， (物件的 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) 來指定預先定義的值，以及可在用戶端的屬性使用者介面中顯示的對應描述性字串。</span><span class="sxs-lookup"><span data-stu-id="33c8f-142">A way (through [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) for the object to specify predefined values and corresponding descriptive strings that could be displayed in a client's own user interface for properties.</span></span>

<span data-ttu-id="33c8f-143">物件可以選擇支援 (2) ，而不支援 (1) ，例如，當物件沒有屬性工作表時。</span><span class="sxs-lookup"><span data-stu-id="33c8f-143">An object can choose to support (2) without supporting (1), such as when the object has no property sheet.</span></span>

<span data-ttu-id="33c8f-144">[**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)和 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)介面的定義如下：</span><span class="sxs-lookup"><span data-stu-id="33c8f-144">The [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) and [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) interfaces are defined as follows:</span></span>

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

<span data-ttu-id="33c8f-145">為了指定其對這類功能的支援，此物件會執行 [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)。</span><span class="sxs-lookup"><span data-stu-id="33c8f-145">To specify its support for such capabilities, the object implements [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing).</span></span> <span data-ttu-id="33c8f-146">透過這個介面，呼叫端可以要求完成流覽所需的資訊，例如預先定義的字串 ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) 和值 ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) 以及指定屬性 ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)) 的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="33c8f-146">Through this interface, the caller can request the information necessary to achieve the browsing, such as predefined strings ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) and values ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) as well as a display string for a given property ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).</span></span>

<span data-ttu-id="33c8f-147">此外，用戶端可以取得屬性頁的 CLSID，讓使用者能夠編輯以 DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)) 識別的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="33c8f-147">In addition, the client can obtain the CLSID of the property page that allows the user to edit a given property identified with a DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)).</span></span> <span data-ttu-id="33c8f-148">接著，用戶端會指示屬性框架先將 CLSID 和 DISPID 傳遞給 [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)，以啟動該頁面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-148">The client then instructs the property frame to activate that page initially by passing the CLSID and the DISPID to [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect).</span></span> <span data-ttu-id="33c8f-149">畫面格會先啟用該頁面，並透過 [**IPropertyPage2：： EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty)將 DISPID 傳遞到頁面。</span><span class="sxs-lookup"><span data-stu-id="33c8f-149">The frame activates that page first and passes the DISPID to the page through [**IPropertyPage2::EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty).</span></span> <span data-ttu-id="33c8f-150">然後頁面會將焦點設定為該屬性的編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="33c8f-150">The page then sets the focus to that property's editing field.</span></span> <span data-ttu-id="33c8f-151">如此一來，用戶端就可以從自己的使用者介面中的屬性名稱跳到可操作該屬性的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="33c8f-151">In this way, a client can jump from a property name in its own user interface to the property page that can manipulate that property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33c8f-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="33c8f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c8f-153">屬性頁和屬性工作表</span><span class="sxs-lookup"><span data-stu-id="33c8f-153">Property Pages and Property Sheets</span></span>](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




