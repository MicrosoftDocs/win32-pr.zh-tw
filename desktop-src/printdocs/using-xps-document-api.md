---
description: 本節說明如何使用 XPS 檔 API 來執行程式設計工作。
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: 使用 XPS 檔 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945084"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="abb70-103">使用 XPS 檔 API</span><span class="sxs-lookup"><span data-stu-id="abb70-103">Using XPS Document API</span></span>

<span data-ttu-id="abb70-104">本節說明如何使用 [XPS 檔 API](documents-xps.md) 來執行程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="abb70-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="abb70-105">如需如何在程式中使用 [Xps 檔 api](documents-xps.md) 的範例，請參閱 [xps 檔 api 程式設計](#xps-document-api-programming-tasks) 工作一節。</span><span class="sxs-lookup"><span data-stu-id="abb70-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="abb70-106">如需有關如何使用 XPS 物件模型以及如何透過 [Xps 檔 api](documents-xps.md)來執行它的詳細資訊，請參閱 [關於 xps 檔 api](about-xps-document-api.md)。</span><span class="sxs-lookup"><span data-stu-id="abb70-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="abb70-107">使用 XPS 檔 API 開始使用</span><span class="sxs-lookup"><span data-stu-id="abb70-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="abb70-108">開始使用 XPS 檔 API 之前，請確定您已熟悉下列程式設計主題：</span><span class="sxs-lookup"><span data-stu-id="abb70-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="abb70-109">COM 程式設計</span><span class="sxs-lookup"><span data-stu-id="abb70-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="abb70-110">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="abb70-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="abb70-111">使用 XPS 檔 API 時，您可能也會想要使用下列技術：</span><span class="sxs-lookup"><span data-stu-id="abb70-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="abb70-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="abb70-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="abb70-113">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="abb70-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="abb70-114">XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="abb70-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="abb70-115">XPS 檔 API 程式設計工作</span><span class="sxs-lookup"><span data-stu-id="abb70-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="abb70-116">本節中的主題描述如何在程式中使用 [XPS 檔 API](documents-xps.md) ，並示範如何執行一些常見的程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="abb70-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="abb70-117">XPS 檔 API 會使用集合來處理介面群組。</span><span class="sxs-lookup"><span data-stu-id="abb70-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="abb70-118">使用[XPS OM 集合介面](working-with-xps-object-model-collection-interfaces.md)描述如何使用這些集合進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="abb70-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="abb70-119">[常見的 XPS 檔程式設計](common-xps-document-tasks.md)工作包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="abb70-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="abb70-120">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="abb70-121">建立空白的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="abb70-122">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="abb70-123">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="abb70-124">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="abb70-125">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="abb70-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="abb70-126">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="abb70-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="abb70-127">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="abb70-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="abb70-128">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="abb70-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="abb70-129">[ADVANCED XPS 檔程式設計](advanced-xps-document-tasks.md)工作包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="abb70-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="abb70-130">合併 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="abb70-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="abb70-131">在 XPSDrv 篩選中處理 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="abb70-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="abb70-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="abb70-132">Related topics</span></span>

<dl> <span data-ttu-id="abb70-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="abb70-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="abb70-134">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="abb70-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="abb70-135">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="abb70-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
