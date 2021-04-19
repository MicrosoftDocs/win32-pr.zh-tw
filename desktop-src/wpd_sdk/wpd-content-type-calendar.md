---
description: WPD \_ 內容 \_ 類型行事 \_ 曆
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975232"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="98282-103">WPD \_ 內容 \_ 類型行事 \_ 曆</span><span class="sxs-lookup"><span data-stu-id="98282-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="98282-104">將其型別描述為 WPD \_ 內容 \_ 類型行事 \_ 曆的物件代表行事曆。</span><span class="sxs-lookup"><span data-stu-id="98282-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="98282-105">物件可以是包含行事曆資訊或資料夾的檔案，其中包含與其他行事曆相關的物件，例如工作、約會等等。</span><span class="sxs-lookup"><span data-stu-id="98282-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="98282-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="98282-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="98282-107">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="98282-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="98282-108">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="98282-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="98282-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="98282-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="98282-110">必要。</span><span class="sxs-lookup"><span data-stu-id="98282-110">Required.</span></span>                                                             |
| [<span data-ttu-id="98282-111">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="98282-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="98282-112">必要。</span><span class="sxs-lookup"><span data-stu-id="98282-112">Required.</span></span>                                                             |
| [<span data-ttu-id="98282-113">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="98282-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="98282-114">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="98282-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="98282-115">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="98282-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="98282-116">必要。</span><span class="sxs-lookup"><span data-stu-id="98282-116">Required.</span></span>                                                             |
| [<span data-ttu-id="98282-117">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="98282-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="98282-118">必要。</span><span class="sxs-lookup"><span data-stu-id="98282-118">Required.</span></span>                                                             |
| [<span data-ttu-id="98282-119">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="98282-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="98282-120">必要。</span><span class="sxs-lookup"><span data-stu-id="98282-120">Required.</span></span>                                                             |
| [<span data-ttu-id="98282-121">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="98282-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="98282-122">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="98282-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="98282-123">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="98282-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="98282-124">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="98282-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="98282-125">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="98282-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="98282-126">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="98282-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="98282-127">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="98282-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="98282-128">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="98282-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="98282-129">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="98282-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="98282-130">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="98282-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="98282-131">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="98282-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="98282-132">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="98282-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="98282-133">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="98282-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="98282-134">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-135">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="98282-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="98282-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-137">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="98282-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="98282-138">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="98282-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="98282-139">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="98282-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="98282-140">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-141">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="98282-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="98282-142">建議使用。</span><span class="sxs-lookup"><span data-stu-id="98282-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="98282-143">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="98282-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="98282-144">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-145">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="98282-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="98282-146">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="98282-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="98282-147">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="98282-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="98282-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-149">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="98282-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="98282-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="98282-151">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="98282-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="98282-152">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="98282-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="98282-153">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="98282-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="98282-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="98282-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="98282-155">一般資源</span><span class="sxs-lookup"><span data-stu-id="98282-155">Typical Resources</span></span>

<span data-ttu-id="98282-156">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="98282-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="98282-157">資源名稱</span><span class="sxs-lookup"><span data-stu-id="98282-157">Resource Name</span></span>                                          | <span data-ttu-id="98282-158">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="98282-158">Required or Optional</span></span>                             | <span data-ttu-id="98282-159">Description</span><span class="sxs-lookup"><span data-stu-id="98282-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="98282-160">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="98282-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="98282-161">如果物件是由二進位資料所支援，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="98282-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="98282-162">包含資料。</span><span class="sxs-lookup"><span data-stu-id="98282-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="98282-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="98282-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98282-164">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="98282-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



