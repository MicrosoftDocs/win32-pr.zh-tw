---
description: 值會定義特定的 SAS 類型。
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: 'WLX_SAS_TYPE_XXX (Winwlx) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975397"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="03bf4-103">WLX \_ SAS \_ 類型 \_ XXX</span><span class="sxs-lookup"><span data-stu-id="03bf4-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="03bf4-104">\[WLX \_ SAS \_ 類型 \_ XXX 常數不再適用于 windows Server 2008 和 windows Vista 的使用。\]</span><span class="sxs-lookup"><span data-stu-id="03bf4-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="03bf4-105">**WLX \_ SAS \_ 類型 \_ XXX** 值會定義特定的 sas 類型。</span><span class="sxs-lookup"><span data-stu-id="03bf4-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="03bf4-106">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="03bf4-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="03bf4-107">從零到127的所有值都會保留給 Microsoft 定義的類型。</span><span class="sxs-lookup"><span data-stu-id="03bf4-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="03bf4-108">127以上的值適用于客戶定義的類型。</span><span class="sxs-lookup"><span data-stu-id="03bf4-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="03bf4-109">下列類型會傳遞至具有 *dwSasType* 參數的函式。</span><span class="sxs-lookup"><span data-stu-id="03bf4-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="03bf4-110">常數</span><span class="sxs-lookup"><span data-stu-id="03bf4-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="03bf4-111">描述</span><span class="sxs-lookup"><span data-stu-id="03bf4-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="03bf4-112"><dt>**WLX \_ SAS \_ 類型 \_ CTRL \_ ALT \_ DEL**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="03bf4-113">表示使用者已輸入標準 CTRL + ALT + DEL SAS。</span><span class="sxs-lookup"><span data-stu-id="03bf4-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="03bf4-114"><dt>**WLX \_ SAS \_ 類型 \_ SC \_ INSERT**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="03bf4-115">指出 [*智慧卡*](../secgloss/s-gly.md) 已插入相容的裝置。</span><span class="sxs-lookup"><span data-stu-id="03bf4-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="03bf4-116"><dt>**WLX \_ SAS \_ 類型 \_ SC \_ REMOVE**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="03bf4-117">表示已從相容裝置移除智慧卡。</span><span class="sxs-lookup"><span data-stu-id="03bf4-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="03bf4-118"><dt>**WLX \_ SAS \_ 類型 \_ SCRNSVR \_ 活動**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="03bf4-119">指出當安全的螢幕保護裝置啟用時，鍵盤或滑鼠活動發生。</span><span class="sxs-lookup"><span data-stu-id="03bf4-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="03bf4-120"><dt>**WLX \_ SAS \_ 類型 \_ SCRNSVR \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="03bf4-121">指出由於鍵盤和滑鼠非活動而發生螢幕保護裝置啟用。</span><span class="sxs-lookup"><span data-stu-id="03bf4-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="03bf4-122"><dt>**WLX \_ SAS \_ 類型 \_ 超時**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="03bf4-123">表示在指定的超時時間內未收到任何使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="03bf4-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="03bf4-124"><dt>**WLX \_ SAS \_ 類型 \_ 使用者 \_ 登出**</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="03bf4-125">指出正在將使用者登出系統。</span><span class="sxs-lookup"><span data-stu-id="03bf4-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="03bf4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="03bf4-126">Requirements</span></span>



| <span data-ttu-id="03bf4-127">需求</span><span class="sxs-lookup"><span data-stu-id="03bf4-127">Requirement</span></span> | <span data-ttu-id="03bf4-128">值</span><span class="sxs-lookup"><span data-stu-id="03bf4-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03bf4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03bf4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="03bf4-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03bf4-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03bf4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03bf4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="03bf4-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03bf4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03bf4-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="03bf4-133">End of client support</span></span><br/>    | <span data-ttu-id="03bf4-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="03bf4-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="03bf4-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="03bf4-135">End of server support</span></span><br/>    | <span data-ttu-id="03bf4-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03bf4-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="03bf4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="03bf4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="03bf4-138"><dt>Winwlx。h</dt></span><span class="sxs-lookup"><span data-stu-id="03bf4-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
