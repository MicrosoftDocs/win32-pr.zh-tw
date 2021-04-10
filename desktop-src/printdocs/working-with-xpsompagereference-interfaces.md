---
description: 本主題說明如何使用提供 XPS OM 中頁面參考存取權的介面。
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: 使用 IXpsOMPageReference 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849748"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="e2abb-103">使用 IXpsOMPageReference 介面</span><span class="sxs-lookup"><span data-stu-id="e2abb-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="e2abb-104">本主題說明如何使用提供 XPS OM 中頁面參考存取權的介面。</span><span class="sxs-lookup"><span data-stu-id="e2abb-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="e2abb-105">介面名稱</span><span class="sxs-lookup"><span data-stu-id="e2abb-105">Interface name</span></span>                                                  | <span data-ttu-id="e2abb-106">邏輯子介面</span><span class="sxs-lookup"><span data-stu-id="e2abb-106">Logical child interfaces</span></span>                    | <span data-ttu-id="e2abb-107">Description</span><span class="sxs-lookup"><span data-stu-id="e2abb-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2abb-108">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="e2abb-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="e2abb-109">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="e2abb-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="e2abb-110">虛擬化檔頁面的內容。</span><span class="sxs-lookup"><span data-stu-id="e2abb-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="e2abb-111">頁面參考包含頁面的基本資訊、一些頁面屬性，以及頁面內容的連結。</span><span class="sxs-lookup"><span data-stu-id="e2abb-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="e2abb-112">由 [**IXpsOMPageReference：： GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)方法傳回包含頁面內容的 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)介面。</span><span class="sxs-lookup"><span data-stu-id="e2abb-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="e2abb-113">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="e2abb-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="e2abb-114">無</span><span class="sxs-lookup"><span data-stu-id="e2abb-114">None</span></span><br/>                             | <span data-ttu-id="e2abb-115">包含超連結目標的頁面專案清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="e2abb-116">[**IXpsOMPageReference：： CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets)方法會傳回此清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="e2abb-117">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="e2abb-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="e2abb-118">無</span><span class="sxs-lookup"><span data-stu-id="e2abb-118">None</span></span><br/>                             | <span data-ttu-id="e2abb-119">包含與頁面相關聯之部分資源的清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="e2abb-120">這份清單是由 [**IXpsOMPageReference：： CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) 方法傳回。</span><span class="sxs-lookup"><span data-stu-id="e2abb-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="e2abb-121">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="e2abb-121">Code Examples</span></span>

<span data-ttu-id="e2abb-122">下列程式碼範例說明如何使用程式中的頁面參考介面。</span><span class="sxs-lookup"><span data-stu-id="e2abb-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="e2abb-123">取得頁面內容</span><span class="sxs-lookup"><span data-stu-id="e2abb-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="e2abb-124">取得此頁面上的超連結目標清單</span><span class="sxs-lookup"><span data-stu-id="e2abb-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="e2abb-125">取得與此頁面相關聯的元件資源</span><span class="sxs-lookup"><span data-stu-id="e2abb-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="e2abb-126">取得頁面內容</span><span class="sxs-lookup"><span data-stu-id="e2abb-126">Get the page contents</span></span>

<span data-ttu-id="e2abb-127">下列程式碼範例會取得 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) 介面的指標，其中包含頁面內容。</span><span class="sxs-lookup"><span data-stu-id="e2abb-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="e2abb-128">如果頁面尚未載入至 XPS OM，則會在透過呼叫 [**IXpsOMObjectFactory：： CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile)來初始化 XPS om 時發生，呼叫 [**IXpsOMPageReference：： GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) 會將頁面載入至 XPS om。</span><span class="sxs-lookup"><span data-stu-id="e2abb-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="e2abb-129">取得此頁面上的超連結目標清單</span><span class="sxs-lookup"><span data-stu-id="e2abb-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="e2abb-130">下列程式碼範例會取得 [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) 介面的指標，其中包含超連結目標的頁面專案清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="e2abb-131">如果頁面尚未載入至 XPS OM，則會從 **PageContent. LinkTargets** 標記讀取超連結目標的清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="e2abb-132">如果已載入頁面， [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) 會檢查頁面中的每個元素，並傳回其 **IsHyperlinkTarget** 屬性為 **TRUE** 的元素清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="e2abb-133">取得與此頁面相關聯的元件資源</span><span class="sxs-lookup"><span data-stu-id="e2abb-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="e2abb-134">下列程式碼範例會取得此頁面所使用之不同資源的清單。</span><span class="sxs-lookup"><span data-stu-id="e2abb-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );
```



## <a name="related-topics"></a><span data-ttu-id="e2abb-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2abb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2abb-136">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="e2abb-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="e2abb-137">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="e2abb-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="e2abb-138">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="e2abb-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="e2abb-139">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="e2abb-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="e2abb-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e2abb-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




