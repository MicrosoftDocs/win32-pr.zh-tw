---
description: 本主題說明提供 XPS OM 檔層級元件存取權的介面。
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: 使用 IXpsOMDocument 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977305"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="4ff19-103">使用 IXpsOMDocument 介面</span><span class="sxs-lookup"><span data-stu-id="4ff19-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="4ff19-104">本主題說明提供 XPS OM 檔層級元件存取權的介面。</span><span class="sxs-lookup"><span data-stu-id="4ff19-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="4ff19-105">介面名稱</span><span class="sxs-lookup"><span data-stu-id="4ff19-105">Interface name</span></span>                                                                        | <span data-ttu-id="4ff19-106">邏輯子介面</span><span class="sxs-lookup"><span data-stu-id="4ff19-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="4ff19-107">Description</span><span class="sxs-lookup"><span data-stu-id="4ff19-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ff19-108">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="4ff19-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="4ff19-109">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="4ff19-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="4ff19-110">代表單一 FixedDocument 元件，並系結頁面參考的集合。</span><span class="sxs-lookup"><span data-stu-id="4ff19-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="4ff19-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) 是用來逐一查看檔中 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) 介面的集合介面。</span><span class="sxs-lookup"><span data-stu-id="4ff19-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="4ff19-112">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="4ff19-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="4ff19-113">無</span><span class="sxs-lookup"><span data-stu-id="4ff19-113">None</span></span><br/>                                               | <span data-ttu-id="4ff19-114">代表 DocumentStructure 元件。</span><span class="sxs-lookup"><span data-stu-id="4ff19-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="4ff19-115">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="4ff19-115">Code Examples</span></span>

<span data-ttu-id="4ff19-116">本章節中的程式碼範例說明如何在程式中使用一些檔介面。</span><span class="sxs-lookup"><span data-stu-id="4ff19-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="4ff19-117">取得檔的頁面參考</span><span class="sxs-lookup"><span data-stu-id="4ff19-117">Get the page references of a document</span></span>

<span data-ttu-id="4ff19-118">下列程式碼範例會取得 [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)的指標，其中包含 *doc* 參數所參考檔的 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)介面清單。</span><span class="sxs-lookup"><span data-stu-id="4ff19-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="4ff19-119">取得檔的檔結構</span><span class="sxs-lookup"><span data-stu-id="4ff19-119">Get the document structure of a document</span></span>

<span data-ttu-id="4ff19-120">下列程式碼範例會取得包含檔結構的資源。</span><span class="sxs-lookup"><span data-stu-id="4ff19-120">The following code example gets the resource that contains the document structure.</span></span>


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




