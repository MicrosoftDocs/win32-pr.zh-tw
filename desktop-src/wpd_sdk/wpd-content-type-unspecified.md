---
description: '\_ \_ 未指定 WPD 內容類型 \_'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423678"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="0b1bf-103">\_ \_ 未指定 WPD 內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="0b1bf-104">如果未指定 WPD 內容類型，則描述其類型的物件代表不一定 \_ \_ \_ 具有基礎實體檔案的泛型物件。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="0b1bf-105">此類型與 WPD 內容類型泛型檔案之間的差異在於 \_ \_ \_ \_ WPD \_ 內容 \_ 類型一般 \_ 檔案 \_ 物件必須有基礎實體檔案。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="0b1bf-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="0b1bf-107">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="0b1bf-107">Property Name</span></span>       | <span data-ttu-id="0b1bf-108">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="0b1bf-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="0b1bf-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1bf-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="0b1bf-110">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-110">Required, read-only.</span></span> <span data-ttu-id="0b1bf-111">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="0b1bf-112">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1bf-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="0b1bf-113">必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-114">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0b1bf-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="0b1bf-115">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="0b1bf-116">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1bf-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="0b1bf-117">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-117">Required, read-only.</span></span> <span data-ttu-id="0b1bf-118">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="0b1bf-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="0b1bf-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="0b1bf-120">必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="0b1bf-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="0b1bf-122">必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="0b1bf-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="0b1bf-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="0b1bf-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="0b1bf-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="0b1bf-126">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="0b1bf-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="0b1bf-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="0b1bf-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="0b1bf-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="0b1bf-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="0b1bf-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="0b1bf-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="0b1bf-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="0b1bf-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="0b1bf-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="0b1bf-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="0b1bf-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="0b1bf-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="0b1bf-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1bf-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="0b1bf-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="0b1bf-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="0b1bf-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="0b1bf-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="0b1bf-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="0b1bf-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="0b1bf-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="0b1bf-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="0b1bf-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="0b1bf-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="0b1bf-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1bf-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="0b1bf-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="0b1bf-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="0b1bf-152">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="0b1bf-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="0b1bf-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="0b1bf-154">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="0b1bf-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="0b1bf-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="0b1bf-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="0b1bf-157">一般資源</span><span class="sxs-lookup"><span data-stu-id="0b1bf-157">Typical Resources</span></span>

<span data-ttu-id="0b1bf-158">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="0b1bf-159">資源名稱</span><span class="sxs-lookup"><span data-stu-id="0b1bf-159">Resource Name</span></span>                                          | <span data-ttu-id="0b1bf-160">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="0b1bf-160">Required or Optional</span></span>                             | <span data-ttu-id="0b1bf-161">描述</span><span class="sxs-lookup"><span data-stu-id="0b1bf-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="0b1bf-162">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="0b1bf-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="0b1bf-163">如果物件是由二進位資料所支援，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="0b1bf-164">包含二進位資料。</span><span class="sxs-lookup"><span data-stu-id="0b1bf-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b1bf-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b1bf-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b1bf-166">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="0b1bf-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



