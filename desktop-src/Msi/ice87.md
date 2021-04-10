---
description: ICE87 會驗證屬性資料表中未撰寫下列屬性。 您應改為在命令列上設定這些屬性。
ms.assetid: b769a01a-a610-474d-ada6-19b91441907c
title: ICE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e88a5126b4bccb4b31d6e30510807862523b775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027328"
---
# <a name="ice87"></a><span data-ttu-id="2f91d-104">ICE87</span><span class="sxs-lookup"><span data-stu-id="2f91d-104">ICE87</span></span>

<span data-ttu-id="2f91d-105">ICE87 會驗證 [屬性資料表](property-table.md)中未撰寫下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2f91d-105">ICE87 validates that the following properties have not been authored in the [Property Table](property-table.md).</span></span> <span data-ttu-id="2f91d-106">您應改為在命令列上設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f91d-106">These properties should instead be set on a command line.</span></span>

-   [<span data-ttu-id="2f91d-107">**ADDLOCAL 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-107">**ADDLOCAL property**</span></span>](addlocal.md)
-   [<span data-ttu-id="2f91d-108">**REMOVE 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-108">**REMOVE property**</span></span>](remove.md)
-   [<span data-ttu-id="2f91d-109">**ADDSOURCE 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-109">**ADDSOURCE property**</span></span>](addsource.md)
-   [<span data-ttu-id="2f91d-110">**ADDDEFAULT 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-110">**ADDDEFAULT property**</span></span>](adddefault.md)
-   [<span data-ttu-id="2f91d-111">**重新安裝屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-111">**REINSTALL property**</span></span>](reinstall.md)
-   [<span data-ttu-id="2f91d-112">**公告屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-112">**ADVERTISE property**</span></span>](advertise.md)
-   [<span data-ttu-id="2f91d-113">**COMPADDLOCAL 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-113">**COMPADDLOCAL property**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="2f91d-114">**COMPADDSOURCE 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-114">**COMPADDSOURCE property**</span></span>](compaddsource.md)
-   [<span data-ttu-id="2f91d-115">**FILEADDLOCAL 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-115">**FILEADDLOCAL property**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="2f91d-116">**FILEADDSOURCE 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-116">**FILEADDSOURCE property**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="2f91d-117">**FILEADDDEFAULT 屬性**</span><span class="sxs-lookup"><span data-stu-id="2f91d-117">**FILEADDDEFAULT property**</span></span>](fileadddefault.md)

## <a name="result"></a><span data-ttu-id="2f91d-118">結果</span><span class="sxs-lookup"><span data-stu-id="2f91d-118">Result</span></span>

<span data-ttu-id="2f91d-119">ICE87 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="2f91d-119">ICE87 posts the following warning.</span></span>



| <span data-ttu-id="2f91d-120">ICE87 警告</span><span class="sxs-lookup"><span data-stu-id="2f91d-120">ICE87 warning</span></span>                                                                                                                        | <span data-ttu-id="2f91d-121">Description</span><span class="sxs-lookup"><span data-stu-id="2f91d-121">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f91d-122">屬性 ' \[ 1 \] ' 不應撰寫至屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="2f91d-122">The property '\[1\]' shouldn't be authored into the Property table.</span></span> <span data-ttu-id="2f91d-123">這樣做可能會導致無法正確地卸載產品</span><span class="sxs-lookup"><span data-stu-id="2f91d-123">Doing so might cause the product to not be uninstalled correctly</span></span> | <span data-ttu-id="2f91d-124">無法在 [屬性工作表](property-table.md)中設定指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f91d-124">The specified property should not be set in the [Property table](property-table.md).</span></span> <span data-ttu-id="2f91d-125">請改為在命令列上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="2f91d-125">Set the property on a command line instead.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2f91d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f91d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f91d-127">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="2f91d-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



