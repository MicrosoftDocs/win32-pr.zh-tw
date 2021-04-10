---
description: WPD \_ 內容 \_ 類型 \_ 無線 \_ 設定檔
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a327efa9e1a4cd3a1e5927da89ae4f9e7092196a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944898"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="ad553-103">WPD \_ 內容 \_ 類型 \_ 無線 \_ 設定檔</span><span class="sxs-lookup"><span data-stu-id="ad553-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="ad553-104">描述其類型作為 WPD \_ 內容 \_ 類型 \_ 無線設定檔的物件， \_ 代表用來存取無線網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad553-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="ad553-105">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ad553-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ad553-106">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="ad553-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="ad553-107">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="ad553-107">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="ad553-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ad553-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="ad553-109">必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-109">Required.</span></span>                                                             |
| [<span data-ttu-id="ad553-110">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ad553-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="ad553-111">必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-111">Required.</span></span>                                                             |
| [<span data-ttu-id="ad553-112">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="ad553-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="ad553-113">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="ad553-114">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ad553-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="ad553-115">必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-115">Required.</span></span>                                                             |
| [<span data-ttu-id="ad553-116">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="ad553-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="ad553-117">必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-117">Required.</span></span>                                                             |
| [<span data-ttu-id="ad553-118">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ad553-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="ad553-119">必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-119">Required.</span></span>                                                             |
| [<span data-ttu-id="ad553-120">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="ad553-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="ad553-121">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ad553-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="ad553-122">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="ad553-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="ad553-123">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="ad553-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="ad553-124">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="ad553-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="ad553-125">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ad553-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="ad553-126">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="ad553-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="ad553-127">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="ad553-128">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad553-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="ad553-129">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="ad553-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="ad553-130">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="ad553-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="ad553-131">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="ad553-132">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="ad553-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="ad553-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-134">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ad553-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="ad553-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-136">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="ad553-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="ad553-137">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ad553-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="ad553-138">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="ad553-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="ad553-139">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-140">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="ad553-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="ad553-141">建議使用。</span><span class="sxs-lookup"><span data-stu-id="ad553-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="ad553-142">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="ad553-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="ad553-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-144">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="ad553-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="ad553-145">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="ad553-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="ad553-146">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="ad553-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="ad553-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-148">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="ad553-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="ad553-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="ad553-150">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="ad553-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="ad553-151">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="ad553-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="ad553-152">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="ad553-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="ad553-153">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ad553-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="ad553-154">一般資源</span><span class="sxs-lookup"><span data-stu-id="ad553-154">Typical Resources</span></span>

<span data-ttu-id="ad553-155">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="ad553-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="ad553-156">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ad553-156">Resource Name</span></span>                                          | <span data-ttu-id="ad553-157">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="ad553-157">Required or Optional</span></span>                                  | <span data-ttu-id="ad553-158">Description</span><span class="sxs-lookup"><span data-stu-id="ad553-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="ad553-159">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="ad553-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="ad553-160">如果物件是以二進位資料表示，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="ad553-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="ad553-161">包含二進位資料。</span><span class="sxs-lookup"><span data-stu-id="ad553-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad553-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad553-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad553-163">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="ad553-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



