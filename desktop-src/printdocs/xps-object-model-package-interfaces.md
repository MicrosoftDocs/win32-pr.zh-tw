---
description: 封裝介面代表 XPS OM 的最上層，其對應于 XPS 檔檔。
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: XPS OM 封裝介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848690"
---
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="c5cd0-103">XPS OM 封裝介面</span><span class="sxs-lookup"><span data-stu-id="c5cd0-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="c5cd0-104">封裝介面代表 XPS OM 的最上層，其對應于 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="c5cd0-105">這些介面包含將 XPS OM 序列化為 XPS 檔或資料流程的方法，並將 XPS 封裝還原序列化以建立 XPS OM，讓程式能夠存取檔的內容。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="c5cd0-106">介面名稱</span><span class="sxs-lookup"><span data-stu-id="c5cd0-106">Interface name</span></span>                                                  | <span data-ttu-id="c5cd0-107">邏輯子介面</span><span class="sxs-lookup"><span data-stu-id="c5cd0-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="c5cd0-108">Description</span><span class="sxs-lookup"><span data-stu-id="c5cd0-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5cd0-109">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="c5cd0-110">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="c5cd0-111">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="c5cd0-112">與包含 XPS 檔的封裝對應的完整 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="c5cd0-113">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="c5cd0-114">無</span><span class="sxs-lookup"><span data-stu-id="c5cd0-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="c5cd0-115">啟用檔頁面至封裝的累加式序列化。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="c5cd0-116">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="c5cd0-117">無</span><span class="sxs-lookup"><span data-stu-id="c5cd0-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="c5cd0-118">存取檔中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="c5cd0-119">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="c5cd0-119">Code Examples</span></span>

<span data-ttu-id="c5cd0-120">接下來的程式碼範例將說明程式如何使用某些套件介面。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="c5cd0-121">除非另有說明，否則所有的斜體專案都是參數名稱。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="c5cd0-122">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="c5cd0-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="c5cd0-123">將 XPS OM 寫入 XPS 檔檔</span><span class="sxs-lookup"><span data-stu-id="c5cd0-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="c5cd0-124">存取 XPS OM 的檔順序</span><span class="sxs-lookup"><span data-stu-id="c5cd0-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="c5cd0-125">存取檔的 CoreProperties</span><span class="sxs-lookup"><span data-stu-id="c5cd0-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="c5cd0-126">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="c5cd0-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="c5cd0-127">從檔案名稱儲存在 *xpsDocumentFilename* 中的現有 xps 檔中，此程式碼範例會建立 *xpsPackage* 所參考的 xps OM。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="c5cd0-128">將 XPS OM 寫入 XPS 檔檔</span><span class="sxs-lookup"><span data-stu-id="c5cd0-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="c5cd0-129">下列程式碼範例會寫入 *xpsPackage* 所參考的 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="c5cd0-130">此範例會在檔案中建立一份 XPS 檔，其名稱會儲存在 *檔案名* 中。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="c5cd0-131">存取 XPS OM 的檔順序</span><span class="sxs-lookup"><span data-stu-id="c5cd0-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="c5cd0-132">下列程式碼範例會取得 [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) 介面的指標，其中包含 *xpsPackage* 所代表之 XPS OM 的檔順序。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="c5cd0-133">存取檔的 CoreProperties</span><span class="sxs-lookup"><span data-stu-id="c5cd0-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="c5cd0-134">下列程式碼範例會取得 [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) 介面的指標，讓程式能夠存取 CoreProperties 元件的內容。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="c5cd0-135">在此範例中，會假設檔已讀入 *xpsPackage* 所代表的 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="c5cd0-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a><span data-ttu-id="c5cd0-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5cd0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5cd0-137">使用 IXpsOMPackageWriter 介面</span><span class="sxs-lookup"><span data-stu-id="c5cd0-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="c5cd0-138">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="c5cd0-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c5cd0-139">**IXpsOMDocumentSequence 介面**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="c5cd0-140">**IXpsOMPackage 介面**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="c5cd0-141">**IXpsOMPackageWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="c5cd0-142">**IXpsOMCoreProperties 介面**</span><span class="sxs-lookup"><span data-stu-id="c5cd0-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




