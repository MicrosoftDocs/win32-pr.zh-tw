---
description: 表示 Shell 資料夾中的專案集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。
title: 'FolderItems 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840649"
---
# <a name="folderitems-object"></a><span data-ttu-id="7b5c7-104">FolderItems 物件</span><span class="sxs-lookup"><span data-stu-id="7b5c7-104">FolderItems object</span></span>

<span data-ttu-id="7b5c7-105">表示 Shell 資料夾中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="7b5c7-106">此物件包含屬性和方法，可讓您取得集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="7b5c7-107">成員</span><span class="sxs-lookup"><span data-stu-id="7b5c7-107">Members</span></span>

<span data-ttu-id="7b5c7-108">**FolderItems** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7b5c7-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="7b5c7-109">方法</span><span class="sxs-lookup"><span data-stu-id="7b5c7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b5c7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7b5c7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b5c7-111">方法</span><span class="sxs-lookup"><span data-stu-id="7b5c7-111">Methods</span></span>

<span data-ttu-id="7b5c7-112">**FolderItems** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="7b5c7-113">方法</span><span class="sxs-lookup"><span data-stu-id="7b5c7-113">Method</span></span>                                    | <span data-ttu-id="7b5c7-114">描述</span><span class="sxs-lookup"><span data-stu-id="7b5c7-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b5c7-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="7b5c7-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="7b5c7-116">未實作。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="7b5c7-117">**項目**</span><span class="sxs-lookup"><span data-stu-id="7b5c7-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="7b5c7-118">抓取集合中指定之專案的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7b5c7-119">屬性</span><span class="sxs-lookup"><span data-stu-id="7b5c7-119">Properties</span></span>

<span data-ttu-id="7b5c7-120">**FolderItems** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="7b5c7-121">屬性</span><span class="sxs-lookup"><span data-stu-id="7b5c7-121">Property</span></span>                                                  | <span data-ttu-id="7b5c7-122">存取類型</span><span class="sxs-lookup"><span data-stu-id="7b5c7-122">Access type</span></span>          | <span data-ttu-id="7b5c7-123">描述</span><span class="sxs-lookup"><span data-stu-id="7b5c7-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b5c7-124">**Application**</span><span class="sxs-lookup"><span data-stu-id="7b5c7-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="7b5c7-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="7b5c7-125">Read-only</span></span><br/> | <span data-ttu-id="7b5c7-126">包含資料夾專案集合的 [**應用程式**](folderitems-application.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="7b5c7-127">**計數**</span><span class="sxs-lookup"><span data-stu-id="7b5c7-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="7b5c7-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="7b5c7-128">Read-only</span></span><br/> | <span data-ttu-id="7b5c7-129">包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="7b5c7-130">**父代**</span><span class="sxs-lookup"><span data-stu-id="7b5c7-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="7b5c7-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="7b5c7-131">Read-only</span></span><br/> | <span data-ttu-id="7b5c7-132">未實作。</span><span class="sxs-lookup"><span data-stu-id="7b5c7-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="7b5c7-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b5c7-133">Requirements</span></span>



| <span data-ttu-id="7b5c7-134">需求</span><span class="sxs-lookup"><span data-stu-id="7b5c7-134">Requirement</span></span> | <span data-ttu-id="7b5c7-135">值</span><span class="sxs-lookup"><span data-stu-id="7b5c7-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5c7-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b5c7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5c7-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b5c7-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7b5c7-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b5c7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5c7-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b5c7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b5c7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7b5c7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b5c7-141"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b5c7-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7b5c7-142">Idl</span><span class="sxs-lookup"><span data-stu-id="7b5c7-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b5c7-143"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b5c7-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7b5c7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5c7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b5c7-145"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7b5c7-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




