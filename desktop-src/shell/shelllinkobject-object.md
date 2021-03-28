---
description: 管理 Shell 連結。 這個物件讓 IShellLink 介面的許多功能可供腳本應用程式使用。
title: 'ShellLinkObject 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973737"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="9f775-104">ShellLinkObject 物件</span><span class="sxs-lookup"><span data-stu-id="9f775-104">ShellLinkObject object</span></span>

<span data-ttu-id="9f775-105">管理 Shell 連結。</span><span class="sxs-lookup"><span data-stu-id="9f775-105">Manages Shell links.</span></span> <span data-ttu-id="9f775-106">這個物件讓 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面的許多功能可供腳本應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="9f775-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="9f775-107">成員</span><span class="sxs-lookup"><span data-stu-id="9f775-107">Members</span></span>

<span data-ttu-id="9f775-108">**ShellLinkObject** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f775-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="9f775-109">方法</span><span class="sxs-lookup"><span data-stu-id="9f775-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f775-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9f775-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f775-111">方法</span><span class="sxs-lookup"><span data-stu-id="9f775-111">Methods</span></span>

<span data-ttu-id="9f775-112">**ShellLinkObject** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9f775-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="9f775-113">方法</span><span class="sxs-lookup"><span data-stu-id="9f775-113">Method</span></span>                                                     | <span data-ttu-id="9f775-114">描述</span><span class="sxs-lookup"><span data-stu-id="9f775-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f775-115">**GetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="9f775-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="9f775-116">取得指派給連結的圖示位置。</span><span class="sxs-lookup"><span data-stu-id="9f775-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="9f775-117">**解決**</span><span class="sxs-lookup"><span data-stu-id="9f775-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="9f775-118">尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。</span><span class="sxs-lookup"><span data-stu-id="9f775-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="9f775-119">**儲存**</span><span class="sxs-lookup"><span data-stu-id="9f775-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="9f775-120">儲存連結的所有變更。</span><span class="sxs-lookup"><span data-stu-id="9f775-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="9f775-121">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="9f775-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="9f775-122">設定指派給連結的圖示位置。</span><span class="sxs-lookup"><span data-stu-id="9f775-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="9f775-123">屬性</span><span class="sxs-lookup"><span data-stu-id="9f775-123">Properties</span></span>

<span data-ttu-id="9f775-124">**ShellLinkObject** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9f775-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="9f775-125">屬性</span><span class="sxs-lookup"><span data-stu-id="9f775-125">Property</span></span>                                                                | <span data-ttu-id="9f775-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="9f775-126">Access type</span></span>           | <span data-ttu-id="9f775-127">Description</span><span class="sxs-lookup"><span data-stu-id="9f775-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f775-128">**引數**</span><span class="sxs-lookup"><span data-stu-id="9f775-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="9f775-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-129">Read/write</span></span><br/> | <span data-ttu-id="9f775-130">包含連結的引數。</span><span class="sxs-lookup"><span data-stu-id="9f775-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="9f775-131">**描述**</span><span class="sxs-lookup"><span data-stu-id="9f775-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="9f775-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-132">Read/write</span></span><br/> | <span data-ttu-id="9f775-133">取得或設定連結的描述。</span><span class="sxs-lookup"><span data-stu-id="9f775-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="9f775-134">**熱鍵**</span><span class="sxs-lookup"><span data-stu-id="9f775-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="9f775-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-135">Read/write</span></span><br/> | <span data-ttu-id="9f775-136">取得或設定連結的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="9f775-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="9f775-137">**路徑**</span><span class="sxs-lookup"><span data-stu-id="9f775-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="9f775-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-138">Read/write</span></span><br/> | <span data-ttu-id="9f775-139">取得或設定連結化物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="9f775-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="9f775-140">**ShowCommand**</span><span class="sxs-lookup"><span data-stu-id="9f775-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="9f775-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-141">Read/write</span></span><br/> | <span data-ttu-id="9f775-142">取得或設定連結命令的初始顯示狀態 (大小、最小化或最大化) 。</span><span class="sxs-lookup"><span data-stu-id="9f775-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="9f775-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="9f775-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="9f775-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9f775-144">Read/write</span></span><br/> | <span data-ttu-id="9f775-145">取得或設定連結中指定的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="9f775-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="9f775-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f775-146">Requirements</span></span>



| <span data-ttu-id="9f775-147">需求</span><span class="sxs-lookup"><span data-stu-id="9f775-147">Requirement</span></span> | <span data-ttu-id="9f775-148">值</span><span class="sxs-lookup"><span data-stu-id="9f775-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f775-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f775-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9f775-150">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f775-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f775-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f775-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9f775-152">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f775-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f775-153">標頭</span><span class="sxs-lookup"><span data-stu-id="9f775-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f775-154"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f775-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9f775-155">Idl</span><span class="sxs-lookup"><span data-stu-id="9f775-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f775-156"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f775-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9f775-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9f775-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f775-158"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9f775-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f775-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f775-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f775-160">Shell 連結</span><span class="sxs-lookup"><span data-stu-id="9f775-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
