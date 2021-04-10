---
description: 描述如何將程式中的 XPS OM 內容寫入 XPS 檔檔。
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: 將 XPS OM 寫入 XPS 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193612"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="b2552-103">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="b2552-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="b2552-104">描述如何將程式中的 XPS OM 內容寫入 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="b2552-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="b2552-105">如果程式的 XPS OM 包含完整的檔，程式可以藉由呼叫 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)方法，以 xps 檔的形式將 xps om 寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="b2552-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="b2552-106">在程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="b2552-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="b2552-107">將完整的 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="b2552-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="b2552-108">設定 XPS OM 的內容之後，您可以藉由呼叫 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)方法，將 XPS om 儲存為 xps 檔。</span><span class="sxs-lookup"><span data-stu-id="b2552-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="b2552-109">將 XPS OM 寫入檔案或資料流程時，不會自動建立 XPS 檔的縮圖。</span><span class="sxs-lookup"><span data-stu-id="b2552-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="b2552-110">若要建立 XPS 檔的縮圖，請使用 [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="b2552-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="b2552-111">以累加方式撰寫 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="b2552-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="b2552-112">[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面可以用來以累加方式寫入 XPS 檔的元件;例如，當檔元件依序建立或處理時。</span><span class="sxs-lookup"><span data-stu-id="b2552-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="b2552-113">將 XPS OM 寫入檔案或資料流程時，不會自動建立 XPS 檔的縮圖。</span><span class="sxs-lookup"><span data-stu-id="b2552-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="b2552-114">若要建立 XPS 檔的縮圖，請使用 [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="b2552-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2552-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2552-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b2552-116">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="b2552-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="b2552-117">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="b2552-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="b2552-118">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="b2552-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="b2552-119">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="b2552-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="b2552-120">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="b2552-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="b2552-121">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="b2552-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="b2552-122">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="b2552-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="b2552-123">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="b2552-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="b2552-124">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="b2552-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b2552-125">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b2552-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
