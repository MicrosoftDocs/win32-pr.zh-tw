---
description: 這個專案的型別。 唯讀。
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000125"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="dee81-104">Item. ItemType 屬性</span><span class="sxs-lookup"><span data-stu-id="dee81-104">Item.ItemType property</span></span>

<span data-ttu-id="dee81-105">這個專案的型別。</span><span class="sxs-lookup"><span data-stu-id="dee81-105">The type of this item.</span></span> <span data-ttu-id="dee81-106">唯讀。</span><span class="sxs-lookup"><span data-stu-id="dee81-106">Read-only.</span></span>

<span data-ttu-id="dee81-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="dee81-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee81-108">語法</span><span class="sxs-lookup"><span data-stu-id="dee81-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="dee81-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="dee81-109">Property value</span></span>

<span data-ttu-id="dee81-110">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="dee81-110">The following values are possible:</span></span>



| <span data-ttu-id="dee81-111">值</span><span class="sxs-lookup"><span data-stu-id="dee81-111">Value</span></span>  | <span data-ttu-id="dee81-112">描述</span><span class="sxs-lookup"><span data-stu-id="dee81-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="dee81-113">裝置</span><span class="sxs-lookup"><span data-stu-id="dee81-113">device</span></span> | <span data-ttu-id="dee81-114">專案是 WIA 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="dee81-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="dee81-115">folder</span><span class="sxs-lookup"><span data-stu-id="dee81-115">folder</span></span> | <span data-ttu-id="dee81-116">專案是包含其他專案的資料夾。</span><span class="sxs-lookup"><span data-stu-id="dee81-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="dee81-117">file</span><span class="sxs-lookup"><span data-stu-id="dee81-117">file</span></span>   | <span data-ttu-id="dee81-118">此專案是影像或音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="dee81-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="dee81-119">音訊</span><span class="sxs-lookup"><span data-stu-id="dee81-119">audio</span></span>  | <span data-ttu-id="dee81-120">專案是音訊剪輯。</span><span class="sxs-lookup"><span data-stu-id="dee81-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="dee81-121">image</span><span class="sxs-lookup"><span data-stu-id="dee81-121">image</span></span>  | <span data-ttu-id="dee81-122">此專案為影像。</span><span class="sxs-lookup"><span data-stu-id="dee81-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="dee81-123">備註</span><span class="sxs-lookup"><span data-stu-id="dee81-123">Remarks</span></span>

<span data-ttu-id="dee81-124">一個專案可以有一個以上的類型。</span><span class="sxs-lookup"><span data-stu-id="dee81-124">An item can have more than one type.</span></span> <span data-ttu-id="dee81-125">例如，每個影像都是 "image" 和 "file" 類型。</span><span class="sxs-lookup"><span data-stu-id="dee81-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="dee81-126">**ItemType** 會傳回字串，其中包含專案的所有有效類型（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="dee81-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="dee81-127">例如，"image; file"。</span><span class="sxs-lookup"><span data-stu-id="dee81-127">For example, "image;file".</span></span> <span data-ttu-id="dee81-128">這個字串中沒有空格，結尾沒有分號。</span><span class="sxs-lookup"><span data-stu-id="dee81-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee81-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="dee81-129">Requirements</span></span>



| <span data-ttu-id="dee81-130">需求</span><span class="sxs-lookup"><span data-stu-id="dee81-130">Requirement</span></span> | <span data-ttu-id="dee81-131">值</span><span class="sxs-lookup"><span data-stu-id="dee81-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee81-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dee81-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dee81-133">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee81-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dee81-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dee81-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dee81-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee81-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dee81-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dee81-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee81-137"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="dee81-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




