---
description: XPS 檔 API 的這個 IXpsOMPrintTicketResource 介面可讓您存取現有的列印票證，也能在 XPS OM 中建立列印票證。
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: XPS OM 列印票證介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982819"
---
# <a name="xps-om-print-ticket-interfaces"></a><span data-ttu-id="6dda6-103">XPS OM 列印票證介面</span><span class="sxs-lookup"><span data-stu-id="6dda6-103">XPS OM Print Ticket Interfaces</span></span>

<span data-ttu-id="6dda6-104">XPS 檔 API 的這個 [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) 介面可讓您存取現有的列印票證，也能在 xps OM 中建立列印票證。</span><span class="sxs-lookup"><span data-stu-id="6dda6-104">This [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) interface of the XPS Document API provides access to an existing print ticket and also the ability to create a print ticket in an XPS OM.</span></span>

## <a name="print-ticket-resources"></a><span data-ttu-id="6dda6-105">列印票證資源</span><span class="sxs-lookup"><span data-stu-id="6dda6-105">Print Ticket Resources</span></span>

<span data-ttu-id="6dda6-106">[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)介面可讓程式藉由呼叫支援列印票證之介面的 **GetPrintTicketResource** 方法，來讀取現有列印票證的內容。</span><span class="sxs-lookup"><span data-stu-id="6dda6-106">The [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) interface enables a program to read the contents of an existing print ticket by calling the **GetPrintTicketResource** method of an interface that supports a print ticket.</span></span> <span data-ttu-id="6dda6-107">藉由呼叫 **SetPrintTicketResource**，可以將新的列印票證資源新增至檔元件。</span><span class="sxs-lookup"><span data-stu-id="6dda6-107">New print ticket resources can be added to a document part by calling **SetPrintTicketResource**.</span></span>

<span data-ttu-id="6dda6-108">有三種列印票證層級，可指定列印票證的範圍。</span><span class="sxs-lookup"><span data-stu-id="6dda6-108">There are three print ticket levels, which specify the scope of the print ticket.</span></span> <span data-ttu-id="6dda6-109">列印票證層級為：工作 (或封裝) 層級、檔層級和頁面層級。</span><span class="sxs-lookup"><span data-stu-id="6dda6-109">The print ticket levels are: the job (or package) level, the document level, and the page level.</span></span> <span data-ttu-id="6dda6-110">下表顯示列印票證層級、對應的 XPS OM 介面，以及用來存取列印票證資源的方法之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="6dda6-110">The following table shows the relationship between the print ticket level, the corresponding XPS OM interface, and the methods used to access the print ticket resource.</span></span>

| <span data-ttu-id="6dda6-111">列印票證層級</span><span class="sxs-lookup"><span data-stu-id="6dda6-111">Print Ticket Level</span></span> | <span data-ttu-id="6dda6-112">介面</span><span class="sxs-lookup"><span data-stu-id="6dda6-112">Interface</span></span>                                                | <span data-ttu-id="6dda6-113">Get 方法</span><span class="sxs-lookup"><span data-stu-id="6dda6-113">Get Method</span></span>                                                                      | <span data-ttu-id="6dda6-114">Set 方法</span><span class="sxs-lookup"><span data-stu-id="6dda6-114">Set Method</span></span>                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6dda6-115">工作 (Job)</span><span class="sxs-lookup"><span data-stu-id="6dda6-115">Job</span></span>                | [<span data-ttu-id="6dda6-116">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="6dda6-116">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [<span data-ttu-id="6dda6-117">**GetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-117">**GetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [<span data-ttu-id="6dda6-118">**SetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-118">**SetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| <span data-ttu-id="6dda6-119">文件</span><span class="sxs-lookup"><span data-stu-id="6dda6-119">Document</span></span>           | [<span data-ttu-id="6dda6-120">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="6dda6-120">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [<span data-ttu-id="6dda6-121">**GetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-121">**GetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [<span data-ttu-id="6dda6-122">**SetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-122">**SetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| <span data-ttu-id="6dda6-123">頁面</span><span class="sxs-lookup"><span data-stu-id="6dda6-123">Page</span></span>               | [<span data-ttu-id="6dda6-124">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="6dda6-124">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [<span data-ttu-id="6dda6-125">**GetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-125">**GetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [<span data-ttu-id="6dda6-126">**SetPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-126">**SetPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a><span data-ttu-id="6dda6-127">列印票證內容</span><span class="sxs-lookup"><span data-stu-id="6dda6-127">Print Ticket Content</span></span>

<span data-ttu-id="6dda6-128">您可以從與資源相關聯的資料流程讀取，以存取現有列印票證資源的內容。</span><span class="sxs-lookup"><span data-stu-id="6dda6-128">The content of an existing print ticket resource can be accessed by reading from the stream associated with the resource.</span></span> <span data-ttu-id="6dda6-129">[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)介面的 [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream)方法會傳回唯讀資料流程的指標，其中包含列印票證的 XML 格式內容。</span><span class="sxs-lookup"><span data-stu-id="6dda6-129">The [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) method of the [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) interface returns the pointer to a read-only stream that contains the XML-formatted contents of the print ticket.</span></span> <span data-ttu-id="6dda6-130">列印 [架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)中說明列印票證內容的格式。</span><span class="sxs-lookup"><span data-stu-id="6dda6-130">The format of the print ticket content is described in the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6dda6-131">您可以建立新的 [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) 介面來建立新的列印票證資源。</span><span class="sxs-lookup"><span data-stu-id="6dda6-131">A new print ticket resource can be created by creating a new [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) interface.</span></span> <span data-ttu-id="6dda6-132">有效的 XML 格式列印票證會寫入資料流程，並建立元件 URI 來識別列印票證部分。</span><span class="sxs-lookup"><span data-stu-id="6dda6-132">A valid, XML-formatted print ticket is written to a stream and a part URI is created to identify the print ticket part.</span></span> <span data-ttu-id="6dda6-133">如需有效列印票證內容的詳細資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6dda6-133">For more information about the content of a valid print ticket, refer to the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span> <span data-ttu-id="6dda6-134">資料流程和元件 URI 會以 [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) 呼叫的參數形式傳遞，以設定新的列印票證資源，並藉由呼叫上表中所示的 **SetPrintTicketResource** 方法，將列印票證資源新增至對應的檔部分。</span><span class="sxs-lookup"><span data-stu-id="6dda6-134">The stream and the part URI are passed as parameters of the [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) call to set the new print ticket resource and the print ticket resource is added to the corresponding document part by calling the **SetPrintTicketResource** method shown in the preceding table.</span></span>

## <a name="print-ticket-inheritance"></a><span data-ttu-id="6dda6-135">列印票證繼承</span><span class="sxs-lookup"><span data-stu-id="6dda6-135">Print Ticket Inheritance</span></span>

<span data-ttu-id="6dda6-136">列印票證會繼承具有更大範圍的列印票證屬性。</span><span class="sxs-lookup"><span data-stu-id="6dda6-136">Print tickets inherit the properties of print tickets with greater scope.</span></span> <span data-ttu-id="6dda6-137">例如，檔層級列印票證會繼承與檔檔順序相關聯的作業層級列印票證屬性。</span><span class="sxs-lookup"><span data-stu-id="6dda6-137">For example, a document-level print ticket inherits the properties of the job-level print ticket that is associated with the document's document sequence.</span></span> <span data-ttu-id="6dda6-138">同樣地，頁面層級列印票證會繼承與分頁檔相關聯的檔層級列印票證屬性。</span><span class="sxs-lookup"><span data-stu-id="6dda6-138">Likewise, a page-level print ticket inherits the properties of the document-level print ticket that is associated with the page's document.</span></span> <span data-ttu-id="6dda6-139">在此繼承程式中，較低層級列印票證中指定的屬性會覆寫對應的屬性，這些屬性會繼承自較高層級的列印票證。</span><span class="sxs-lookup"><span data-stu-id="6dda6-139">In this inheritance process, properties that are specified in the lower-level print ticket override the corresponding properties that would otherwise be inherited from the higher-level print ticket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dda6-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="6dda6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dda6-141">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6dda6-141">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="6dda6-142">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="6dda6-142">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="6dda6-143">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="6dda6-143">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="6dda6-144">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="6dda6-144">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="6dda6-145">**IXpsOMPrintTicketResource**</span><span class="sxs-lookup"><span data-stu-id="6dda6-145">**IXpsOMPrintTicketResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[<span data-ttu-id="6dda6-146">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="6dda6-146">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



