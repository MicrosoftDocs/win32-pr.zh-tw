---
description: XPS 列印 API 介面
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: XPS 列印 API 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105186"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="eb1ed-103">XPS 列印 API 介面</span><span class="sxs-lookup"><span data-stu-id="eb1ed-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="eb1ed-104">\[本節所述的介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="eb1ed-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="eb1ed-105">用戶端應用程式應該改用 [列印檔案套件 API](./tailored-app-printing-api.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="eb1ed-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="eb1ed-106">\[IXpsPrintJob 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="eb1ed-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="eb1ed-107">\]</span><span class="sxs-lookup"><span data-stu-id="eb1ed-107">\]</span></span>

<span data-ttu-id="eb1ed-108">\[IXpsPrintJobStream 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="eb1ed-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="eb1ed-109">\]</span><span class="sxs-lookup"><span data-stu-id="eb1ed-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb1ed-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="eb1ed-110">In this section</span></span>



| <span data-ttu-id="eb1ed-111">介面</span><span class="sxs-lookup"><span data-stu-id="eb1ed-111">Interface</span></span>                                                   | <span data-ttu-id="eb1ed-112">描述</span><span class="sxs-lookup"><span data-stu-id="eb1ed-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb1ed-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="eb1ed-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="eb1ed-114">提供目前進行中之列印工作的存取權。</span><span class="sxs-lookup"><span data-stu-id="eb1ed-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="eb1ed-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="eb1ed-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="eb1ed-116">唯讀資料流程介面，應用程式會在其中寫入列印工作資料。</span><span class="sxs-lookup"><span data-stu-id="eb1ed-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="eb1ed-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb1ed-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb1ed-118">文件</span><span class="sxs-lookup"><span data-stu-id="eb1ed-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="eb1ed-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="eb1ed-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

