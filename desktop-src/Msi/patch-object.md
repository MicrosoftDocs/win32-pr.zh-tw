---
description: Patch 物件代表已註冊或套用之修補程式的唯一實例。您可以使用 Patch 屬性將物件具現化為 &\# 0034;WindowsInstaller： Patch (PatchCode、ProductCode、UserSid、CoNtext) &\# 0034;。
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991547"
---
# <a name="patch-object"></a><span data-ttu-id="a8de7-103">Patch 物件</span><span class="sxs-lookup"><span data-stu-id="a8de7-103">Patch object</span></span>

<span data-ttu-id="a8de7-104">**Patch** 物件代表已註冊或套用之修補程式的唯一實例。</span><span class="sxs-lookup"><span data-stu-id="a8de7-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="a8de7-105">您可以使用 Patch 屬性將此物件具 **現** 化為 "WindowsInstaller"， (*PatchCode*、 *ProductCode*、 *UserSid*、 *CoNtext*) "。</span><span class="sxs-lookup"><span data-stu-id="a8de7-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="a8de7-106">若為電腦內容， *UserSid* 參數必須是空字串。</span><span class="sxs-lookup"><span data-stu-id="a8de7-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="a8de7-107">您可以針對只註冊但尚未套用至任何產品的修補程式，將 *ProductCode* 設定為空字串。</span><span class="sxs-lookup"><span data-stu-id="a8de7-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="a8de7-108">只有在讀取或更新修補程式的來源清單資訊時，才能將 *ProductCode* 設定為空字串。</span><span class="sxs-lookup"><span data-stu-id="a8de7-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="a8de7-109">成員</span><span class="sxs-lookup"><span data-stu-id="a8de7-109">Members</span></span>

<span data-ttu-id="a8de7-110">**Patch** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a8de7-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="a8de7-111">方法</span><span class="sxs-lookup"><span data-stu-id="a8de7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a8de7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a8de7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a8de7-113">方法</span><span class="sxs-lookup"><span data-stu-id="a8de7-113">Methods</span></span>

<span data-ttu-id="a8de7-114">**Patch** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a8de7-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="a8de7-115">方法</span><span class="sxs-lookup"><span data-stu-id="a8de7-115">Method</span></span>                                                               | <span data-ttu-id="a8de7-116">描述</span><span class="sxs-lookup"><span data-stu-id="a8de7-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8de7-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="a8de7-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="a8de7-118">將磁片新增至已註冊的磁片集。</span><span class="sxs-lookup"><span data-stu-id="a8de7-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a8de7-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="a8de7-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="a8de7-120">將網路或 URL 來源新增至來源清單。</span><span class="sxs-lookup"><span data-stu-id="a8de7-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="a8de7-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="a8de7-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="a8de7-122">清除指定類型來源的完整來源清單。</span><span class="sxs-lookup"><span data-stu-id="a8de7-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="a8de7-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="a8de7-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="a8de7-124">從來源清單中移除已註冊磁片集的磁片。</span><span class="sxs-lookup"><span data-stu-id="a8de7-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="a8de7-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="a8de7-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="a8de7-126">從來源清單中移除網路或 URL 來源。</span><span class="sxs-lookup"><span data-stu-id="a8de7-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="a8de7-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="a8de7-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="a8de7-128">清除來源清單中上次使用的來源。</span><span class="sxs-lookup"><span data-stu-id="a8de7-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="a8de7-129">這會在下一次需要來源時強制來源清單解析。</span><span class="sxs-lookup"><span data-stu-id="a8de7-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a8de7-130">屬性</span><span class="sxs-lookup"><span data-stu-id="a8de7-130">Properties</span></span>

<span data-ttu-id="a8de7-131">**Patch** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8de7-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="a8de7-132">屬性</span><span class="sxs-lookup"><span data-stu-id="a8de7-132">Property</span></span>                                                  | <span data-ttu-id="a8de7-133">描述</span><span class="sxs-lookup"><span data-stu-id="a8de7-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8de7-134">**Context**</span><span class="sxs-lookup"><span data-stu-id="a8de7-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="a8de7-135">此修補程式實例的內容是 MSIINSTALLCONTEXT 值。</span><span class="sxs-lookup"><span data-stu-id="a8de7-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="a8de7-136">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="a8de7-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="a8de7-137">列舉此 patch 實例的所有媒體磁片。</span><span class="sxs-lookup"><span data-stu-id="a8de7-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="a8de7-138">**PatchCode**</span><span class="sxs-lookup"><span data-stu-id="a8de7-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="a8de7-139">傳回修補程式碼。</span><span class="sxs-lookup"><span data-stu-id="a8de7-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="a8de7-140">**PatchProperty**</span><span class="sxs-lookup"><span data-stu-id="a8de7-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="a8de7-141">取得套用至特定產品實例之特定 patch 的相關屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="a8de7-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="a8de7-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="a8de7-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="a8de7-143">傳回產品代碼。</span><span class="sxs-lookup"><span data-stu-id="a8de7-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="a8de7-144">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="a8de7-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="a8de7-145">取得和設定來源資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="a8de7-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="a8de7-146">這是讀取或寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="a8de7-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="a8de7-147">**來源**</span><span class="sxs-lookup"><span data-stu-id="a8de7-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="a8de7-148">列舉此 patch 實例的所有來源。</span><span class="sxs-lookup"><span data-stu-id="a8de7-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="a8de7-149">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a8de7-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="a8de7-150">修補程式的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="a8de7-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="a8de7-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="a8de7-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="a8de7-152">傳回此 patch 實例可用之帳戶下的使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="a8de7-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="a8de7-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8de7-153">Requirements</span></span>



| <span data-ttu-id="a8de7-154">需求</span><span class="sxs-lookup"><span data-stu-id="a8de7-154">Requirement</span></span> | <span data-ttu-id="a8de7-155">值</span><span class="sxs-lookup"><span data-stu-id="a8de7-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8de7-156">版本</span><span class="sxs-lookup"><span data-stu-id="a8de7-156">Version</span></span><br/> | <span data-ttu-id="a8de7-157">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="a8de7-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8de7-158">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="a8de7-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8de7-159">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a8de7-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a8de7-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a8de7-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8de7-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8de7-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a8de7-162">IID</span><span class="sxs-lookup"><span data-stu-id="a8de7-162">IID</span></span><br/>     | <span data-ttu-id="a8de7-163">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a8de7-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a8de7-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8de7-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8de7-165">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="a8de7-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




