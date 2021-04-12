---
description: 將其類型描述為 WPD \_ 內容類型電視的物件， \_ \_ 代表電視節目。
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319928"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="897f0-103">WPD \_ 內容 \_ 類型 \_ 電視</span><span class="sxs-lookup"><span data-stu-id="897f0-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="897f0-104">將其類型描述為 WPD \_ 內容類型電視的物件， \_ \_ 代表電視節目。</span><span class="sxs-lookup"><span data-stu-id="897f0-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="897f0-105">這種類型的物件應該裝載下列屬性。</span><span class="sxs-lookup"><span data-stu-id="897f0-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="897f0-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="897f0-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="897f0-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="897f0-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="897f0-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="897f0-109">必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="897f0-110">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="897f0-111">必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="897f0-112">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="897f0-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="897f0-113">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="897f0-114">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="897f0-115">必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="897f0-116">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="897f0-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="897f0-117">必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="897f0-118">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="897f0-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="897f0-119">必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="897f0-120">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="897f0-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="897f0-121">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="897f0-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="897f0-122">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="897f0-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="897f0-123">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="897f0-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="897f0-124">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="897f0-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="897f0-125">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="897f0-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="897f0-126">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="897f0-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="897f0-127">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="897f0-128">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="897f0-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="897f0-129">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="897f0-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="897f0-130">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="897f0-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="897f0-131">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="897f0-132">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="897f0-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="897f0-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-134">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="897f0-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-136">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="897f0-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="897f0-137">如果物件受到數位 Rights Management 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="897f0-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="897f0-138">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="897f0-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="897f0-139">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-140">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="897f0-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="897f0-141">建議使用。</span><span class="sxs-lookup"><span data-stu-id="897f0-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="897f0-142">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="897f0-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="897f0-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-144">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="897f0-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="897f0-145">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="897f0-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="897f0-146">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="897f0-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-148">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="897f0-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="897f0-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-150">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="897f0-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="897f0-151">選擇性。</span><span class="sxs-lookup"><span data-stu-id="897f0-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="897f0-152">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="897f0-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="897f0-153">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="897f0-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="897f0-154">一般資源</span><span class="sxs-lookup"><span data-stu-id="897f0-154">Typical Resources</span></span>

<span data-ttu-id="897f0-155">無。</span><span class="sxs-lookup"><span data-stu-id="897f0-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="897f0-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="897f0-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897f0-157">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="897f0-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



