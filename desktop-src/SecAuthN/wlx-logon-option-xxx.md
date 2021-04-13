---
description: WlxLoggedOutSAS 的 >dwoptions 參數會使用值。
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: 'WLX_LOGON_OPTION_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319831"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="ea7ed-103">WLX \_ LOGON \_ 選項 \_ XXX</span><span class="sxs-lookup"><span data-stu-id="ea7ed-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="ea7ed-104">\[WLX \_ LOGON \_ 選項 \_ XXX 常數不再適用于 windows Server 2008 和 windows Vista 的使用。\]</span><span class="sxs-lookup"><span data-stu-id="ea7ed-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="ea7ed-105">**WLX \_ LOGON \_ 選項 \_ XXX** 值是由 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)的 *>dwoptions* 參數使用。</span><span class="sxs-lookup"><span data-stu-id="ea7ed-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="ea7ed-106">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="ea7ed-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="ea7ed-107">成功登入時，您的 GINA DLL 可以使用此值來指定下列選項。</span><span class="sxs-lookup"><span data-stu-id="ea7ed-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="ea7ed-108">常數</span><span class="sxs-lookup"><span data-stu-id="ea7ed-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="ea7ed-109">描述</span><span class="sxs-lookup"><span data-stu-id="ea7ed-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="ea7ed-110"><dt>**WLX \_ 登入 \_ 選擇 \_ 沒有 \_ 設定檔**</dt></span><span class="sxs-lookup"><span data-stu-id="ea7ed-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="ea7ed-111">指定 Winlogon 不得為登入的使用者載入設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea7ed-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="ea7ed-112">在此情況下，您的 GINA DLL 將會載入設定檔，或使用者不需要設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea7ed-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ea7ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea7ed-113">Requirements</span></span>



| <span data-ttu-id="ea7ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="ea7ed-114">Requirement</span></span> | <span data-ttu-id="ea7ed-115">值</span><span class="sxs-lookup"><span data-stu-id="ea7ed-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7ed-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea7ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea7ed-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea7ed-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ea7ed-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea7ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea7ed-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea7ed-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ea7ed-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ea7ed-120">End of client support</span></span><br/>    | <span data-ttu-id="ea7ed-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea7ed-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="ea7ed-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ea7ed-122">End of server support</span></span><br/>    | <span data-ttu-id="ea7ed-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea7ed-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="ea7ed-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ea7ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea7ed-125"><dt>Winwlx。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea7ed-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




