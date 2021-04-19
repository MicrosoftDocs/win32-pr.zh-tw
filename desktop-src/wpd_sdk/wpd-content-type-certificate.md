---
description: WPD \_ 內容 \_ 類型 \_ 憑證
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987315"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="b4b3e-103">WPD \_ 內容 \_ 類型 \_ 憑證</span><span class="sxs-lookup"><span data-stu-id="b4b3e-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="b4b3e-104">將其類型描述為 WPD \_ 內容類型憑證的物件， \_ \_ 代表用於驗證的憑證。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="b4b3e-105">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="b4b3e-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="b4b3e-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="b4b3e-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="b4b3e-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b4b3e-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b3e-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="b4b3e-109">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-109">Required.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-110">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b3e-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="b4b3e-111">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-111">Required.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-112">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="b4b3e-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="b4b3e-113">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="b4b3e-114">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b3e-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="b4b3e-115">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-115">Required.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-116">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="b4b3e-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="b4b3e-117">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-117">Required.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-118">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="b4b3e-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="b4b3e-119">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-119">Required.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-120">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="b4b3e-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="b4b3e-121">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="b4b3e-122">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="b4b3e-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="b4b3e-123">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="b4b3e-124">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b4b3e-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="b4b3e-125">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="b4b3e-126">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="b4b3e-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="b4b3e-127">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="b4b3e-128">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4b3e-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="b4b3e-129">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="b4b3e-130">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="b4b3e-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="b4b3e-131">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="b4b3e-132">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="b4b3e-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="b4b3e-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-134">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b3e-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="b4b3e-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-136">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="b4b3e-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="b4b3e-137">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="b4b3e-138">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="b4b3e-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="b4b3e-139">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-140">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="b4b3e-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="b4b3e-141">建議使用。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="b4b3e-142">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="b4b3e-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="b4b3e-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-144">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="b4b3e-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="b4b3e-145">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="b4b3e-146">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="b4b3e-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="b4b3e-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-148">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="b4b3e-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="b4b3e-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="b4b3e-150">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="b4b3e-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="b4b3e-151">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="b4b3e-152">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="b4b3e-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="b4b3e-153">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="b4b3e-154">一般資源</span><span class="sxs-lookup"><span data-stu-id="b4b3e-154">Typical Resources</span></span>

<span data-ttu-id="b4b3e-155">這些物件通常包含下列資源。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="b4b3e-156">資源名稱</span><span class="sxs-lookup"><span data-stu-id="b4b3e-156">Resource Name</span></span>                                          | <span data-ttu-id="b4b3e-157">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="b4b3e-157">Required or Optional</span></span> | <span data-ttu-id="b4b3e-158">Description</span><span class="sxs-lookup"><span data-stu-id="b4b3e-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="b4b3e-159">**WPD \_ 資源 \_ 預設**</span><span class="sxs-lookup"><span data-stu-id="b4b3e-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="b4b3e-160">必要。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-160">Required.</span></span>            | <span data-ttu-id="b4b3e-161">包含資料。</span><span class="sxs-lookup"><span data-stu-id="b4b3e-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b4b3e-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4b3e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4b3e-163">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="b4b3e-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



