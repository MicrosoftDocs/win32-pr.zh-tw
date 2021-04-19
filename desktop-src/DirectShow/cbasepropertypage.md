---
description: CBasePropertyPage 類別是用來執行屬性頁的抽象類別。 如果您要撰寫篩選 (或其他支援屬性頁的物件) ，請使用這個類別。
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: 'CBasePropertyPage 類別 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998632"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="01b22-104">CBasePropertyPage 類別</span><span class="sxs-lookup"><span data-stu-id="01b22-104">CBasePropertyPage class</span></span>

![cbasepropertypage 類別階層](images/cprop01.png)

<span data-ttu-id="01b22-106">`CBasePropertyPage`類別是用來執行屬性頁的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="01b22-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="01b22-107">如果您要撰寫篩選 (或其他支援屬性頁的物件) ，請使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="01b22-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="01b22-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="01b22-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="01b22-109">Description</span><span class="sxs-lookup"><span data-stu-id="01b22-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b22-110">**m \_ bDirty**</span><span class="sxs-lookup"><span data-stu-id="01b22-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="01b22-111">指出是否有任何屬性變更。</span><span class="sxs-lookup"><span data-stu-id="01b22-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="01b22-112">**m \_ DialogId**</span><span class="sxs-lookup"><span data-stu-id="01b22-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="01b22-113">對話方塊的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="01b22-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="01b22-114">**m \_ Dlg**</span><span class="sxs-lookup"><span data-stu-id="01b22-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="01b22-115">對話方塊視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="01b22-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="01b22-116">**m \_ hwnd**</span><span class="sxs-lookup"><span data-stu-id="01b22-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="01b22-117">對話方塊視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="01b22-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="01b22-118">**m \_ pPageSite**</span><span class="sxs-lookup"><span data-stu-id="01b22-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="01b22-119">屬性頁網站之 **IPropertyPageSite** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="01b22-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="01b22-120">**m \_ TitleId**</span><span class="sxs-lookup"><span data-stu-id="01b22-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="01b22-121">包含對話方塊標題之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="01b22-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="01b22-122">公用方法</span><span class="sxs-lookup"><span data-stu-id="01b22-122">Public Methods</span></span>                                                         | <span data-ttu-id="01b22-123">Description</span><span class="sxs-lookup"><span data-stu-id="01b22-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="01b22-124">**CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="01b22-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="01b22-125">函式方法。</span><span class="sxs-lookup"><span data-stu-id="01b22-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="01b22-126">**~ CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="01b22-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="01b22-127">函式方法。</span><span class="sxs-lookup"><span data-stu-id="01b22-127">Destructor method.</span></span> <span data-ttu-id="01b22-128">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="01b22-129">**OnActivate**</span><span class="sxs-lookup"><span data-stu-id="01b22-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="01b22-130">在屬性頁啟用時呼叫。</span><span class="sxs-lookup"><span data-stu-id="01b22-130">Called when the property page is activated.</span></span> <span data-ttu-id="01b22-131">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="01b22-132">**OnApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="01b22-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="01b22-133">當使用者將變更套用至屬性頁時呼叫。</span><span class="sxs-lookup"><span data-stu-id="01b22-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="01b22-134">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="01b22-135">**OnConnect**</span><span class="sxs-lookup"><span data-stu-id="01b22-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="01b22-136">提供與屬性頁相關聯之物件的 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="01b22-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="01b22-137">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="01b22-138">**OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="01b22-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="01b22-139">當對話方塊視窗終結時呼叫。</span><span class="sxs-lookup"><span data-stu-id="01b22-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="01b22-140">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="01b22-141">**OnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="01b22-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="01b22-142">當屬性頁應該釋放相關聯的物件時呼叫。</span><span class="sxs-lookup"><span data-stu-id="01b22-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="01b22-143">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="01b22-144">**OnReceiveMessage**</span><span class="sxs-lookup"><span data-stu-id="01b22-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="01b22-145">當對話方塊收到訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="01b22-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="01b22-146">虛擬。</span><span class="sxs-lookup"><span data-stu-id="01b22-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="01b22-147">IPropertyPage 方法</span><span class="sxs-lookup"><span data-stu-id="01b22-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="01b22-148">Description</span><span class="sxs-lookup"><span data-stu-id="01b22-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="01b22-149">**啟動**</span><span class="sxs-lookup"><span data-stu-id="01b22-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="01b22-150">建立對話方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="01b22-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="01b22-151">**套用**</span><span class="sxs-lookup"><span data-stu-id="01b22-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="01b22-152">將目前的屬性頁值套用至與屬性頁面相關聯的物件</span><span class="sxs-lookup"><span data-stu-id="01b22-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="01b22-153">**停用**</span><span class="sxs-lookup"><span data-stu-id="01b22-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="01b22-154">終結對話方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="01b22-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="01b22-155">**GetPageInfo**</span><span class="sxs-lookup"><span data-stu-id="01b22-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="01b22-156">抓取屬性頁的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01b22-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="01b22-157">**Help**</span><span class="sxs-lookup"><span data-stu-id="01b22-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="01b22-158">叫用屬性頁說明。</span><span class="sxs-lookup"><span data-stu-id="01b22-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="01b22-159">**IsPageDirty**</span><span class="sxs-lookup"><span data-stu-id="01b22-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="01b22-160">指出屬性頁面在啟動後，或自最近一次呼叫 **IPropertyPage：： Apply** 之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="01b22-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="01b22-161">**移動**</span><span class="sxs-lookup"><span data-stu-id="01b22-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="01b22-162">放置對話方塊並調整其大小。</span><span class="sxs-lookup"><span data-stu-id="01b22-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="01b22-163">**SetObjects**</span><span class="sxs-lookup"><span data-stu-id="01b22-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="01b22-164">為與屬性頁相關聯的物件提供 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="01b22-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="01b22-165">**SetPageSite**</span><span class="sxs-lookup"><span data-stu-id="01b22-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="01b22-166">初始化屬性頁。</span><span class="sxs-lookup"><span data-stu-id="01b22-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="01b22-167">**顯示**</span><span class="sxs-lookup"><span data-stu-id="01b22-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="01b22-168">顯示或隱藏對話方塊。</span><span class="sxs-lookup"><span data-stu-id="01b22-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="01b22-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="01b22-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="01b22-170">指示屬性頁處理按鍵。</span><span class="sxs-lookup"><span data-stu-id="01b22-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="01b22-171">備註</span><span class="sxs-lookup"><span data-stu-id="01b22-171">Remarks</span></span>

<span data-ttu-id="01b22-172">屬性頁是 COM 物件，因此您必須為類別識別碼 (CLSID) 產生 GUID，並在 [**CFactoryTemplate**](cfactorytemplate.md) 陣列中提供專案。</span><span class="sxs-lookup"><span data-stu-id="01b22-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="01b22-173">如需詳細資訊，請參閱 [DirectShow 和 COM](directshow-and-com.md)。</span><span class="sxs-lookup"><span data-stu-id="01b22-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="01b22-174">下列範例顯示一般的 class factory 專案：</span><span class="sxs-lookup"><span data-stu-id="01b22-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="01b22-175">您的篩選準則必須公開 **ISpecifyPropertyPages** 介面。</span><span class="sxs-lookup"><span data-stu-id="01b22-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="01b22-176">這個介面包含單一方法 **GetPages**，它會傳回屬性頁的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="01b22-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="01b22-177">下列範例顯示如何執行此方法：</span><span class="sxs-lookup"><span data-stu-id="01b22-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="01b22-178">請記得也要覆寫篩選準則的 **NonDelegatingQueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="01b22-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="01b22-179">如需詳細資訊，請參閱 [DirectShow 和 COM](directshow-and-com.md) 與 [**INonDelegatingUnknown**](inondelegatingunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="01b22-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="01b22-180">接下來，將對話方塊建立為專案中的資源，並建立保存對話方塊標題的字串資源。</span><span class="sxs-lookup"><span data-stu-id="01b22-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="01b22-181">這兩個資源識別碼都是 **CBasePropertyPage** 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="01b22-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="01b22-182">將標題字串保留在資源中，可讓您更輕鬆地將屬性頁當地語系化。</span><span class="sxs-lookup"><span data-stu-id="01b22-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="01b22-183">**CBasePropertyPage** 類別提供 **IPropertyPage** 介面的架構。</span><span class="sxs-lookup"><span data-stu-id="01b22-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="01b22-184">這個架構會呼叫數個虛擬方法，包括 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md)、 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md)等等。</span><span class="sxs-lookup"><span data-stu-id="01b22-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="01b22-185">在基類中，這些方法只會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="01b22-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="01b22-186">您的衍生類別必須覆寫這些虛擬方法的部分或全部。</span><span class="sxs-lookup"><span data-stu-id="01b22-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="01b22-187">如需詳細資訊，請參閱個別方法的備註。</span><span class="sxs-lookup"><span data-stu-id="01b22-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="01b22-188">如需如何使用這個類別來建立屬性頁的延伸範例，請參閱 [建立篩選屬性頁](creating-a-filter-property-page.md)。</span><span class="sxs-lookup"><span data-stu-id="01b22-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01b22-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="01b22-189">Requirements</span></span>



| <span data-ttu-id="01b22-190">需求</span><span class="sxs-lookup"><span data-stu-id="01b22-190">Requirement</span></span> | <span data-ttu-id="01b22-191">值</span><span class="sxs-lookup"><span data-stu-id="01b22-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b22-192">標頭</span><span class="sxs-lookup"><span data-stu-id="01b22-192">Header</span></span><br/>  | <dl> <span data-ttu-id="01b22-193"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="01b22-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="01b22-194">程式庫</span><span class="sxs-lookup"><span data-stu-id="01b22-194">Library</span></span><br/> | <dl> <span data-ttu-id="01b22-195"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="01b22-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




