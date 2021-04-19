---
description: WPD \_ 內容 \_ 類型 \_ 網路 \_ 關聯
ms.assetid: 5c17aba1-98f7-4d6c-a5d2-2b4623a65255
title: WPD_CONTENT_TYPE_NETWORK_ASSOCIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab3fd2f76efef5b85991f1334977c17e34d06b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985293"
---
# <a name="wpd_content_type_network_association"></a><span data-ttu-id="2190b-103">WPD \_ 內容 \_ 類型 \_ 網路 \_ 關聯</span><span class="sxs-lookup"><span data-stu-id="2190b-103">WPD\_CONTENT\_TYPE\_NETWORK\_ASSOCIATION</span></span>

<span data-ttu-id="2190b-104">將其型別描述為 WPD \_ 內容 \_ 類型網路關聯的物件， \_ \_ 代表主機與裝置之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="2190b-104">An object that describes its type as WPD\_CONTENT\_TYPE\_NETWORK\_ASSOCIATION represents an association between a host and a device.</span></span>

<span data-ttu-id="2190b-105">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="2190b-105">This type of object supports the following properties.</span></span>



|                                                                                                                                              |                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="2190b-106">**屬性名稱**</span><span class="sxs-lookup"><span data-stu-id="2190b-106">**Property Name**</span></span>                                                                                                                            | <span data-ttu-id="2190b-107">**必要或選擇性**</span><span class="sxs-lookup"><span data-stu-id="2190b-107">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="2190b-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                                       | <span data-ttu-id="2190b-109">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-109">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-110">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                                        | <span data-ttu-id="2190b-111">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-111">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-112">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2190b-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                                                   | <span data-ttu-id="2190b-113">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="2190b-114">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="2190b-115">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-115">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-116">WPD \_ 物件 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="2190b-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                                               | <span data-ttu-id="2190b-117">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-117">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-118">WPD \_ 物件 \_ 內容 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="2190b-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                                                  | <span data-ttu-id="2190b-119">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-119">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-120">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="2190b-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                                           | <span data-ttu-id="2190b-121">如果物件是隱藏的，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="2190b-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="2190b-122">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="2190b-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                                           | <span data-ttu-id="2190b-123">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="2190b-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="2190b-124">WPD \_ 物件 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2190b-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                                                   | <span data-ttu-id="2190b-125">如果物件至少有一個資源，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="2190b-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="2190b-126">WPD \_ 物件 \_ 原始檔案 \_ \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2190b-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                                                     | <span data-ttu-id="2190b-127">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="2190b-128">不可取用的 WPD \_ 物件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="2190b-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                                              | <span data-ttu-id="2190b-129">如果物件不打算供裝置取用，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="2190b-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="2190b-130">WPD \_ 物件 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="2190b-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                                       | <span data-ttu-id="2190b-131">如果物件具有其他物件的參考，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="2190b-132">WPD \_ 物件 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="2190b-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                                           | <span data-ttu-id="2190b-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-134">WPD \_ 物件 \_ 同步 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                                            | <span data-ttu-id="2190b-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-136">WPD \_ 物件 \_ 受到 \_ DRM \_ 保護</span><span class="sxs-lookup"><span data-stu-id="2190b-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                                         | <span data-ttu-id="2190b-137">如果物件受到 DRM 技術的保護，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="2190b-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="2190b-138">已 \_ 建立 WPD 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="2190b-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                                                  | <span data-ttu-id="2190b-139">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-140">修改的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="2190b-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                                                | <span data-ttu-id="2190b-141">建議使用。</span><span class="sxs-lookup"><span data-stu-id="2190b-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="2190b-142">撰寫的 WPD \_ 物件 \_ 日期 \_</span><span class="sxs-lookup"><span data-stu-id="2190b-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                                                | <span data-ttu-id="2190b-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-144">WPD \_ 物件 \_ 反向 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="2190b-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                                       | <span data-ttu-id="2190b-145">如果物件是由另一個物件參考，則建議使用。</span><span class="sxs-lookup"><span data-stu-id="2190b-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="2190b-146">WPD \_ 物件 \_ 容器 \_ 功能 \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)                            | <span data-ttu-id="2190b-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-148">WPD \_ 物件 \_ \_ \_ 從資源產生縮圖 \_</span><span class="sxs-lookup"><span data-stu-id="2190b-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md)                        | <span data-ttu-id="2190b-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-150">WPD \_ 物件 \_ 可以 \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="2190b-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                      | <span data-ttu-id="2190b-151">如果無法刪除物件，則為必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="2190b-152">WPD \_ 物件 \_ 語言 \_ 區域變數</span><span class="sxs-lookup"><span data-stu-id="2190b-152">WPD\_OBJECT\_LANGUAGE\_LOCAL</span></span>](object-properties.md)                                                                                        | <span data-ttu-id="2190b-153">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-153">Optional.</span></span>                                                             |
| [<span data-ttu-id="2190b-154">WPD \_ 網路 \_ 關聯 \_ 主機 \_ 網路 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="2190b-154">WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS</span></span>](network-association-properties.md) | <span data-ttu-id="2190b-155">必要。</span><span class="sxs-lookup"><span data-stu-id="2190b-155">Required.</span></span>                                                             |
| [<span data-ttu-id="2190b-156">WPD \_ 網路 \_ 關聯 \_ X509V3SEQUENCE</span><span class="sxs-lookup"><span data-stu-id="2190b-156">WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE</span></span>](network-association-properties.md)                       | <span data-ttu-id="2190b-157">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2190b-157">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="2190b-158">一般資源</span><span class="sxs-lookup"><span data-stu-id="2190b-158">Typical Resources</span></span>

<span data-ttu-id="2190b-159">這些物件通常不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="2190b-159">These objects typically do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2190b-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="2190b-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2190b-161">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="2190b-161">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



