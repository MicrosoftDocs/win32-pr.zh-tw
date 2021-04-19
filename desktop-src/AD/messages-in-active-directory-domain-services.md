---
title: Active Directory Domain Services 中的訊息
description: Active Directory Domain Services 中的訊息可在 Windows 2000 和 Windows NT 4.0 （含 Service Pack 6a (SP6a) 和更新版本與 DSClient）中運作。
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory 訊息廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968008"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="59f74-104">Active Directory Domain Services 中的訊息</span><span class="sxs-lookup"><span data-stu-id="59f74-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="59f74-105">Active Directory Domain Services 中的訊息可在 Windows 2000 和 Windows NT 4.0 （含 Service Pack 6a (SP6a) 和更新版本與 DSClient）中運作。</span><span class="sxs-lookup"><span data-stu-id="59f74-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="59f74-106">它們也可以在具有 IE 4.01 和更新版本和 DSClient 的 Windows 98/95 工作站中運作。</span><span class="sxs-lookup"><span data-stu-id="59f74-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="59f74-107">但是，如果從 shell 啟動了多重選屬性頁，則會 [**\_ 通知 WM ADSPROP \_ 通知 \_ 錯誤**](wm-adsprop-notify-error.md) 訊息及其對應的 helper 函式， [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) 和 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) 無法正常運作，且不會顯示。</span><span class="sxs-lookup"><span data-stu-id="59f74-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="59f74-108">如果在系統管理工具（例如 AD 使用者和電腦）內啟動多重複選屬性頁面，則所有訊息都可以正常運作，並可在多重複選屬性頁面中顯示。</span><span class="sxs-lookup"><span data-stu-id="59f74-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="59f74-109">Active Directory Domain Services 使用下列訊息：</span><span class="sxs-lookup"><span data-stu-id="59f74-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="59f74-110">**WM \_ ADSPROP \_ 通知 \_ 申請**</span><span class="sxs-lookup"><span data-stu-id="59f74-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="59f74-111">**WM \_ ADSPROP \_ 通知 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="59f74-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="59f74-112">**WM \_ ADSPROP \_ 通知 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="59f74-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="59f74-113">**WM \_ ADSPROP \_ 通知 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="59f74-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="59f74-114">**WM \_ ADSPROP \_ 通知 \_ 前景**</span><span class="sxs-lookup"><span data-stu-id="59f74-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="59f74-115">**WM \_ ADSPROP \_ 通知 \_ PAGEHWND**</span><span class="sxs-lookup"><span data-stu-id="59f74-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="59f74-116">**WM \_ ADSPROP \_ 通知 \_ PAGEINIT**</span><span class="sxs-lookup"><span data-stu-id="59f74-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="59f74-117">**WM \_ ADSPROP \_ 通知 \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="59f74-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="59f74-118">**WM \_ ADSPROP \_ 工作表 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="59f74-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="59f74-119">**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="59f74-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="59f74-120">**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="59f74-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




