---
title: 桌面安全性與存取權限
description: 安全性可讓您控制對桌面物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375960"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="d335f-104">桌面安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="d335f-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="d335f-105">安全性可讓您控制對桌面物件的存取。</span><span class="sxs-lookup"><span data-stu-id="d335f-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="d335f-106">如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。</span><span class="sxs-lookup"><span data-stu-id="d335f-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="d335f-107">當您呼叫 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)或 [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)函式時，可以指定桌面物件的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。</span><span class="sxs-lookup"><span data-stu-id="d335f-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="d335f-108">如果您指定 Null，桌面會取得預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="d335f-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="d335f-109">桌面預設安全描述項中的 Acl 來自于其父視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="d335f-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="d335f-110">若要取得或設定視窗站物件的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="d335f-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="d335f-111">當您呼叫 [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) 或 [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="d335f-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="d335f-112">桌面物件的有效存取權限包括 [標準存取權限](/windows/desktop/SecAuthZ/standard-access-rights) ，以及某些特定物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="d335f-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="d335f-113">下表列出所有物件使用的標準存取權限。</span><span class="sxs-lookup"><span data-stu-id="d335f-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="d335f-114">值</span><span class="sxs-lookup"><span data-stu-id="d335f-114">Value</span></span>                       | <span data-ttu-id="d335f-115">意義</span><span class="sxs-lookup"><span data-stu-id="d335f-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d335f-116">刪除 (0x00010000L) </span><span class="sxs-lookup"><span data-stu-id="d335f-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="d335f-117">刪除物件的必要參數。</span><span class="sxs-lookup"><span data-stu-id="d335f-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d335f-118">讀取 \_ 控制 (0x00020000L) </span><span class="sxs-lookup"><span data-stu-id="d335f-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="d335f-119">需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。</span><span class="sxs-lookup"><span data-stu-id="d335f-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="d335f-120">若要讀取或寫入 SACL，您必須要求存取 \_ 系統 \_ 安全性存取權限。</span><span class="sxs-lookup"><span data-stu-id="d335f-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="d335f-121">如需詳細資訊，請參閱 [SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權。</span><span class="sxs-lookup"><span data-stu-id="d335f-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="d335f-122">同步處理 (0x00100000L) </span><span class="sxs-lookup"><span data-stu-id="d335f-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="d335f-123">不支援桌面物件。</span><span class="sxs-lookup"><span data-stu-id="d335f-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d335f-124">撰寫 \_ DAC (0x00040000L) </span><span class="sxs-lookup"><span data-stu-id="d335f-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="d335f-125">修改物件安全描述項中的 DACL 時需要。</span><span class="sxs-lookup"><span data-stu-id="d335f-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="d335f-126">撰寫 \_ 擁有者 (0x00080000L) </span><span class="sxs-lookup"><span data-stu-id="d335f-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="d335f-127">需要變更物件之安全描述項中的擁有者。</span><span class="sxs-lookup"><span data-stu-id="d335f-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="d335f-128">下表列出特定物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="d335f-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="d335f-129">存取權限</span><span class="sxs-lookup"><span data-stu-id="d335f-129">Access right</span></span>                       | <span data-ttu-id="d335f-130">Description</span><span class="sxs-lookup"><span data-stu-id="d335f-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d335f-131">DESKTOP \_ CREATEMENU (0x0004L) </span><span class="sxs-lookup"><span data-stu-id="d335f-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="d335f-132">在桌面上建立功能表所需。</span><span class="sxs-lookup"><span data-stu-id="d335f-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="d335f-133">桌上型電腦 \_ CREATEWINDOW (0x0002L) </span><span class="sxs-lookup"><span data-stu-id="d335f-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="d335f-134">需要在桌面上建立視窗。</span><span class="sxs-lookup"><span data-stu-id="d335f-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="d335f-135">桌面 \_ 列舉 (0x0040L) </span><span class="sxs-lookup"><span data-stu-id="d335f-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="d335f-136">要列舉桌面的必要參數。</span><span class="sxs-lookup"><span data-stu-id="d335f-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="d335f-137">DESKTOP \_ HOOKCONTROL (0x0008L) </span><span class="sxs-lookup"><span data-stu-id="d335f-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="d335f-138">建立任何視窗勾點所需。</span><span class="sxs-lookup"><span data-stu-id="d335f-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="d335f-139">DESKTOP \_ JOURNALPLAYBACK (0x0020L) </span><span class="sxs-lookup"><span data-stu-id="d335f-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="d335f-140">在桌面上執行日誌播放所需。</span><span class="sxs-lookup"><span data-stu-id="d335f-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="d335f-141">DESKTOP \_ JOURNALRECORD (0x0010L) </span><span class="sxs-lookup"><span data-stu-id="d335f-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="d335f-142">在桌上型電腦上執行日誌記錄的必要。</span><span class="sxs-lookup"><span data-stu-id="d335f-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="d335f-143">DESKTOP \_ READOBJECTS (0x0001L) </span><span class="sxs-lookup"><span data-stu-id="d335f-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="d335f-144">讀取桌面上的物件所需。</span><span class="sxs-lookup"><span data-stu-id="d335f-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="d335f-145">DESKTOP \_ SWITCHDESKTOP (0x0100L) </span><span class="sxs-lookup"><span data-stu-id="d335f-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="d335f-146">必須使用 [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) 函式來啟動桌面。</span><span class="sxs-lookup"><span data-stu-id="d335f-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="d335f-147">DESKTOP \_ WRITEOBJECTS (0x0080L) </span><span class="sxs-lookup"><span data-stu-id="d335f-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="d335f-148">需要在桌上型電腦上撰寫物件。</span><span class="sxs-lookup"><span data-stu-id="d335f-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="d335f-149">以下是使用者登入會話的互動式視窗工作站中包含的桌面物件 [一般存取權限](/windows/desktop/SecAuthZ/generic-access-rights) 。</span><span class="sxs-lookup"><span data-stu-id="d335f-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d335f-150">存取權限</span><span class="sxs-lookup"><span data-stu-id="d335f-150">Access right</span></span></th>
<th><span data-ttu-id="d335f-151">Description</span><span class="sxs-lookup"><span data-stu-id="d335f-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d335f-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="d335f-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="d335f-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="d335f-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="d335f-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d335f-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="d335f-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="d335f-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d335f-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="d335f-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="d335f-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="d335f-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="d335f-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="d335f-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="d335f-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="d335f-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="d335f-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="d335f-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="d335f-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="d335f-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="d335f-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d335f-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="d335f-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="d335f-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d335f-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="d335f-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="d335f-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="d335f-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="d335f-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="d335f-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d335f-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="d335f-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="d335f-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="d335f-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="d335f-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="d335f-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="d335f-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="d335f-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="d335f-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="d335f-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="d335f-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="d335f-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="d335f-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="d335f-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="d335f-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d335f-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="d335f-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="d335f-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="d335f-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="d335f-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="d335f-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="d335f-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d335f-178">\_ \_ 如果您想要讀取或寫入物件的 SACL，您可以向桌面物件要求存取系統安全性存取權。</span><span class="sxs-lookup"><span data-stu-id="d335f-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="d335f-179">如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。</span><span class="sxs-lookup"><span data-stu-id="d335f-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 