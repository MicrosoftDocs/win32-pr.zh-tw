---
title: 多播站屬性
description: 多播站屬性
ms.assetid: 24b81ccb-4030-49a4-802c-5b45f7dd5950
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，多播站
- 多播站屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618ffa645055bf10a9247272d57c7e3f76853c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968064"
---
# <a name="multicast-station-attributes"></a><span data-ttu-id="8b09a-108">多播站屬性</span><span class="sxs-lookup"><span data-stu-id="8b09a-108">Multicast Station Attributes</span></span>

<span data-ttu-id="8b09a-109">當檔案從多播站進行串流處理時，該工作站可以在檔案上強加某些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b09a-109">When a file is streaming from a multicast station, the station can impose some attributes on the file.</span></span> <span data-ttu-id="8b09a-110">下表所列的這些屬性實際上並不會儲存在檔案中，而且只有在檔案進行資料流程處理時才可使用。</span><span class="sxs-lookup"><span data-stu-id="8b09a-110">These attributes, listed in the following table, are not actually stored in the file and are only available when the file is streaming.</span></span> <span data-ttu-id="8b09a-111">它們包含工作站的相關資訊，而且通常會與工作站上的所有內容完全相同。</span><span class="sxs-lookup"><span data-stu-id="8b09a-111">They contain information about the station and would typically be identical for all content from the station.</span></span>



| <span data-ttu-id="8b09a-112">多播站屬性</span><span class="sxs-lookup"><span data-stu-id="8b09a-112">Multicast station attribute</span></span>                 | <span data-ttu-id="8b09a-113">全域識別碼</span><span class="sxs-lookup"><span data-stu-id="8b09a-113">Global identifier</span></span>      | <span data-ttu-id="8b09a-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="8b09a-114">Data type</span></span>             |
|---------------------------------------------|------------------------|-----------------------|
| [<span data-ttu-id="8b09a-115">**.NSC \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="8b09a-115">**NSC\_Address**</span></span>](nsc-address.md)         | <span data-ttu-id="8b09a-116">g \_ wszWMNSCAddress</span><span class="sxs-lookup"><span data-stu-id="8b09a-116">g\_wszWMNSCAddress</span></span>     | <span data-ttu-id="8b09a-117">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8b09a-117">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="8b09a-118">**.NSC \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="8b09a-118">**NSC\_Description**</span></span>](nsc-description.md) | <span data-ttu-id="8b09a-119">g \_ wszWMNSCDescription</span><span class="sxs-lookup"><span data-stu-id="8b09a-119">g\_wszWMNSCDescription</span></span> | <span data-ttu-id="8b09a-120">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8b09a-120">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="8b09a-121">**.NSC \_ 電子郵件**</span><span class="sxs-lookup"><span data-stu-id="8b09a-121">**NSC\_Email**</span></span>](nsc-email.md)             | <span data-ttu-id="8b09a-122">g \_ wszWMNSCEmail</span><span class="sxs-lookup"><span data-stu-id="8b09a-122">g\_wszWMNSCEmail</span></span>       | <span data-ttu-id="8b09a-123">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8b09a-123">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="8b09a-124">**.NSC \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="8b09a-124">**NSC\_Name**</span></span>](nsc-name.md)               | <span data-ttu-id="8b09a-125">g \_ wszWMNSCName</span><span class="sxs-lookup"><span data-stu-id="8b09a-125">g\_wszWMNSCName</span></span>        | <span data-ttu-id="8b09a-126">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8b09a-126">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="8b09a-127">**.NSC \_ 電話**</span><span class="sxs-lookup"><span data-stu-id="8b09a-127">**NSC\_Phone**</span></span>](nsc-phone.md)             | <span data-ttu-id="8b09a-128">g \_ wszWMNSCPhone</span><span class="sxs-lookup"><span data-stu-id="8b09a-128">g\_wszWMNSCPhone</span></span>       | <span data-ttu-id="8b09a-129">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="8b09a-129">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8b09a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b09a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b09a-131">**依類型的屬性**</span><span class="sxs-lookup"><span data-stu-id="8b09a-131">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="8b09a-132">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="8b09a-132">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




