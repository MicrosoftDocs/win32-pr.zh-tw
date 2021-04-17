---
description: WPD \_ 內容 \_ 類型 \_ 一般 \_ 訊息
ms.assetid: 8e58d15f-ee51-42c2-9d8b-6c3b9c730ff4
title: WPD_CONTENT_TYPE_GENERIC_MESSAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febde68787366dc0f84b1b187f1393017ceb9c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319935"
---
# <a name="wpd_content_type_generic_message"></a><span data-ttu-id="f7931-103">WPD \_ 內容 \_ 類型 \_ 一般 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="f7931-103">WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE</span></span>

<span data-ttu-id="f7931-104">描述其類型作為 WPD \_ 內容 \_ 類型一般訊息的物件， \_ \_ 代表訊息，例如 SMS、電子郵件等等。</span><span class="sxs-lookup"><span data-stu-id="f7931-104">An object that describes its type as WPD\_CONTENT\_TYPE\_GENERIC\_MESSAGE represents a message, for example, SMS, e-mail, and so on.</span></span>

<span data-ttu-id="f7931-105">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f7931-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="f7931-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="f7931-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="f7931-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="f7931-107">Required or Optional</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="f7931-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7931-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="f7931-109">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="f7931-109">Required, read-only.</span></span> <span data-ttu-id="f7931-110">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f7931-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="f7931-111">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7931-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="f7931-112">必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="f7931-113">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="f7931-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="f7931-114">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="f7931-115">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7931-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="f7931-116">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="f7931-116">Required, read-only.</span></span> <span data-ttu-id="f7931-117">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f7931-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="f7931-118">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="f7931-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="f7931-119">必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-119">Required.</span></span>                                                                      |
| [<span data-ttu-id="f7931-120">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="f7931-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="f7931-121">必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-121">Required.</span></span>                                                                      |
| [<span data-ttu-id="f7931-122">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="f7931-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="f7931-123">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="f7931-123">Required if the object is hidden.</span></span>                                              |
| [<span data-ttu-id="f7931-124">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="f7931-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="f7931-125">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="f7931-125">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="f7931-126">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f7931-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="f7931-127">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="f7931-127">Required if the object has at least one resource.</span></span>                              |
| [<span data-ttu-id="f7931-128">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="f7931-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="f7931-129">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-129">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="f7931-130">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="f7931-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="f7931-131">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="f7931-131">Recommended if the object is not meant for consumption by the device.</span></span>          |
| [<span data-ttu-id="f7931-132">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="f7931-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="f7931-133">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-133">Required if the object has references to other objects.</span></span>                        |
| [<span data-ttu-id="f7931-134">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="f7931-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="f7931-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-135">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-136">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7931-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="f7931-137">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-137">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-138">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="f7931-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="f7931-139">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="f7931-139">Required if the object is protected by DRM technology.</span></span>                         |
| [<span data-ttu-id="f7931-140">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="f7931-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="f7931-141">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-141">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-142">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="f7931-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="f7931-143">建議使用。</span><span class="sxs-lookup"><span data-stu-id="f7931-143">Recommended.</span></span>                                                                   |
| [<span data-ttu-id="f7931-144">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="f7931-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="f7931-145">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-145">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-146">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="f7931-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="f7931-147">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="f7931-147">Recommended if the object is referenced by another object.</span></span>                     |
| [<span data-ttu-id="f7931-148">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7931-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="f7931-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-149">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-150">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="f7931-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="f7931-151">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-151">Optional.</span></span>                                                                      |
| [<span data-ttu-id="f7931-152">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="f7931-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="f7931-153">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="f7931-153">Required if the object can be deleted.</span></span>                                         |
| [<span data-ttu-id="f7931-154">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="f7931-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="f7931-155">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f7931-155">Optional.</span></span>                                                                      |



 

## <a name="typical-resources"></a><span data-ttu-id="f7931-156">一般資源</span><span class="sxs-lookup"><span data-stu-id="f7931-156">Typical Resources</span></span>

<span data-ttu-id="f7931-157">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="f7931-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="f7931-158">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f7931-158">Resource Name</span></span>                                          | <span data-ttu-id="f7931-159">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="f7931-159">Required or Optional</span></span>                                  | <span data-ttu-id="f7931-160">Description</span><span class="sxs-lookup"><span data-stu-id="f7931-160">Description</span></span>        |
|--------------------------------------------------------|-------------------------------------------------------|--------------------|
| [<span data-ttu-id="f7931-161">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="f7931-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="f7931-162">如果支援二進位資料的物件，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="f7931-162">Required if the object is supported with binary data.</span></span> | <span data-ttu-id="f7931-163">包含資料。</span><span class="sxs-lookup"><span data-stu-id="f7931-163">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f7931-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7931-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7931-165">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="f7931-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



