---
description: 服務物件
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: 服務物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852555"
---
# <a name="service-object"></a><span data-ttu-id="171da-103">服務物件</span><span class="sxs-lookup"><span data-stu-id="171da-103">Service Object</span></span>

<span data-ttu-id="171da-104">服務物件必須支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="171da-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="171da-105">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="171da-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="171da-106">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="171da-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="171da-107">[WPD \_ 物件 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="171da-108">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-108">Required.</span></span> <span data-ttu-id="171da-109">.</span><span class="sxs-lookup"><span data-stu-id="171da-109">.</span></span>                                                                           |
| <span data-ttu-id="171da-110">[WPD \_ 物件 \_ 父 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="171da-111">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-111">Required.</span></span>                                                                             |
| <span data-ttu-id="171da-112">[WPD \_ 物件 \_ 名稱](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="171da-113">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-113">Required.</span></span>                                                                             |
| <span data-ttu-id="171da-114">[WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="171da-115">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-115">Required.</span></span>                                                                             |
| <span data-ttu-id="171da-116">[WPD \_ 物件 \_ ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="171da-117">如果不應該對使用者顯示服務物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="171da-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="171da-118">[WPD \_ 物件 \_ ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="171da-119">如果物件為系統物件，則為必要項 (例如，它代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="171da-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="171da-120">[WPD \_ 功能 \_ 物件 \_ 類別](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="171da-121">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-121">Required.</span></span> <span data-ttu-id="171da-122">這代表裝置服務類型，例如服務連絡人。</span><span class="sxs-lookup"><span data-stu-id="171da-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="171da-123">[WPD \_ 服務 \_ 版本](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="171da-124">必要。</span><span class="sxs-lookup"><span data-stu-id="171da-124">Required.</span></span>                                                                             |
| <span data-ttu-id="171da-125">[WPD \_ 儲存體 \_ 類型](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="171da-126">如果服務用來儲存物件，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="171da-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="171da-127">[WPD \_ 儲存體 \_ 容量](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="171da-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="171da-128">如果服務用來儲存物件，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="171da-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="171da-129">一般資源</span><span class="sxs-lookup"><span data-stu-id="171da-129">Typical Resources</span></span>

<span data-ttu-id="171da-130">這些物件通常不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="171da-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="171da-131">一般格式</span><span class="sxs-lookup"><span data-stu-id="171da-131">Typical Formats</span></span>

<span data-ttu-id="171da-132">下列清單會識別服務物件所使用的一般格式。</span><span class="sxs-lookup"><span data-stu-id="171da-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="171da-133">不過，此物件不限於這些格式。</span><span class="sxs-lookup"><span data-stu-id="171da-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="171da-134">\_ \_ 未指定 WPD 物件格式 \_</span><span class="sxs-lookup"><span data-stu-id="171da-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="171da-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="171da-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="171da-136">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="171da-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
