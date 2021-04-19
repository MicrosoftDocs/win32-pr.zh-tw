---
title: 存取替代登錄視圖
description: 根據預設，在 WOW64 上執行的 32 位元應用程式會存取 32 位元登錄檢視，而 64 位元應用程式會存取 64 位元登錄檢視。
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- 登錄視圖64位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，登錄視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "106998935"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="8820f-105">存取替代登錄視圖</span><span class="sxs-lookup"><span data-stu-id="8820f-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="8820f-106">根據預設，在 WOW64 上執行的 32 位元應用程式會存取 32 位元登錄檢視，而 64 位元應用程式會存取 64 位元登錄檢視。</span><span class="sxs-lookup"><span data-stu-id="8820f-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="8820f-107">下列旗標可讓32位應用程式存取64位登錄視圖和64位應用程式中重新導向的金鑰，以存取32位登錄視圖中重新導向的金鑰。</span><span class="sxs-lookup"><span data-stu-id="8820f-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="8820f-108">這些旗標對共用的登錄機碼沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="8820f-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="8820f-109">如需詳細資訊，請參閱 [受 WOW64 影響的](shared-registry-keys.md)登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="8820f-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="8820f-110">旗標名稱</span><span class="sxs-lookup"><span data-stu-id="8820f-110">Flag name</span></span>         | <span data-ttu-id="8820f-111">值</span><span class="sxs-lookup"><span data-stu-id="8820f-111">Value</span></span>  | <span data-ttu-id="8820f-112">描述</span><span class="sxs-lookup"><span data-stu-id="8820f-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8820f-113">KEY \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="8820f-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="8820f-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="8820f-114">0x0100</span></span> | <span data-ttu-id="8820f-115">從32位或64位應用程式存取64位金鑰。</span><span class="sxs-lookup"><span data-stu-id="8820f-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="8820f-116">KEY \_ WOW64 \_ 32KEY</span><span class="sxs-lookup"><span data-stu-id="8820f-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="8820f-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="8820f-117">0x0200</span></span> | <span data-ttu-id="8820f-118">從32位或64位應用程式存取32位金鑰。</span><span class="sxs-lookup"><span data-stu-id="8820f-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="8820f-119">**ARM 上的 Windows 10：** 這是指32位 ARM 進程的32位 ARM 登錄視圖，以及適用于32位 x86 和 64 bit ARM64 進程的32位 x86 登錄視圖。</span><span class="sxs-lookup"><span data-stu-id="8820f-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="8820f-120">您可以在下列登錄函式的 *samDesired* 參數中指定這些旗標：</span><span class="sxs-lookup"><span data-stu-id="8820f-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="8820f-121">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="8820f-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="8820f-122">**RegDeleteKeyEx**</span><span class="sxs-lookup"><span data-stu-id="8820f-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="8820f-123">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="8820f-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="8820f-124">您 \_ \_ 可以指定 key wow64 32KEY 或 key \_ wow64 \_ 64KEY。</span><span class="sxs-lookup"><span data-stu-id="8820f-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="8820f-125">如果同時指定這兩個旗標，則函式會失敗，並出現錯誤 \_ \_ 參數無效。</span><span class="sxs-lookup"><span data-stu-id="8820f-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="8820f-126">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 如果同時指定這兩個旗標，則函式的行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8820f-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="8820f-127">[**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)函數不能用來存取替代登錄視圖。</span><span class="sxs-lookup"><span data-stu-id="8820f-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="8820f-128">以下是從應用程式存取登錄的最佳作法：</span><span class="sxs-lookup"><span data-stu-id="8820f-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="8820f-129">應用程式使用其中一個旗標存取替代登錄視圖之後，所有後續的作業 (建立、刪除或開啟子登錄機碼) ，必須明確地使用相同的旗標。</span><span class="sxs-lookup"><span data-stu-id="8820f-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="8820f-130">否則，可能會發生非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="8820f-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="8820f-131">若要正確列舉兩個視圖中的所有索引鍵，請在兩個階段中執行列舉。</span><span class="sxs-lookup"><span data-stu-id="8820f-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="8820f-132">第一個階段應使用以其中一個旗標開啟的控制碼，而另一個傳遞應使用以其他旗標開啟的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8820f-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="8820f-133">**Wow6432Node** 和 **WowAA32Node** 金鑰是保留的。</span><span class="sxs-lookup"><span data-stu-id="8820f-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="8820f-134">為了相容，應用程式不應該直接使用這些金鑰。</span><span class="sxs-lookup"><span data-stu-id="8820f-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="8820f-135">如需透過 WMI 存取替代登錄視圖的詳細資訊，請參閱 [在64位平臺上要求 WMI 資料](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform)。</span><span class="sxs-lookup"><span data-stu-id="8820f-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8820f-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8820f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8820f-137">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="8820f-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="8820f-138">登錄反映</span><span class="sxs-lookup"><span data-stu-id="8820f-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

