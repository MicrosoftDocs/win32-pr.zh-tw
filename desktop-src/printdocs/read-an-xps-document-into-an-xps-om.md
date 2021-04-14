---
description: 說明如何從檔案將現有的 XPS 檔讀取至 XPS OM。
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: 將 XPS 檔讀入 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320264"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="2847a-103">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2847a-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="2847a-104">說明如何從檔案將現有的 XPS 檔讀取至 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="2847a-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="2847a-105">若要從 XPS 檔建立 XPS OM，請呼叫 [**IXpsOMObjectFactory：： CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) 方法。</span><span class="sxs-lookup"><span data-stu-id="2847a-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="2847a-106">在您的程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="2847a-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="2847a-107">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="2847a-107">Code Example</span></span>

<span data-ttu-id="2847a-108">下列程式碼範例假設 [初始化 XPS OM](xps-object-model-initialization.md) 中所述的初始化成功。</span><span class="sxs-lookup"><span data-stu-id="2847a-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="2847a-109">若要從儲存為數據流的 XPS 檔建立 XPS OM，請呼叫 [**IXpsOMObjectFactory：： CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream)。</span><span class="sxs-lookup"><span data-stu-id="2847a-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="2847a-110">備註</span><span class="sxs-lookup"><span data-stu-id="2847a-110">Remarks</span></span>

<span data-ttu-id="2847a-111">如果您在讀取 XPS 封裝之後立即撰寫 XPS OM，部分原始內容可能會遺失或變更。</span><span class="sxs-lookup"><span data-stu-id="2847a-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="2847a-112">這種情況下可能會發生的一些變更，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="2847a-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="2847a-113">檔功能</span><span class="sxs-lookup"><span data-stu-id="2847a-113">Document feature</span></span>                      | <span data-ttu-id="2847a-114">動作</span><span class="sxs-lookup"><span data-stu-id="2847a-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2847a-115">數位簽章</span><span class="sxs-lookup"><span data-stu-id="2847a-115">Digital signatures</span></span><br/>         | <span data-ttu-id="2847a-116">從檔中移除</span><span class="sxs-lookup"><span data-stu-id="2847a-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="2847a-117">DiscardControl 元件</span><span class="sxs-lookup"><span data-stu-id="2847a-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="2847a-118">從檔中移除</span><span class="sxs-lookup"><span data-stu-id="2847a-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="2847a-119">外部檔部分</span><span class="sxs-lookup"><span data-stu-id="2847a-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="2847a-120">從檔中移除</span><span class="sxs-lookup"><span data-stu-id="2847a-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="2847a-121">FixedPage 標記</span><span class="sxs-lookup"><span data-stu-id="2847a-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="2847a-122">從原始的修改</span><span class="sxs-lookup"><span data-stu-id="2847a-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="2847a-123">資源字典標記</span><span class="sxs-lookup"><span data-stu-id="2847a-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="2847a-124">如果已設定優化旗標，則從原始修改</span><span class="sxs-lookup"><span data-stu-id="2847a-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2847a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="2847a-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2847a-126">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="2847a-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="2847a-127">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2847a-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2847a-128">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2847a-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2847a-129">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="2847a-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="2847a-130">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="2847a-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="2847a-131">**在本節中使用**</span><span class="sxs-lookup"><span data-stu-id="2847a-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="2847a-132">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="2847a-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="2847a-133">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="2847a-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="2847a-134">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="2847a-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="2847a-135">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="2847a-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="2847a-136">封裝 API</span><span class="sxs-lookup"><span data-stu-id="2847a-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="2847a-137">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="2847a-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="2847a-138">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="2847a-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

