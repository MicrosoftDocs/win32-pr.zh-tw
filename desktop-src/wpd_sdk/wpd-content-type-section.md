---
description: WPD \_ 內容 \_ 類型 \_ 區段
ms.assetid: 8680a74b-9594-4271-a511-637f617aa12a
title: WPD_CONTENT_TYPE_SECTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fbb63821f75115c5855653dc811067891652615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027294"
---
# <a name="wpd_content_type_section"></a><span data-ttu-id="44127-103">WPD \_ 內容 \_ 類型 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="44127-103">WPD\_CONTENT\_TYPE\_SECTION</span></span>

<span data-ttu-id="44127-104">將其類型描述為 WPD \_ 內容類型區段的物件， \_ \_ 代表包含在另一個物件中的資料區段。</span><span class="sxs-lookup"><span data-stu-id="44127-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SECTION represents a section of data that is contained in another object.</span></span> <span data-ttu-id="44127-105">例如，大型音訊檔案可以描述為多個章節的集合，而且每個章節都可能是 WPD \_ 內容 \_ 類型 \_ 區段物件。</span><span class="sxs-lookup"><span data-stu-id="44127-105">For example, a large audio file can be described as a collection of multiple chapters, and each chapter might be a WPD\_CONTENT\_TYPE\_SECTION object.</span></span>

<span data-ttu-id="44127-106">WPD \_ 物件 \_ 參考屬性可識別指定區段的父物件。</span><span class="sxs-lookup"><span data-stu-id="44127-106">The WPD\_OBJECT\_REFERENCES property identifies a given section's parent object.</span></span>

<span data-ttu-id="44127-107">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="44127-107">This type of object supports the following properties.</span></span>



|                                                                                                                                  |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="44127-108">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="44127-108">**Property Name**</span></span>                                                                                                                | <span data-ttu-id="44127-109">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="44127-109">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="44127-110">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="44127-110">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                           | <span data-ttu-id="44127-111">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-111">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-112">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="44127-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                            | <span data-ttu-id="44127-113">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-113">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-114">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="44127-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                                       | <span data-ttu-id="44127-115">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="44127-115">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44127-116">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="44127-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                                     | <span data-ttu-id="44127-117">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-117">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-118">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="44127-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                                   | <span data-ttu-id="44127-119">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-119">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-120">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="44127-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                                      | <span data-ttu-id="44127-121">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-121">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-122">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="44127-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                               | <span data-ttu-id="44127-123">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="44127-123">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="44127-124">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="44127-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                               | <span data-ttu-id="44127-125">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="44127-125">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="44127-126">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="44127-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                                       | <span data-ttu-id="44127-127">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="44127-127">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="44127-128">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="44127-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                                         | <span data-ttu-id="44127-129">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="44127-129">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44127-130">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="44127-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                                  | <span data-ttu-id="44127-131">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="44127-131">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="44127-132">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="44127-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                           | <span data-ttu-id="44127-133">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="44127-133">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="44127-134">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="44127-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                               | <span data-ttu-id="44127-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-136">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="44127-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="44127-137">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-137">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-138">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="44127-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                             | <span data-ttu-id="44127-139">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="44127-139">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="44127-140">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="44127-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                                      | <span data-ttu-id="44127-141">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-141">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-142">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="44127-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                                    | <span data-ttu-id="44127-143">建議使用。</span><span class="sxs-lookup"><span data-stu-id="44127-143">Recommended.</span></span>                                                          |
| [<span data-ttu-id="44127-144">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="44127-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                                    | <span data-ttu-id="44127-145">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-145">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-146">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="44127-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="44127-147">如果物件具有其他物件的參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="44127-147">Recommended if the object has references to other objects.</span></span>            |
| [<span data-ttu-id="44127-148">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="44127-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)                | <span data-ttu-id="44127-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-150">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="44127-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md)            | <span data-ttu-id="44127-151">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-151">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-152">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="44127-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                          | <span data-ttu-id="44127-153">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="44127-153">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="44127-154">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="44127-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                           | <span data-ttu-id="44127-155">選擇性。</span><span class="sxs-lookup"><span data-stu-id="44127-155">Optional.</span></span>                                                             |
| [<span data-ttu-id="44127-156">WPD \_ 區段 \_ 資料 \_ 位移</span><span class="sxs-lookup"><span data-stu-id="44127-156">WPD\_SECTION\_DATA\_OFFSET</span></span>](section-attribute-properties.md)                                           | <span data-ttu-id="44127-157">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-157">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-158">WPD \_ 區段 \_ 資料 \_ 長度</span><span class="sxs-lookup"><span data-stu-id="44127-158">WPD\_SECTION\_DATA\_LENGTH</span></span>](section-attribute-properties.md)                                           | <span data-ttu-id="44127-159">必要。</span><span class="sxs-lookup"><span data-stu-id="44127-159">Required.</span></span>                                                             |
| [<span data-ttu-id="44127-160">WPD \_ 區段 \_ 資料 \_ 單位</span><span class="sxs-lookup"><span data-stu-id="44127-160">WPD\_SECTION\_DATA\_UNITS</span></span>](section-attribute-properties.md)                                             | <span data-ttu-id="44127-161">建議使用。</span><span class="sxs-lookup"><span data-stu-id="44127-161">Recommended.</span></span>                                                          |
| [<span data-ttu-id="44127-162">WPD \_ 區段 \_ 資料 \_ 參考的 \_ 物件 \_ 資源</span><span class="sxs-lookup"><span data-stu-id="44127-162">WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE</span></span>](section-attribute-properties.md) | <span data-ttu-id="44127-163">建議使用。</span><span class="sxs-lookup"><span data-stu-id="44127-163">Recommended.</span></span>                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="44127-164">一般資源</span><span class="sxs-lookup"><span data-stu-id="44127-164">Typical Resources</span></span>

<span data-ttu-id="44127-165">這些物件通常不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="44127-165">These objects typically do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44127-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="44127-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44127-167">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="44127-167">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



