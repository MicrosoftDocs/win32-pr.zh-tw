---
title: Windows 工作站安全性與存取權限
description: 安全性可讓您控制對 window 站物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968907"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="10ac0-104">Windows 工作站安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="10ac0-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="10ac0-105">安全性可讓您控制對 window 站物件的存取。</span><span class="sxs-lookup"><span data-stu-id="10ac0-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="10ac0-106">如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。</span><span class="sxs-lookup"><span data-stu-id="10ac0-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="10ac0-107">當您呼叫 [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)函式時，可以指定視窗站物件的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。</span><span class="sxs-lookup"><span data-stu-id="10ac0-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="10ac0-108">如果您指定 Null，則視窗站會取得預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="10ac0-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="10ac0-109">視窗工作站之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。</span><span class="sxs-lookup"><span data-stu-id="10ac0-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="10ac0-110">若要取得或設定視窗站物件的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="10ac0-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="10ac0-111">當您呼叫 [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="10ac0-112">Windows 工作站物件的有效存取權限包括 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及某些特定物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="10ac0-113">下表列出所有物件使用的標準存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="10ac0-114">值</span><span class="sxs-lookup"><span data-stu-id="10ac0-114">Value</span></span>                       | <span data-ttu-id="10ac0-115">意義</span><span class="sxs-lookup"><span data-stu-id="10ac0-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ac0-116">刪除 (0x00010000L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="10ac0-117">刪除物件的必要參數。</span><span class="sxs-lookup"><span data-stu-id="10ac0-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="10ac0-118">讀取 \_ 控制 (0x00020000L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="10ac0-119">需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="10ac0-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="10ac0-120">若要讀取或寫入 SACL，您必須要求存取 \_ 系統 \_ 安全性存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="10ac0-121">如需詳細資訊，請參閱 [SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權。</span><span class="sxs-lookup"><span data-stu-id="10ac0-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="10ac0-122">同步處理 (0x00100000L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="10ac0-123">不支援 window 站物件。</span><span class="sxs-lookup"><span data-stu-id="10ac0-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="10ac0-124">撰寫 \_ DAC (0x00040000L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="10ac0-125">修改物件安全描述項中的 DACL 時需要。</span><span class="sxs-lookup"><span data-stu-id="10ac0-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="10ac0-126">撰寫 \_ 擁有者 (0x00080000L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="10ac0-127">需要變更物件之安全描述項中的擁有者。</span><span class="sxs-lookup"><span data-stu-id="10ac0-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="10ac0-128">下表列出特定物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="10ac0-129">存取權限</span><span class="sxs-lookup"><span data-stu-id="10ac0-129">Access right</span></span>                        | <span data-ttu-id="10ac0-130">Description</span><span class="sxs-lookup"><span data-stu-id="10ac0-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ac0-131">WINSTA \_ 所有 \_ 存取 (0x37F) </span><span class="sxs-lookup"><span data-stu-id="10ac0-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="10ac0-132">視窗工作站的所有可能存取權限。</span><span class="sxs-lookup"><span data-stu-id="10ac0-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="10ac0-133">WINSTA \_ ACCESSCLIPBOARD (0x0004L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="10ac0-134">使用剪貼簿所需。</span><span class="sxs-lookup"><span data-stu-id="10ac0-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="10ac0-135">WINSTA \_ ACCESSGLOBALATOMS (0x0020L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="10ac0-136">操作全域原子的必要參數。</span><span class="sxs-lookup"><span data-stu-id="10ac0-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="10ac0-137">WINSTA \_ CREATEDESKTOP (0x0008L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="10ac0-138">需要在視窗工作站上建立新的桌面物件。</span><span class="sxs-lookup"><span data-stu-id="10ac0-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="10ac0-139">WINSTA \_ ENUMDESKTOPS (0x0001L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="10ac0-140">列舉現有桌面物件所需。</span><span class="sxs-lookup"><span data-stu-id="10ac0-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="10ac0-141">WINSTA \_ 列舉 (0x0100L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="10ac0-142">要列舉之視窗工作站的必要參數。</span><span class="sxs-lookup"><span data-stu-id="10ac0-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="10ac0-143">WINSTA \_ EXITWINDOWS (0x0040L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="10ac0-144">成功呼叫 [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) 或 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函數所需。</span><span class="sxs-lookup"><span data-stu-id="10ac0-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="10ac0-145">使用者可以共用視窗工作站，而這種存取類型可以防止視窗工作站的其他使用者登出視窗工作站擁有者。</span><span class="sxs-lookup"><span data-stu-id="10ac0-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="10ac0-146">WINSTA \_ READATTRIBUTES (0x0002L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="10ac0-147">讀取視窗站物件的屬性時需要。</span><span class="sxs-lookup"><span data-stu-id="10ac0-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="10ac0-148">此屬性包含色彩設定和其他全域視窗工作站屬性。</span><span class="sxs-lookup"><span data-stu-id="10ac0-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="10ac0-149">WINSTA \_ READSCREEN (0x0200L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="10ac0-150">存取螢幕內容所需。</span><span class="sxs-lookup"><span data-stu-id="10ac0-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="10ac0-151">WINSTA \_ WRITEATTRIBUTES (0x0010L) </span><span class="sxs-lookup"><span data-stu-id="10ac0-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="10ac0-152">修改視窗工作站物件的屬性時所需。</span><span class="sxs-lookup"><span data-stu-id="10ac0-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="10ac0-153">這些屬性包括色彩設定和其他全域視窗工作站屬性。</span><span class="sxs-lookup"><span data-stu-id="10ac0-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="10ac0-154">以下是互動式視窗工作站物件的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) ，也就是指派給互動式使用者登入會話的視窗站。</span><span class="sxs-lookup"><span data-stu-id="10ac0-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10ac0-155">存取權限</span><span class="sxs-lookup"><span data-stu-id="10ac0-155">Access right</span></span></th>
<th><span data-ttu-id="10ac0-156">Description</span><span class="sxs-lookup"><span data-stu-id="10ac0-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10ac0-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="10ac0-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="10ac0-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="10ac0-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="10ac0-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="10ac0-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="10ac0-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="10ac0-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="10ac0-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="10ac0-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="10ac0-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10ac0-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="10ac0-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="10ac0-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="10ac0-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="10ac0-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="10ac0-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="10ac0-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="10ac0-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="10ac0-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10ac0-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="10ac0-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="10ac0-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="10ac0-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="10ac0-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="10ac0-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="10ac0-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="10ac0-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10ac0-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="10ac0-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="10ac0-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="10ac0-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="10ac0-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="10ac0-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="10ac0-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="10ac0-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="10ac0-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="10ac0-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="10ac0-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="10ac0-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="10ac0-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="10ac0-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="10ac0-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="10ac0-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="10ac0-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="10ac0-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="10ac0-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="10ac0-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10ac0-183">以下是非互動式視窗工作站物件的 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="10ac0-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="10ac0-184">系統會將非互動式視窗工作站指派給互動式使用者以外的所有登入會話。</span><span class="sxs-lookup"><span data-stu-id="10ac0-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10ac0-185">存取權限</span><span class="sxs-lookup"><span data-stu-id="10ac0-185">Access right</span></span></th>
<th><span data-ttu-id="10ac0-186">Description</span><span class="sxs-lookup"><span data-stu-id="10ac0-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10ac0-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="10ac0-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="10ac0-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="10ac0-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="10ac0-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="10ac0-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="10ac0-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="10ac0-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="10ac0-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10ac0-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="10ac0-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="10ac0-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="10ac0-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="10ac0-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="10ac0-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="10ac0-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="10ac0-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10ac0-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="10ac0-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="10ac0-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="10ac0-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="10ac0-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="10ac0-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="10ac0-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="10ac0-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10ac0-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="10ac0-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="10ac0-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="10ac0-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="10ac0-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="10ac0-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="10ac0-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="10ac0-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="10ac0-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="10ac0-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="10ac0-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="10ac0-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="10ac0-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="10ac0-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="10ac0-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="10ac0-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="10ac0-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="10ac0-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10ac0-209">\_ \_ 如果您想要讀取或寫入物件的 SACL，您可以向 windows 工作站物件要求存取系統安全性存取權。</span><span class="sxs-lookup"><span data-stu-id="10ac0-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="10ac0-210">如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="10ac0-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 