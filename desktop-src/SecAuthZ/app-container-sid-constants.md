---
description: 指示應用程式封裝授權單位。
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: '應用程式容器 SID 常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980440"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="7cf36-103">應用程式容器 SID 常數</span><span class="sxs-lookup"><span data-stu-id="7cf36-103">App Container SID Constants</span></span>

<span data-ttu-id="7cf36-104">應用程式容器的特定 SID 常數會指示應用程式封裝授權單位。</span><span class="sxs-lookup"><span data-stu-id="7cf36-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="7cf36-105">雖然開發人員可以直接使用這些常數，但大部分的開發人員不需要定義這些應用程式容器 Sid。</span><span class="sxs-lookup"><span data-stu-id="7cf36-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="7cf36-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**安全性 \_應用程式 \_ 套件 \_ 授權** 單位 ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **安全性 \_ 應用程式 \_ 套件 \_ 基底 \_ RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> **安全性內 \_ 建 \_ 應用程式 \_ 套件 \_ rid \_ 計數** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **安全性 \_ 應用程式 \_ 套件 \_ rid \_ 計數** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **安全性 \_ 功能 \_ 基礎 \_ rid** (0x00000003L) 安全性內 <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **\_ 建 \_ 功能 \_ rid \_** 計數 (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> **安全性 \_ 功能 \_ rid \_ 計數** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **安全性內 \_ 建 \_ 封裝 \_ 任何 \_ 套件** (0x00000001L) </span><span class="sxs-lookup"><span data-stu-id="7cf36-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="7cf36-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cf36-107">Requirements</span></span>



| <span data-ttu-id="7cf36-108">需求</span><span class="sxs-lookup"><span data-stu-id="7cf36-108">Requirement</span></span> | <span data-ttu-id="7cf36-109">值</span><span class="sxs-lookup"><span data-stu-id="7cf36-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf36-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cf36-110">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf36-111">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf36-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7cf36-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cf36-112">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf36-113">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cf36-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7cf36-114">標頭</span><span class="sxs-lookup"><span data-stu-id="7cf36-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf36-115"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf36-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




