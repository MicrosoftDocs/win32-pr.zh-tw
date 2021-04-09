---
description: WPD \_ 內容 \_ 類型 \_ 服務
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944899"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="fe8d5-103">WPD \_ 內容 \_ 類型 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="fe8d5-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="fe8d5-104">將其型別描述為 WPD \_ 內容 \_ 類型服務的物件 \_ 代表裝置服務。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="fe8d5-105">這種類型的物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="fe8d5-106">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="fe8d5-106">Property Name</span></span>                                                                                        | <span data-ttu-id="fe8d5-107">必要或選擇性</span><span class="sxs-lookup"><span data-stu-id="fe8d5-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="fe8d5-108">WPD \_ 物件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="fe8d5-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="fe8d5-109">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-109">Required, read-only.</span></span> <span data-ttu-id="fe8d5-110">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="fe8d5-111">WPD \_ 物件 \_ 父 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="fe8d5-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="fe8d5-112">必要。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="fe8d5-113">WPD \_ 物件 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="fe8d5-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="fe8d5-114">如果物件代表檔案，則為必要。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="fe8d5-115">WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="fe8d5-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="fe8d5-116">必要、唯讀。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-116">Required, read-only.</span></span> <span data-ttu-id="fe8d5-117">即使在建立時，用戶端也無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="fe8d5-118">WPD \_ 物件 \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="fe8d5-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="fe8d5-119">如果不應該對使用者顯示服務，則為必要。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="fe8d5-120">WPD \_ 物件 \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="fe8d5-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="fe8d5-121">如果物件為系統物件，則為必要項， (代表) 的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="fe8d5-122">WPD \_ 功能 \_ 物件 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="fe8d5-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="fe8d5-123">必要。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-123">Required.</span></span> <span data-ttu-id="fe8d5-124">這代表裝置服務類型。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="fe8d5-125">WPD \_ 服務 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="fe8d5-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="fe8d5-126">必要。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="fe8d5-127">WPD \_ 儲存體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="fe8d5-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="fe8d5-128">如果服務用來儲存物件，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="fe8d5-129">WPD \_ 儲存體 \_ 容量</span><span class="sxs-lookup"><span data-stu-id="fe8d5-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="fe8d5-130">如果服務用來儲存物件，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="fe8d5-131">一般資源</span><span class="sxs-lookup"><span data-stu-id="fe8d5-131">Typical Resources</span></span>

<span data-ttu-id="fe8d5-132">這些物件不會裝載資源。</span><span class="sxs-lookup"><span data-stu-id="fe8d5-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe8d5-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe8d5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe8d5-134">**物件的需求**</span><span class="sxs-lookup"><span data-stu-id="fe8d5-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



