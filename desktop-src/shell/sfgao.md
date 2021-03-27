---
description: 可以在專案 (檔案或資料夾) 或一組專案上抓取的屬性。
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: 'SFGAO (Shobjidl.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f01691c3dbb1e5b76d93739b4893ffaf7c69e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693791"
---
# <a name="sfgao"></a><span data-ttu-id="afdd4-103">SFGAO</span><span class="sxs-lookup"><span data-stu-id="afdd4-103">SFGAO</span></span>

<span data-ttu-id="afdd4-104">可以在專案 (檔案或資料夾) 或一組專案上抓取的屬性。</span><span class="sxs-lookup"><span data-stu-id="afdd4-104">Attributes that can be retrieved on an item (file or folder) or set of items.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="afdd4-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="afdd4-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="afdd4-106">Description</span><span class="sxs-lookup"><span data-stu-id="afdd4-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl> <span data-ttu-id="afdd4-107"><dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-107"><dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-108">您可以複製指定的專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-108">The specified items can be copied.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl> <span data-ttu-id="afdd4-109"><dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-109"><dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-110">您可以移動指定的專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-110">The specified items can be moved.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl> <span data-ttu-id="afdd4-111"><dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-111"><dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-112">您可以為指定的專案建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="afdd4-112">Shortcuts can be created for the specified items.</span></span> <span data-ttu-id="afdd4-113">這個屬性與 <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>的值相同。</span><span class="sxs-lookup"><span data-stu-id="afdd4-113">This attribute has the same value as <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>.</span></span> <br/> <span data-ttu-id="afdd4-114">如果命名空間延伸模組傳回這個屬性，則會在拖放作業期間，將具有預設處理常式的 <strong>建立快捷方式</strong> 專案加入至顯示的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="afdd4-114">If a namespace extension returns this attribute, a <strong>Create Shortcut</strong> entry with a default handler is added to the shortcut menu that is displayed during drag-and-drop operations.</span></span> <span data-ttu-id="afdd4-115">延伸模組也可以針對 <em>連結</em> 動詞來執行自己的處理常式，以取代預設值。</span><span class="sxs-lookup"><span data-stu-id="afdd4-115">The extension can also implement its own handler for the <em>link</em> verb in place of the default.</span></span> <span data-ttu-id="afdd4-116">如果延伸模組這麼做，它會負責建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="afdd4-116">If the extension does so, it is responsible for creating the shortcut.</span></span><br/> <span data-ttu-id="afdd4-117">[ <strong>建立快捷方式</strong> ] 專案也會加入至 <strong>[Windows 檔案總管檔案</strong> ] 功能表和一般快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="afdd4-117">A <strong>Create Shortcut</strong> item is also added to the Windows Explorer <strong>File</strong> menu and to normal shortcut menus.</span></span><br/> <span data-ttu-id="afdd4-118">如果選取專案，則會叫用應用程式的<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>ICoNtextMenu：： InvokeCommand</strong></a>方法，並將<a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a>結構的<strong>lpVerb</strong>成員設為<em>連結</em>。</span><span class="sxs-lookup"><span data-stu-id="afdd4-118">If the item is selected, your application's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> method is invoked with the <strong>lpVerb</strong> member of the <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> structure set to <em>link</em>.</span></span> <span data-ttu-id="afdd4-119">您的應用程式會負責建立連結。</span><span class="sxs-lookup"><span data-stu-id="afdd4-119">Your application is responsible for creating the link.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl> <span data-ttu-id="afdd4-120"><dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-120"><dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-121">指定的專案可以透過<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a>系結至<a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>物件。</span><span class="sxs-lookup"><span data-stu-id="afdd4-121">The specified items can be bound to an <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a> object through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>.</span></span> <span data-ttu-id="afdd4-122">如需命名空間操作功能的詳細資訊，請參閱 <strong>IStorage</strong>。</span><span class="sxs-lookup"><span data-stu-id="afdd4-122">For more information about namespace manipulation capabilities, see <strong>IStorage</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl> <span data-ttu-id="afdd4-123"><dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-123"><dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-124">您可以重新命名指定的專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-124">The specified items can be renamed.</span></span> <span data-ttu-id="afdd4-125">請注意，此值基本上是建議事項;並非所有命名空間用戶端都允許重新命名專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-125">Note that this value is essentially a suggestion; not all namespace clients allow items to be renamed.</span></span> <span data-ttu-id="afdd4-126">但是，必須設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="afdd4-126">However, those that do must have this attribute set.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl> <span data-ttu-id="afdd4-127"><dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-127"><dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-128">可以刪除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-128">The specified items can be deleted.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl> <span data-ttu-id="afdd4-129"><dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-129"><dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-130">指定的專案具有屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="afdd4-130">The specified items have property sheets.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl> <span data-ttu-id="afdd4-131"><dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-131"><dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-132">指定的專案是放置目標。</span><span class="sxs-lookup"><span data-stu-id="afdd4-132">The specified items are drop targets.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl> <span data-ttu-id="afdd4-133"><dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-133"><dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-134">此旗標是功能屬性的遮罩： SFGAO_CANCOPY、SFGAO_CANMOVE、SFGAO_CANLINK、SFGAO_CANRENAME、SFGAO_CANDELETE、SFGAO_HASPROPSHEET 和 SFGAO_DROPTARGET。</span><span class="sxs-lookup"><span data-stu-id="afdd4-134">This flag is a mask for the capability attributes: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET, and SFGAO_DROPTARGET.</span></span> <span data-ttu-id="afdd4-135">呼叫端通常不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="afdd4-135">Callers normally do not use this value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl> <span data-ttu-id="afdd4-136"><dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-136"><dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-137"><strong>Windows 7 和更新版本</strong>。</span><span class="sxs-lookup"><span data-stu-id="afdd4-137"><strong>Windows 7 and later</strong>.</span></span> <span data-ttu-id="afdd4-138">指定的專案為系統專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-138">The specified items are system items.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl> <span data-ttu-id="afdd4-139"><dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-139"><dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-140">指定的專案會加密，而且可能需要特殊的簡報。</span><span class="sxs-lookup"><span data-stu-id="afdd4-140">The specified items are encrypted and might require special presentation.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl> <span data-ttu-id="afdd4-141"><dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-141"><dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-142">透過 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> 或其他儲存體介面存取 (的專案，) 預期會是很慢的作業。</span><span class="sxs-lookup"><span data-stu-id="afdd4-142">Accessing the item (through <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> or other storage interfaces) is expected to be a slow operation.</span></span> <span data-ttu-id="afdd4-143">應用程式應該避免存取以 SFGAO_ISSLOW 標記的專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-143">Applications should avoid accessing items flagged with SFGAO_ISSLOW.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="afdd4-144">開啟專案的資料流程通常是緩慢的作業。</span><span class="sxs-lookup"><span data-stu-id="afdd4-144">Opening a stream for an item is generally a slow operation at all times.</span></span> <span data-ttu-id="afdd4-145">SFGAO_ISSLOW 指出預期的速度特別慢，例如，當網路連線緩慢或離線 (FILE_ATTRIBUTE_OFFLINE) 檔時。</span><span class="sxs-lookup"><span data-stu-id="afdd4-145">SFGAO_ISSLOW indicates that it is expected to be especially slow, for example in the case of slow network connections or offline (FILE_ATTRIBUTE_OFFLINE) files.</span></span> <span data-ttu-id="afdd4-146">不過，查詢 SFGAO_ISSLOW 本身是一項緩慢的操作。</span><span class="sxs-lookup"><span data-stu-id="afdd4-146">However, querying SFGAO_ISSLOW is itself a slow operation.</span></span> <span data-ttu-id="afdd4-147">應用程式應該只在背景執行緒上查詢 SFGAO_ISSLOW。</span><span class="sxs-lookup"><span data-stu-id="afdd4-147">Applications should query SFGAO_ISSLOW only on a background thread.</span></span> <span data-ttu-id="afdd4-148">替代方法（例如，抓取 <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> 屬性和測試 FILE_ATTRIBUTE_OFFLINE）可以用來取代涉及 SFGAO_ISSLOW 的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="afdd4-148">An alternate method, such as retrieving the <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> property and testing for FILE_ATTRIBUTE_OFFLINE, could be used in place of a method call that involves SFGAO_ISSLOW.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl> <span data-ttu-id="afdd4-149"><dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-149"><dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-150">指定的專案會顯示為暗灰色，而且無法供使用者使用。</span><span class="sxs-lookup"><span data-stu-id="afdd4-150">The specified items are shown as dimmed and unavailable to the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl> <span data-ttu-id="afdd4-151"><dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-151"><dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-152">指定的專案是快捷方式。</span><span class="sxs-lookup"><span data-stu-id="afdd4-152">The specified items are shortcuts.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl> <span data-ttu-id="afdd4-153"><dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-153"><dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-154">指定的物件是共用的。</span><span class="sxs-lookup"><span data-stu-id="afdd4-154">The specified objects are shared.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl> <span data-ttu-id="afdd4-155"><dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-155"><dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-156">指定的專案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="afdd4-156">The specified items are read-only.</span></span> <span data-ttu-id="afdd4-157">如果是資料夾，這表示無法在這些資料夾中建立新專案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-157">In the case of folders, this means that new items cannot be created in those folders.</span></span> <span data-ttu-id="afdd4-158">這不應該與<a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a>結構中<a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider：： GetItemData</strong></a>所抓取 FILE_ATTRIBUTE_READONLY 旗標所指定的行為混淆。</span><span class="sxs-lookup"><span data-stu-id="afdd4-158">This should not be confused with the behavior specified by the FILE_ATTRIBUTE_READONLY flag retrieved by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> in a <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a> structure.</span></span> <span data-ttu-id="afdd4-159">FILE_ATTRIBUTE_READONLY 對 Win32 檔系統資料夾沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="afdd4-159">FILE_ATTRIBUTE_READONLY has no meaning for Win32 file system folders.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl> <span data-ttu-id="afdd4-160"><dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-160"><dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-161">除非在 [<strong>資料夾設定</strong>] 中啟用 [<strong>顯示隱藏的檔案和資料夾</strong>] 選項，否則專案會隱藏，而且不應該顯示。</span><span class="sxs-lookup"><span data-stu-id="afdd4-161">The item is hidden and should not be displayed unless the <strong>Show hidden files and folders</strong> option is enabled in <strong>Folder Settings</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl> <span data-ttu-id="afdd4-162"><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000FC000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-162"><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000FC000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-163">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="afdd4-163">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl> <span data-ttu-id="afdd4-164"><dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-164"><dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-165">專案是 nonenumerated 專案，而且應該隱藏。</span><span class="sxs-lookup"><span data-stu-id="afdd4-165">The items are nonenumerated items and should be hidden.</span></span> <span data-ttu-id="afdd4-166">它們不會透過 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder：： EnumObjects</strong></a> 方法所建立的列舉值來傳回。</span><span class="sxs-lookup"><span data-stu-id="afdd4-166">They are not returned through an enumerator such as that created by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder::EnumObjects</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl> <span data-ttu-id="afdd4-167"><dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-167"><dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-168">專案包含新的內容，如特定應用程式所定義。</span><span class="sxs-lookup"><span data-stu-id="afdd4-168">The items contain new content, as defined by the particular application.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl> <span data-ttu-id="afdd4-169"><dt><strong>SFGAO_CANMONIKER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-169"><dt><strong>SFGAO_CANMONIKER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-170">不支援。</span><span class="sxs-lookup"><span data-stu-id="afdd4-170">Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl> <span data-ttu-id="afdd4-171"><dt><strong>SFGAO_HASSTORAGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-171"><dt><strong>SFGAO_HASSTORAGE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-172">不支援。</span><span class="sxs-lookup"><span data-stu-id="afdd4-172">Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl> <span data-ttu-id="afdd4-173"><dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-173"><dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-174">指出專案具有與其相關聯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="afdd4-174">Indicates that the item has a stream associated with it.</span></span> <span data-ttu-id="afdd4-175">您可以透過呼叫 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder：： BindToObject</strong></a> 或 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem：： BindToHandler</strong></a> ，在 <em>riid</em> 參數中使用 IID_IStream 來存取該資料流程。</span><span class="sxs-lookup"><span data-stu-id="afdd4-175">That stream can be accessed through a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a> with IID_IStream in the <em>riid</em> parameter.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl> <span data-ttu-id="afdd4-176"><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-176"><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-177">此專案的子系可透過 <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> 或 <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>存取。</span><span class="sxs-lookup"><span data-stu-id="afdd4-177">Children of this item are accessible through <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> or <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>.</span></span> <span data-ttu-id="afdd4-178">這些子系會標示 SFGAO_STORAGE 或 SFGAO_STREAM。</span><span class="sxs-lookup"><span data-stu-id="afdd4-178">Those children are flagged with SFGAO_STORAGE or SFGAO_STREAM.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl> <span data-ttu-id="afdd4-179"><dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-179"><dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-180">當指定為輸入時，SFGAO_VALIDATE 指示資料夾驗證資料夾或 Shell 專案陣列中包含的專案是否存在。</span><span class="sxs-lookup"><span data-stu-id="afdd4-180">When specified as input, SFGAO_VALIDATE instructs the folder to validate that the items contained in a folder or Shell item array exist.</span></span> <span data-ttu-id="afdd4-181">如果其中一或多個專案不存在， <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder：： GetAttributesOf</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray：： GetAttributes</strong></a> 會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="afdd4-181">If one or more of those items do not exist, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder::GetAttributesOf</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray::GetAttributes</strong></a> return a failure code.</span></span> <span data-ttu-id="afdd4-182">此旗標絕不會以 [out] 值傳回。</span><span class="sxs-lookup"><span data-stu-id="afdd4-182">This flag is never returned as an [out] value.</span></span><br/> <span data-ttu-id="afdd4-183">搭配檔系統資料夾使用時，SFGAO_VALIDATE 會指示資料夾捨棄 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2：： GetDetailsEx</strong></a> 用戶端所抓取的快取屬性，這些用戶端可能已針對指定的專案累積。</span><span class="sxs-lookup"><span data-stu-id="afdd4-183">When used with the file system folder, SFGAO_VALIDATE instructs the folder to discard cached properties retrieved by clients of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2::GetDetailsEx</strong></a> that might have accumulated for the specified items.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl> <span data-ttu-id="afdd4-184"><dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-184"><dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-185">指定的專案位於卸載式媒體或本身為卸載式裝置。</span><span class="sxs-lookup"><span data-stu-id="afdd4-185">The specified items are on removable media or are themselves removable devices.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl> <span data-ttu-id="afdd4-186"><dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-186"><dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-187">指定的專案會壓縮。</span><span class="sxs-lookup"><span data-stu-id="afdd4-187">The specified items are compressed.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl> <span data-ttu-id="afdd4-188"><dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-188"><dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-189">指定的專案可以裝載在網頁瀏覽器或 Windows 檔案總管框架內。</span><span class="sxs-lookup"><span data-stu-id="afdd4-189">The specified items can be hosted inside a web browser or Windows Explorer frame.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl> <span data-ttu-id="afdd4-190"><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-190"><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-191">指定的資料夾是檔系統資料夾，或包含至少一個子系 (子域、孫版或更新版本的) ，也就是檔案系統 (SFGAO_FILESYSTEM) 資料夾。</span><span class="sxs-lookup"><span data-stu-id="afdd4-191">The specified folders are either file system folders or contain at least one descendant (child, grandchild, or later) that is a file system (SFGAO_FILESYSTEM) folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl> <span data-ttu-id="afdd4-192"><dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-192"><dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-193">指定的專案是資料夾。</span><span class="sxs-lookup"><span data-stu-id="afdd4-193">The specified items are folders.</span></span> <span data-ttu-id="afdd4-194">某些專案可以用 SFGAO_STREAM 和 SFGAO_FOLDER 標記，例如副檔名為 .zip 的壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="afdd4-194">Some items can be flagged with both SFGAO_STREAM and SFGAO_FOLDER, such as a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="afdd4-195">當測試同時為檔案和容器的專案時，某些應用程式可能會包含此旗標。</span><span class="sxs-lookup"><span data-stu-id="afdd4-195">Some applications might include this flag when testing for items that are both files and containers.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl> <span data-ttu-id="afdd4-196"><dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-196"><dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-197">指定的資料夾或檔案是檔案系統的一部分 (也就是) 的檔案、目錄或根目錄。</span><span class="sxs-lookup"><span data-stu-id="afdd4-197">The specified folders or files are part of the file system (that is, they are files, directories, or root directories).</span></span> <span data-ttu-id="afdd4-198">專案的剖析名稱可以假設為有效的 Win32 檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="afdd4-198">The parsed names of the items can be assumed to be valid Win32 file system paths.</span></span> <span data-ttu-id="afdd4-199">這些路徑可以是以 UNC 或磁碟機號為基礎。</span><span class="sxs-lookup"><span data-stu-id="afdd4-199">These paths can be either UNC or drive-letter based.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl> <span data-ttu-id="afdd4-200"><dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70C50008</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-200"><dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70C50008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-201">此旗標是儲存功能屬性的遮罩： SFGAO_STORAGE、SFGAO_LINK、SFGAO_READONLY、SFGAO_STREAM、SFGAO_STORAGEANCESTOR、SFGAO_FILESYSANCESTOR、SFGAO_FOLDER 和 SFGAO_FILESYSTEM。</span><span class="sxs-lookup"><span data-stu-id="afdd4-201">This flag is a mask for the storage capability attributes: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER, and SFGAO_FILESYSTEM.</span></span> <span data-ttu-id="afdd4-202">呼叫端通常不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="afdd4-202">Callers normally do not use this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl> <span data-ttu-id="afdd4-203"><dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-203"><dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-204">指定的資料夾具有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="afdd4-204">The specified folders have subfolders.</span></span> <span data-ttu-id="afdd4-205">SFGAO_HASSUBFOLDER 屬性只是諮詢，而且可能會由 Shell 資料夾執行所傳回，即使它們不包含子資料夾也一樣。</span><span class="sxs-lookup"><span data-stu-id="afdd4-205">The SFGAO_HASSUBFOLDER attribute is only advisory and might be returned by Shell folder implementations even if they do not contain subfolders.</span></span> <span data-ttu-id="afdd4-206">不過請注意，相反地，無法傳回 SFGAO_HASSUBFOLDER，會明確指出資料夾物件沒有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="afdd4-206">Note, however, that the converse—failing to return SFGAO_HASSUBFOLDER—definitively states that the folder objects do not have subfolders.</span></span><br/> <span data-ttu-id="afdd4-207">當需要很長的時間來判斷是否有任何子資料夾時，建議您傳回 SFGAO_HASSUBFOLDER。</span><span class="sxs-lookup"><span data-stu-id="afdd4-207">Returning SFGAO_HASSUBFOLDER is recommended whenever a significant amount of time is required to determine whether any subfolders exist.</span></span> <span data-ttu-id="afdd4-208">例如，當資料夾位於網路磁碟機機上時，Shell 一律會傳回 SFGAO_HASSUBFOLDER。</span><span class="sxs-lookup"><span data-stu-id="afdd4-208">For example, the Shell always returns SFGAO_HASSUBFOLDER when a folder is located on a network drive.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl> <span data-ttu-id="afdd4-209"><dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-209"><dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-210">此旗標是 content 屬性的遮罩，目前只 SFGAO_HASSUBFOLDER。</span><span class="sxs-lookup"><span data-stu-id="afdd4-210">This flag is a mask for content attributes, at present only SFGAO_HASSUBFOLDER.</span></span> <span data-ttu-id="afdd4-211">呼叫端通常不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="afdd4-211">Callers normally do not use this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl> <span data-ttu-id="afdd4-212"><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </span><span class="sxs-lookup"><span data-stu-id="afdd4-212"><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="afdd4-213"><a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a>屬性所使用的遮罩，可判斷被視為導致緩慢計算或缺少內容的屬性： SFGAO_ISSLOW、SFGAO_READONLY、SFGAO_HASSUBFOLDER 和 SFGAO_VALIDATE。</span><span class="sxs-lookup"><span data-stu-id="afdd4-213">Mask used by the <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> property to determine attributes that are considered to cause slow calculations or lack context: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER, and SFGAO_VALIDATE.</span></span> <span data-ttu-id="afdd4-214">呼叫端通常不會使用此值。</span><span class="sxs-lookup"><span data-stu-id="afdd4-214">Callers normally do not use this value.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="afdd4-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="afdd4-215">Requirements</span></span>



| <span data-ttu-id="afdd4-216">需求</span><span class="sxs-lookup"><span data-stu-id="afdd4-216">Requirement</span></span> | <span data-ttu-id="afdd4-217">值</span><span class="sxs-lookup"><span data-stu-id="afdd4-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afdd4-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afdd4-218">Minimum supported client</span></span><br/> | <span data-ttu-id="afdd4-219">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afdd4-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afdd4-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afdd4-220">Minimum supported server</span></span><br/> | <span data-ttu-id="afdd4-221">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afdd4-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afdd4-222">標頭</span><span class="sxs-lookup"><span data-stu-id="afdd4-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdd4-223"><dt>Shobjidl.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="afdd4-223"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="afdd4-224">Idl</span><span class="sxs-lookup"><span data-stu-id="afdd4-224">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afdd4-225"><dt>Shobjidl.h .idl</dt></span><span class="sxs-lookup"><span data-stu-id="afdd4-225"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdd4-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afdd4-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdd4-227">**IShellFolder::GetAttributesOf**</span><span class="sxs-lookup"><span data-stu-id="afdd4-227">**IShellFolder::GetAttributesOf**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[<span data-ttu-id="afdd4-228">**IShellFolder：:P arseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="afdd4-228">**IShellFolder::ParseDisplayName**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[<span data-ttu-id="afdd4-229">**IShellItemArray：： GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="afdd4-229">**IShellItemArray::GetAttributes**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
