---
description: Collection 類別
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319216"
---
# <a name="collection-object"></a><span data-ttu-id="b5d39-103">Collection 物件</span><span class="sxs-lookup"><span data-stu-id="b5d39-103">Collection object</span></span>

<span data-ttu-id="b5d39-104">Collection 類別</span><span class="sxs-lookup"><span data-stu-id="b5d39-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="b5d39-105">成員</span><span class="sxs-lookup"><span data-stu-id="b5d39-105">Members</span></span>

<span data-ttu-id="b5d39-106">**Collection** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5d39-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="b5d39-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b5d39-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5d39-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b5d39-108">Properties</span></span>

<span data-ttu-id="b5d39-109">**Collection** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b5d39-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="b5d39-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b5d39-110">Property</span></span>                                           | <span data-ttu-id="b5d39-111">存取類型</span><span class="sxs-lookup"><span data-stu-id="b5d39-111">Access type</span></span>          | <span data-ttu-id="b5d39-112">Description</span><span class="sxs-lookup"><span data-stu-id="b5d39-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="b5d39-113">**計數**</span><span class="sxs-lookup"><span data-stu-id="b5d39-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="b5d39-114">唯讀</span><span class="sxs-lookup"><span data-stu-id="b5d39-114">Read-only</span></span><br/> | <span data-ttu-id="b5d39-115">傳回集合中的成員數目。</span><span class="sxs-lookup"><span data-stu-id="b5d39-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="b5d39-116">**項目**</span><span class="sxs-lookup"><span data-stu-id="b5d39-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="b5d39-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="b5d39-117">Read-only</span></span><br/> | <span data-ttu-id="b5d39-118">傳回集合中的指定專案。</span><span class="sxs-lookup"><span data-stu-id="b5d39-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b5d39-119">備註</span><span class="sxs-lookup"><span data-stu-id="b5d39-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="b5d39-120">建立 \\ 存取函數</span><span class="sxs-lookup"><span data-stu-id="b5d39-120">Creation\\Access Functions</span></span>

<span data-ttu-id="b5d39-121">使用下列任何一項來取得物件的參考：</span><span class="sxs-lookup"><span data-stu-id="b5d39-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="b5d39-122">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="b5d39-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="b5d39-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="b5d39-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="b5d39-124">**設備**</span><span class="sxs-lookup"><span data-stu-id="b5d39-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="b5d39-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5d39-125">Requirements</span></span>



| <span data-ttu-id="b5d39-126">需求</span><span class="sxs-lookup"><span data-stu-id="b5d39-126">Requirement</span></span> | <span data-ttu-id="b5d39-127">值</span><span class="sxs-lookup"><span data-stu-id="b5d39-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d39-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5d39-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d39-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d39-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5d39-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5d39-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d39-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d39-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b5d39-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d39-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d39-133"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b5d39-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




