---
description: 表示 Shell 資料夾。 此物件包含屬性和方法，可讓您取得資料夾的相關資訊。
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: '資料夾物件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510784"
---
# <a name="folder-object"></a><span data-ttu-id="1780e-104">Folder 物件</span><span class="sxs-lookup"><span data-stu-id="1780e-104">Folder object</span></span>

<span data-ttu-id="1780e-105">表示 Shell 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1780e-105">Represents a Shell folder.</span></span> <span data-ttu-id="1780e-106">此物件包含屬性和方法，可讓您取得資料夾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1780e-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="1780e-107">成員</span><span class="sxs-lookup"><span data-stu-id="1780e-107">Members</span></span>

<span data-ttu-id="1780e-108">**資料夾** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1780e-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="1780e-109">方法</span><span class="sxs-lookup"><span data-stu-id="1780e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1780e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1780e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1780e-111">方法</span><span class="sxs-lookup"><span data-stu-id="1780e-111">Methods</span></span>

<span data-ttu-id="1780e-112">**資料夾** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1780e-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="1780e-113">方法</span><span class="sxs-lookup"><span data-stu-id="1780e-113">Method</span></span>                                      | <span data-ttu-id="1780e-114">描述</span><span class="sxs-lookup"><span data-stu-id="1780e-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1780e-115">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="1780e-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="1780e-116">將專案或專案複製到資料夾。</span><span class="sxs-lookup"><span data-stu-id="1780e-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="1780e-117">**GetDetailsOf**</span><span class="sxs-lookup"><span data-stu-id="1780e-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="1780e-118">抓取資料夾中專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1780e-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="1780e-119">例如，其大小、類型或上次修改的時間。</span><span class="sxs-lookup"><span data-stu-id="1780e-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="1780e-120">**項目**</span><span class="sxs-lookup"><span data-stu-id="1780e-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="1780e-121">抓取 [**FolderItems**](folderitems.md) 物件，該物件表示資料夾中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="1780e-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="1780e-122">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="1780e-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="1780e-123">將專案或專案移至此資料夾。</span><span class="sxs-lookup"><span data-stu-id="1780e-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="1780e-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="1780e-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="1780e-125">建立新的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1780e-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="1780e-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="1780e-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="1780e-127">建立並傳回 [**FolderItem**](folderitem.md) 物件，該物件表示指定的專案。</span><span class="sxs-lookup"><span data-stu-id="1780e-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="1780e-128">屬性</span><span class="sxs-lookup"><span data-stu-id="1780e-128">Properties</span></span>

<span data-ttu-id="1780e-129">**資料夾** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1780e-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="1780e-130">屬性</span><span class="sxs-lookup"><span data-stu-id="1780e-130">Property</span></span>                                               | <span data-ttu-id="1780e-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="1780e-131">Access type</span></span>          | <span data-ttu-id="1780e-132">Description</span><span class="sxs-lookup"><span data-stu-id="1780e-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="1780e-133">**Application**</span><span class="sxs-lookup"><span data-stu-id="1780e-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="1780e-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="1780e-134">Read-only</span></span><br/> | <span data-ttu-id="1780e-135">包含資料夾的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="1780e-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="1780e-136">**父代**</span><span class="sxs-lookup"><span data-stu-id="1780e-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="1780e-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="1780e-137">Read-only</span></span><br/> | <span data-ttu-id="1780e-138">未實作。</span><span class="sxs-lookup"><span data-stu-id="1780e-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="1780e-139">**ParentFolder**</span><span class="sxs-lookup"><span data-stu-id="1780e-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="1780e-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="1780e-140">Read-only</span></span><br/> | <span data-ttu-id="1780e-141">包含父 **資料夾** 物件。</span><span class="sxs-lookup"><span data-stu-id="1780e-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="1780e-142">**標題**</span><span class="sxs-lookup"><span data-stu-id="1780e-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="1780e-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="1780e-143">Read-only</span></span><br/> | <span data-ttu-id="1780e-144">包含資料夾的標題。</span><span class="sxs-lookup"><span data-stu-id="1780e-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1780e-145">備註</span><span class="sxs-lookup"><span data-stu-id="1780e-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1780e-146">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="1780e-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="1780e-147">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="1780e-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="1780e-148">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="1780e-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1780e-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="1780e-149">Requirements</span></span>



| <span data-ttu-id="1780e-150">需求</span><span class="sxs-lookup"><span data-stu-id="1780e-150">Requirement</span></span> | <span data-ttu-id="1780e-151">值</span><span class="sxs-lookup"><span data-stu-id="1780e-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1780e-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1780e-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1780e-153">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1780e-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="1780e-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1780e-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1780e-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1780e-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1780e-156">標頭</span><span class="sxs-lookup"><span data-stu-id="1780e-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="1780e-157"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1780e-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1780e-158">Idl</span><span class="sxs-lookup"><span data-stu-id="1780e-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1780e-159"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1780e-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




