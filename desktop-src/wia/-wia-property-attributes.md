---
description: 所有專案物件都有屬性。
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: " (WIA) 的屬性屬性"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469116"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="c7360-103"> (WIA) 的屬性屬性</span><span class="sxs-lookup"><span data-stu-id="c7360-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="c7360-104">所有專案物件都有屬性。</span><span class="sxs-lookup"><span data-stu-id="c7360-104">All item objects have properties.</span></span> <span data-ttu-id="c7360-105">屬性有屬性。</span><span class="sxs-lookup"><span data-stu-id="c7360-105">The properties have attributes.</span></span> <span data-ttu-id="c7360-106">例如，屬性屬性會指出屬性是讀取、寫入或刪除。</span><span class="sxs-lookup"><span data-stu-id="c7360-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="c7360-107">它們也會指出有效的屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7360-107">They also indicate the valid property values.</span></span> <span data-ttu-id="c7360-108">下列常數是有效的屬性屬性：</span><span class="sxs-lookup"><span data-stu-id="c7360-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="c7360-109">Property 屬性</span><span class="sxs-lookup"><span data-stu-id="c7360-109">Property Attribute</span></span>        | <span data-ttu-id="c7360-110">意義</span><span class="sxs-lookup"><span data-stu-id="c7360-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7360-111">WIA 的可快取 \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7360-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="c7360-112">裝置可以快取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c7360-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="c7360-113">WIA 的 [ \_ \_ 識別碼]</span><span class="sxs-lookup"><span data-stu-id="c7360-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="c7360-114">屬性具有合法旗標值的清單。</span><span class="sxs-lookup"><span data-stu-id="c7360-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="c7360-115">旗標值會使用位 **or** 運算來合併。</span><span class="sxs-lookup"><span data-stu-id="c7360-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="c7360-116">WIA \_ 的 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="c7360-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="c7360-117">屬性具有合法值的清單。</span><span class="sxs-lookup"><span data-stu-id="c7360-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="c7360-118">WIA \_ \_ 內容無</span><span class="sxs-lookup"><span data-stu-id="c7360-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="c7360-119">屬性沒有任何與其相關聯的有效值。</span><span class="sxs-lookup"><span data-stu-id="c7360-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="c7360-120">WIA \_ 的 \_ 範圍</span><span class="sxs-lookup"><span data-stu-id="c7360-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="c7360-121">屬性具有有效值的範圍。</span><span class="sxs-lookup"><span data-stu-id="c7360-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="c7360-122">已 \_ 讀取的 WIA \_</span><span class="sxs-lookup"><span data-stu-id="c7360-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="c7360-123">應用程式可以讀取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c7360-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="c7360-124">WIA \_ 和 \_ RW</span><span class="sxs-lookup"><span data-stu-id="c7360-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="c7360-125">應用程式可以讀取和寫入屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c7360-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="c7360-126">需要 WIA 參數 \_ \_ 同步 \_</span><span class="sxs-lookup"><span data-stu-id="c7360-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="c7360-127">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="c7360-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="c7360-128">WIA \_ \_ 目錄寫入</span><span class="sxs-lookup"><span data-stu-id="c7360-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="c7360-129">應用程式可以寫入屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c7360-129">The application can write the property's value.</span></span>                                                          |



 

 

 



