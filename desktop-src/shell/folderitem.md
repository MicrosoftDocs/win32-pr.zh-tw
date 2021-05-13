---
description: 表示 Shell 資料夾中的專案。 此物件包含屬性和方法，可讓您取得專案的相關資訊。
title: 'FolderItem 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840979"
---
# <a name="folderitem-object"></a><span data-ttu-id="d1b08-104">FolderItem 物件</span><span class="sxs-lookup"><span data-stu-id="d1b08-104">FolderItem object</span></span>

<span data-ttu-id="d1b08-105">表示 Shell 資料夾中的專案。</span><span class="sxs-lookup"><span data-stu-id="d1b08-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="d1b08-106">此物件包含屬性和方法，可讓您取得專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1b08-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="d1b08-107">成員</span><span class="sxs-lookup"><span data-stu-id="d1b08-107">Members</span></span>

<span data-ttu-id="d1b08-108">**FolderItem** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d1b08-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="d1b08-109">方法</span><span class="sxs-lookup"><span data-stu-id="d1b08-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1b08-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d1b08-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1b08-111">方法</span><span class="sxs-lookup"><span data-stu-id="d1b08-111">Methods</span></span>

<span data-ttu-id="d1b08-112">**FolderItem** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d1b08-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="d1b08-113">方法</span><span class="sxs-lookup"><span data-stu-id="d1b08-113">Method</span></span>                                      | <span data-ttu-id="d1b08-114">描述</span><span class="sxs-lookup"><span data-stu-id="d1b08-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b08-115">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="d1b08-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="d1b08-116">在專案上執行動詞。</span><span class="sxs-lookup"><span data-stu-id="d1b08-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="d1b08-117">**動詞**</span><span class="sxs-lookup"><span data-stu-id="d1b08-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="d1b08-118">抓取專案的 [**FolderItemVerbs**](folderitemverbs.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d1b08-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="d1b08-119">此物件是可以在專案上執行的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="d1b08-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d1b08-120">屬性</span><span class="sxs-lookup"><span data-stu-id="d1b08-120">Properties</span></span>

<span data-ttu-id="d1b08-121">**FolderItem** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d1b08-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="d1b08-122">屬性</span><span class="sxs-lookup"><span data-stu-id="d1b08-122">Property</span></span>                                                   | <span data-ttu-id="d1b08-123">存取類型</span><span class="sxs-lookup"><span data-stu-id="d1b08-123">Access type</span></span>           | <span data-ttu-id="d1b08-124">描述</span><span class="sxs-lookup"><span data-stu-id="d1b08-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1b08-125">**Application**</span><span class="sxs-lookup"><span data-stu-id="d1b08-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="d1b08-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-126">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-127">包含資料夾專案的 [**應用程式**](folderitem-application.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d1b08-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="d1b08-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="d1b08-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="d1b08-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-129">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-130">如果專案是資料夾，則包含專案的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d1b08-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="d1b08-131">**GetLink**</span><span class="sxs-lookup"><span data-stu-id="d1b08-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="d1b08-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-132">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-133">如果專案是快捷方式，則包含專案的 [**ShellLinkObject**](shelllinkobject-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d1b08-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="d1b08-134">**IsBrowsable**</span><span class="sxs-lookup"><span data-stu-id="d1b08-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="d1b08-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-135">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-136">指出專案是否可裝載于瀏覽器或 Windows 檔案總管框架內。</span><span class="sxs-lookup"><span data-stu-id="d1b08-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="d1b08-137">**IsFileSystem**</span><span class="sxs-lookup"><span data-stu-id="d1b08-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="d1b08-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-138">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-139">指出專案是否為檔案系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1b08-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="d1b08-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="d1b08-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="d1b08-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-141">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-142">指出專案是否為資料夾。</span><span class="sxs-lookup"><span data-stu-id="d1b08-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="d1b08-143">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="d1b08-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="d1b08-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-144">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-145">指出專案是否為快捷方式。</span><span class="sxs-lookup"><span data-stu-id="d1b08-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="d1b08-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="d1b08-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="d1b08-147">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1b08-147">Read/write</span></span><br/> | <span data-ttu-id="d1b08-148">設定或取得上次修改檔案的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d1b08-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="d1b08-149">[**ModifyDate**](folderitem-modifydate.md) 可以用來取得上次修改資料夾的日期和時間，但無法加以設定。</span><span class="sxs-lookup"><span data-stu-id="d1b08-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="d1b08-150">name - \*\*</span><span class="sxs-lookup"><span data-stu-id="d1b08-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="d1b08-151">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1b08-151">Read/write</span></span><br/> | <span data-ttu-id="d1b08-152">設定或取得專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b08-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="d1b08-153">**父代**</span><span class="sxs-lookup"><span data-stu-id="d1b08-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="d1b08-154">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-154">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-155">取得物件，該物件表示專案的父系。</span><span class="sxs-lookup"><span data-stu-id="d1b08-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="d1b08-156">**路徑**</span><span class="sxs-lookup"><span data-stu-id="d1b08-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="d1b08-157">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-157">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-158">包含專案的完整路徑和名稱。</span><span class="sxs-lookup"><span data-stu-id="d1b08-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="d1b08-159">**大小**</span><span class="sxs-lookup"><span data-stu-id="d1b08-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="d1b08-160">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-160">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-161">包含專案的大小。</span><span class="sxs-lookup"><span data-stu-id="d1b08-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="d1b08-162">**類型**</span><span class="sxs-lookup"><span data-stu-id="d1b08-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="d1b08-163">唯讀</span><span class="sxs-lookup"><span data-stu-id="d1b08-163">Read-only</span></span><br/>  | <span data-ttu-id="d1b08-164">包含專案類型的字串表示。</span><span class="sxs-lookup"><span data-stu-id="d1b08-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="d1b08-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1b08-165">Requirements</span></span>



| <span data-ttu-id="d1b08-166">需求</span><span class="sxs-lookup"><span data-stu-id="d1b08-166">Requirement</span></span> | <span data-ttu-id="d1b08-167">值</span><span class="sxs-lookup"><span data-stu-id="d1b08-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b08-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1b08-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b08-169">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1b08-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d1b08-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1b08-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b08-171">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1b08-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1b08-172">標頭</span><span class="sxs-lookup"><span data-stu-id="d1b08-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b08-173"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b08-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d1b08-174">Idl</span><span class="sxs-lookup"><span data-stu-id="d1b08-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1b08-175"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1b08-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d1b08-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b08-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b08-177"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d1b08-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




