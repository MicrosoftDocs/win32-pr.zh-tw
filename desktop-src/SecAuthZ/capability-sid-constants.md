---
description: 使用 AllocateAndInitializeSid 函式來定義應用程式的知名功能。
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: '功能 SID 常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195573"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="be0e5-103">功能 SID 常數</span><span class="sxs-lookup"><span data-stu-id="be0e5-103">Capability SID Constants</span></span>

<span data-ttu-id="be0e5-104">功能 SID 常數會使用 [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) 函式來定義應用程式的知名功能。</span><span class="sxs-lookup"><span data-stu-id="be0e5-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="be0e5-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**安全性 \_ 功能 \_ 網際網路 \_ 用戶端**</span><span class="sxs-lookup"><span data-stu-id="be0e5-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-106"> (0x00000001L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-107">帳戶可以從用戶端電腦存取網際網路。</span><span class="sxs-lookup"><span data-stu-id="be0e5-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**安全性 \_ 功能 \_ 網際網路 \_ 用戶端 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="be0e5-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-109"> (0x00000002L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-110">帳戶可以從用戶端和伺服器電腦存取網際網路。</span><span class="sxs-lookup"><span data-stu-id="be0e5-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**安全性 \_ 功能 \_ 專用 \_ 網 \_ 用戶端 \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="be0e5-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-112"> (0x00000003L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-113">帳戶可以從私人網路存取網際網路。</span><span class="sxs-lookup"><span data-stu-id="be0e5-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**安全性 \_ 功能 \_ 圖片 \_ 庫**</span><span class="sxs-lookup"><span data-stu-id="be0e5-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-115"> (0x00000004L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-116">帳戶具有圖片媒體櫃的存取權。</span><span class="sxs-lookup"><span data-stu-id="be0e5-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**安全性 \_ 功能 \_ 影片 \_ 庫**</span><span class="sxs-lookup"><span data-stu-id="be0e5-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-118"> (0x00000005L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-119">帳戶可以存取影片庫。</span><span class="sxs-lookup"><span data-stu-id="be0e5-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**安全性 \_ 功能 \_ 音樂 \_ 媒體櫃**</span><span class="sxs-lookup"><span data-stu-id="be0e5-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-121"> (0x00000006L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-122">帳戶具有音樂媒體櫃的存取權。</span><span class="sxs-lookup"><span data-stu-id="be0e5-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**安全性 \_ 功能 \_ 文檔 \_ 庫**</span><span class="sxs-lookup"><span data-stu-id="be0e5-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-124"> (0x00000007L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-125">帳戶可以存取文件庫。</span><span class="sxs-lookup"><span data-stu-id="be0e5-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**安全性 \_ 功能 \_ 企業 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="be0e5-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-127"> (0x00000008L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-128">帳戶可以存取預設的 Windows 認證。</span><span class="sxs-lookup"><span data-stu-id="be0e5-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**安全性 \_ 功能 \_ 共用 \_ 使用者 \_ 憑證**</span><span class="sxs-lookup"><span data-stu-id="be0e5-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-130"> (0x00000009L) </span><span class="sxs-lookup"><span data-stu-id="be0e5-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-131">帳戶可以存取共用使用者憑證。</span><span class="sxs-lookup"><span data-stu-id="be0e5-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="be0e5-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**安全性 \_ 功能 \_ 可移動 \_ 存儲**</span><span class="sxs-lookup"><span data-stu-id="be0e5-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0e5-133"> (0x0000000AL) </span><span class="sxs-lookup"><span data-stu-id="be0e5-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="be0e5-134">帳戶具有卸除式存放裝置的存取權。</span><span class="sxs-lookup"><span data-stu-id="be0e5-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be0e5-135">備註</span><span class="sxs-lookup"><span data-stu-id="be0e5-135">Remarks</span></span>

<span data-ttu-id="be0e5-136">在建立功能 SID 時，您需要在 AllocateAndInitializeSid 函式的呼叫中包含封裝授權單位、安全性 \_ 應用程式 \_ 封裝 \_ 授權 {0,0,0,0,0,15} 單位。 [](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)</span><span class="sxs-lookup"><span data-stu-id="be0e5-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="be0e5-137">此外，您還需要內建功能、安全性 \_ 功能 \_ 基礎 \_ rid (0X00000003L) 和安全性內 \_ 建 \_ 功能 \_ rid \_ 計數 (2L) 的基礎 RID 和 rid 計數。</span><span class="sxs-lookup"><span data-stu-id="be0e5-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="be0e5-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="be0e5-138">Requirements</span></span>



| <span data-ttu-id="be0e5-139">需求</span><span class="sxs-lookup"><span data-stu-id="be0e5-139">Requirement</span></span> | <span data-ttu-id="be0e5-140">值</span><span class="sxs-lookup"><span data-stu-id="be0e5-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be0e5-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be0e5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="be0e5-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be0e5-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="be0e5-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be0e5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="be0e5-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be0e5-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be0e5-145">標頭</span><span class="sxs-lookup"><span data-stu-id="be0e5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="be0e5-146"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="be0e5-146"><dt>Winnt.h</dt></span></span> </dl> |



 

