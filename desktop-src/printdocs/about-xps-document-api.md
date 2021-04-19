---
description: XPS 檔 API 會執行 XPS 物件模型，並可讓開發人員建立 XPS OM、操作原生 Windows 程式中的 XPS 檔內容 \\ \\ ，並將 xps om 儲存為檔案或串流作為 xps 檔。
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: 關於 XPS 檔 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971537"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="01a1e-103">關於 XPS 檔 API</span><span class="sxs-lookup"><span data-stu-id="01a1e-103">About XPS Document API</span></span>

<span data-ttu-id="01a1e-104">[Xps 檔 API](documents-xps.md)會執行 xps 物件模型，並可讓開發人員建立 xps om、操作原生 Windows 程式中的 xps 檔內容 \\ \\ ，並將 xps om 儲存為檔案或串流作為 xps 檔。</span><span class="sxs-lookup"><span data-stu-id="01a1e-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="01a1e-105">XPSDrv 篩選管線模組的開發人員也可以使用 XPS 檔 API，在 XPSDrv 印表機驅動程式篩選器中操作 XPS 檔內容。</span><span class="sxs-lookup"><span data-stu-id="01a1e-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="01a1e-106">XPS 檔 API 總覽</span><span class="sxs-lookup"><span data-stu-id="01a1e-106">XPS Document API Overview</span></span>

<span data-ttu-id="01a1e-107">XPS 物件模型是 XPS 檔的資訊模型。</span><span class="sxs-lookup"><span data-stu-id="01a1e-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="01a1e-108">XPS 檔的資訊模型與檔元件內使用的標記模型不同。</span><span class="sxs-lookup"><span data-stu-id="01a1e-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="01a1e-109">XPS 物件模型會描述組成 XPS 檔的內部元件組織，而標記模型則會描述這些元件的內容。</span><span class="sxs-lookup"><span data-stu-id="01a1e-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="01a1e-110">在程式中，XPS 物件模型會以 XPS OM 的形式具現化。</span><span class="sxs-lookup"><span data-stu-id="01a1e-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="01a1e-111">XPS OM 本質上是 XPS 檔內容的記憶體中版本。</span><span class="sxs-lookup"><span data-stu-id="01a1e-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="01a1e-112">在將邏輯組織與 XPS 檔類似的情況下，XPS OM 在序列化為檔案或資料流程之前，都不會被視為 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="01a1e-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="01a1e-113">當 XPS 檔從標記還原序列化為 XPS OM 時，XPS OM 無法使用正確的標記結構。</span><span class="sxs-lookup"><span data-stu-id="01a1e-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="01a1e-114">例如，無論屬性是以專案或標記中的屬性工作表示，XPS OM 都會以完全相同的方式來呈現檔物件的屬性值。</span><span class="sxs-lookup"><span data-stu-id="01a1e-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="01a1e-115">[XPS 檔 API](documents-xps.md)可分為下列類別：</span><span class="sxs-lookup"><span data-stu-id="01a1e-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="01a1e-116">XPS OM 主幹介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="01a1e-117">主幹介面可讓您存取 XPS 檔結構的最上層元件。</span><span class="sxs-lookup"><span data-stu-id="01a1e-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="01a1e-118">這些介面也提供序列化 XPS OM 和還原序列化 XPS 檔的方法。</span><span class="sxs-lookup"><span data-stu-id="01a1e-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="01a1e-119">XPS OM 頁面介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="01a1e-120">頁面介面可讓您存取 XPS 檔中的頁面內容。</span><span class="sxs-lookup"><span data-stu-id="01a1e-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="01a1e-121">描述頁面內容的介面也會包含在頁面介面中。</span><span class="sxs-lookup"><span data-stu-id="01a1e-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="01a1e-122">XPS OM 數位簽章</span><span class="sxs-lookup"><span data-stu-id="01a1e-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="01a1e-123">XPS OM 支援數位簽章。</span><span class="sxs-lookup"><span data-stu-id="01a1e-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="01a1e-124">不過，您可以直接存取 XPS 檔中的數位簽章，而不需要建立 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="01a1e-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="01a1e-125">如需有關如何在不使用 XPS OM 的情況下存取 XPS 數位簽章的詳細資訊，請參閱 [Xps 數位簽章 API](xps-digital-signatures.md)。</span><span class="sxs-lookup"><span data-stu-id="01a1e-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="01a1e-126">XPS OM 列印票證介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="01a1e-127">XPS 檔支援封裝的列印票證 (作業) 、檔和頁面層級。</span><span class="sxs-lookup"><span data-stu-id="01a1e-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="01a1e-128">列印票證包含有關如何格式化檔內容以進行列印或觀看的資訊。</span><span class="sxs-lookup"><span data-stu-id="01a1e-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01a1e-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="01a1e-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="01a1e-130">**本節內容**</span><span class="sxs-lookup"><span data-stu-id="01a1e-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="01a1e-131">XPS OM 主幹介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="01a1e-132">XPS OM 頁面介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="01a1e-133">XPS OM 數位簽章</span><span class="sxs-lookup"><span data-stu-id="01a1e-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="01a1e-134">XPS OM 列印票證介面</span><span class="sxs-lookup"><span data-stu-id="01a1e-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="01a1e-135">**其他相關主題**</span><span class="sxs-lookup"><span data-stu-id="01a1e-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="01a1e-136">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="01a1e-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="01a1e-137">XPS OM 數位簽章</span><span class="sxs-lookup"><span data-stu-id="01a1e-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="01a1e-138">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="01a1e-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="01a1e-139">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="01a1e-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



