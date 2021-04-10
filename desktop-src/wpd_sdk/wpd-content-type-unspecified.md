---
description: '\_ \_ 未指定 WPD 內容類型 \_'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b767ba2d76dc569def42b80eb646ae0e6a6aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851396"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="31484-103">\_ \_ 未指定 WPD 內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="31484-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="31484-104">如果未指定 WPD 內容類型，則描述其類型的物件代表不一定 \_ \_ \_ 具有基礎實體檔案的泛型物件。</span><span class="sxs-lookup"><span data-stu-id="31484-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="31484-105">此類型與 WPD 內容類型泛型檔案之間的差異在於 \_ \_ \_ \_ WPD \_ 內容 \_ 類型一般 \_ 檔案 \_ 物件必須有基礎實體檔案。</span><span class="sxs-lookup"><span data-stu-id="31484-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="31484-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="31484-106">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="31484-107">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="31484-107">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="31484-108">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="31484-108">**Required or Optional**</span></span>                                                      |
| [<span data-ttu-id="31484-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="31484-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="31484-110">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="31484-110">Required, read-only.</span></span> <span data-ttu-id="31484-111">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="31484-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="31484-112">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="31484-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="31484-113">必要。</span><span class="sxs-lookup"><span data-stu-id="31484-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="31484-114">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="31484-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="31484-115">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="31484-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="31484-116">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="31484-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="31484-117">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="31484-117">Required, read-only.</span></span> <span data-ttu-id="31484-118">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="31484-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="31484-119">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="31484-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="31484-120">必要。</span><span class="sxs-lookup"><span data-stu-id="31484-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="31484-121">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="31484-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="31484-122">必要。</span><span class="sxs-lookup"><span data-stu-id="31484-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="31484-123">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="31484-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="31484-124">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="31484-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="31484-125">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="31484-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="31484-126">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="31484-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="31484-127">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="31484-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="31484-128">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="31484-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="31484-129">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="31484-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="31484-130">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="31484-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="31484-131">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="31484-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="31484-132">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="31484-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="31484-133">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="31484-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="31484-134">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="31484-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="31484-135">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="31484-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="31484-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-137">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="31484-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="31484-138">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-139">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="31484-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="31484-140">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="31484-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="31484-141">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="31484-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="31484-142">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-143">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="31484-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="31484-144">建議使用。</span><span class="sxs-lookup"><span data-stu-id="31484-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="31484-145">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="31484-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="31484-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-147">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="31484-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="31484-148">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="31484-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="31484-149">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="31484-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="31484-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-151">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="31484-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="31484-152">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="31484-153">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="31484-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="31484-154">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="31484-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="31484-155">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="31484-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="31484-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="31484-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="31484-157">一般資源</span><span class="sxs-lookup"><span data-stu-id="31484-157">Typical Resources</span></span>

<span data-ttu-id="31484-158">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="31484-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="31484-159">資源名稱</span><span class="sxs-lookup"><span data-stu-id="31484-159">Resource Name</span></span>                                          | <span data-ttu-id="31484-160">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="31484-160">Required or Optional</span></span>                             | <span data-ttu-id="31484-161">Description</span><span class="sxs-lookup"><span data-stu-id="31484-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="31484-162">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="31484-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="31484-163">如果物件是由二進位資料所支援，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="31484-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="31484-164">包含二進位資料。</span><span class="sxs-lookup"><span data-stu-id="31484-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="31484-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="31484-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31484-166">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="31484-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



