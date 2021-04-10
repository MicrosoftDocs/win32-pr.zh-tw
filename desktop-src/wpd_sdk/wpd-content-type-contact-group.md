---
description: WPD \_ 內容 \_ 類型 \_ 連絡人 \_ 群組
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194240"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="da63d-103">WPD \_ 內容 \_ 類型 \_ 連絡人 \_ 群組</span><span class="sxs-lookup"><span data-stu-id="da63d-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="da63d-104">將其型別描述為 WPD \_ 內容 \_ 類型連絡人群組的物件 \_ \_ 代表一組連絡人。</span><span class="sxs-lookup"><span data-stu-id="da63d-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="da63d-105">此物件的 WPD \_ 物件 \_ 參考包含各種 WPD \_ 內容 \_ 類型連絡人物件的物件識別碼清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="da63d-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="da63d-106">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="da63d-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="da63d-107">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="da63d-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="da63d-108">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="da63d-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="da63d-109">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="da63d-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="da63d-110">必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-110">Required.</span></span>                                                             |
| [<span data-ttu-id="da63d-111">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="da63d-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="da63d-112">必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-112">Required.</span></span>                                                             |
| [<span data-ttu-id="da63d-113">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="da63d-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="da63d-114">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="da63d-115">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="da63d-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="da63d-116">必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-116">Required.</span></span>                                                             |
| [<span data-ttu-id="da63d-117">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="da63d-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="da63d-118">必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-118">Required.</span></span>                                                             |
| [<span data-ttu-id="da63d-119">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="da63d-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="da63d-120">必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-120">Required.</span></span>                                                             |
| [<span data-ttu-id="da63d-121">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="da63d-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="da63d-122">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="da63d-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="da63d-123">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="da63d-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="da63d-124">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="da63d-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="da63d-125">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="da63d-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="da63d-126">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="da63d-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="da63d-127">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="da63d-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="da63d-128">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="da63d-129">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="da63d-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="da63d-130">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="da63d-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="da63d-131">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="da63d-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="da63d-132">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="da63d-133">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="da63d-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="da63d-134">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="da63d-135">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="da63d-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="da63d-136">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="da63d-137">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="da63d-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="da63d-138">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="da63d-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="da63d-139">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="da63d-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="da63d-140">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="da63d-141">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="da63d-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="da63d-142">建議使用。</span><span class="sxs-lookup"><span data-stu-id="da63d-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="da63d-143">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="da63d-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="da63d-144">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="da63d-145">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="da63d-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="da63d-146">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="da63d-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="da63d-147">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="da63d-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="da63d-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="da63d-149">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="da63d-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="da63d-150">選擇性</span><span class="sxs-lookup"><span data-stu-id="da63d-150">Optional</span></span>                                                              |
| [<span data-ttu-id="da63d-151">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="da63d-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="da63d-152">如果可以刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="da63d-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="da63d-153">WPD \_ 物件 \_ 語言 \_ 地區設定</span><span class="sxs-lookup"><span data-stu-id="da63d-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="da63d-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="da63d-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="da63d-155">一般資源</span><span class="sxs-lookup"><span data-stu-id="da63d-155">Typical Resources</span></span>

<span data-ttu-id="da63d-156">無。</span><span class="sxs-lookup"><span data-stu-id="da63d-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da63d-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="da63d-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da63d-158">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="da63d-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



