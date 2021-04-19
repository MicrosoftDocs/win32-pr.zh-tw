---
description: ICategory 介面會定義下列屬性。
ms.assetid: aa9c4dbb-5e33-47b7-ae6c-8d83010e205b
title: ICategory 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d01e5b5eac4701ebdff4c79981ee91806a18329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973489"
---
# <a name="icategory-properties"></a><span data-ttu-id="03139-103">ICategory 屬性</span><span class="sxs-lookup"><span data-stu-id="03139-103">ICategory Properties</span></span>

<span data-ttu-id="03139-104">[**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="03139-104">The [**ICategory**](/windows/desktop/api/Wuapi/nn-wuapi-icategory) interface defines the following properties.</span></span>



| <span data-ttu-id="03139-105">屬性</span><span class="sxs-lookup"><span data-stu-id="03139-105">Property</span></span>                                     | <span data-ttu-id="03139-106">描述</span><span class="sxs-lookup"><span data-stu-id="03139-106">Description</span></span>                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03139-107">**Id**</span><span class="sxs-lookup"><span data-stu-id="03139-107">**CategoryID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_categoryid)   | <span data-ttu-id="03139-108">取得類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03139-108">Gets the identifier of the category.</span></span>                                                              |
| [<span data-ttu-id="03139-109">**Children**</span><span class="sxs-lookup"><span data-stu-id="03139-109">**Children**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_children)       | <span data-ttu-id="03139-110">取得介面集合，其中包含這個類別目錄的子類別。</span><span class="sxs-lookup"><span data-stu-id="03139-110">Gets an interface collection that contains the child categories of this category.</span></span>                 |
| [<span data-ttu-id="03139-111">**描述**</span><span class="sxs-lookup"><span data-stu-id="03139-111">**Description**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_description) | <span data-ttu-id="03139-112">取得類別目錄的描述。</span><span class="sxs-lookup"><span data-stu-id="03139-112">Gets the description of the category.</span></span>                                                             |
| [<span data-ttu-id="03139-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="03139-113">**Image**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_image)             | <span data-ttu-id="03139-114">取得介面，其中包含與類別目錄相關聯之影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="03139-114">Gets an interface that contains information about the image that is associated with the category.</span></span> |
| [<span data-ttu-id="03139-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="03139-115">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_name)               | <span data-ttu-id="03139-116">取得分類的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="03139-116">Gets the localized name of the category.</span></span>                                                          |
| [<span data-ttu-id="03139-117">**單**</span><span class="sxs-lookup"><span data-stu-id="03139-117">**Order**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_order)             | <span data-ttu-id="03139-118">取得此分類在其同級類別之間的建議顯示順序。</span><span class="sxs-lookup"><span data-stu-id="03139-118">Gets the recommended display order of this category among its sibling categories.</span></span>                 |
| [<span data-ttu-id="03139-119">**父代**</span><span class="sxs-lookup"><span data-stu-id="03139-119">**Parent**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_parent)           | <span data-ttu-id="03139-120">取得介面，這個介面會描述這個類別目錄的父類別。</span><span class="sxs-lookup"><span data-stu-id="03139-120">Gets an interface that describes the parent category of this category.</span></span>                            |
| [<span data-ttu-id="03139-121">**類型**</span><span class="sxs-lookup"><span data-stu-id="03139-121">**Type**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_type)               | <span data-ttu-id="03139-122">取得分類的型別。</span><span class="sxs-lookup"><span data-stu-id="03139-122">Gets the type of the category.</span></span>                                                                    |
| [<span data-ttu-id="03139-123">**更新**</span><span class="sxs-lookup"><span data-stu-id="03139-123">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-icategory-get_updates)         | <span data-ttu-id="03139-124">取得介面，其中包含立即屬於分類的更新集合。</span><span class="sxs-lookup"><span data-stu-id="03139-124">Gets an interface that contains a collection of updates that immediately belong to the category.</span></span>  |



 

 

 



