---
title: 'TBN_GETDISPINFO (Commctrl 的通知碼) '
description: 抓取工具列專案的顯示資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ed6e4141-2bf8-4a92-8349-f3833c87fcf3
keywords:
- TBN_GETDISPINFO 通知碼 Windows 控制項
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f3a0a47adfe7f172f7a4d0e4c9139b67aef01d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105029"
---
# <a name="tbn_getdispinfo-notification-code"></a><span data-ttu-id="b301c-105">TBN \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="b301c-105">TBN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="b301c-106">抓取工具列專案的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="b301c-106">Retrieves display information for a toolbar item.</span></span> <span data-ttu-id="b301c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b301c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETDISPINFO 

    lptbdi = (LPNMTBDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b301c-108">參數</span><span class="sxs-lookup"><span data-stu-id="b301c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b301c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b301c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b301c-110">[**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b301c-110">Pointer to an [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa) structure.</span></span> <span data-ttu-id="b301c-111">**IdCommand** 成員會指定專案的命令識別碼、 **lParam** 成員包含專案的應用程式定義資料，而 **dwMask** 成員會指定所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="b301c-111">The **idCommand** member specifies the item's command identifier, the **lParam** member contains the item's application-defined data, and the **dwMask** member specifies what information is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b301c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b301c-112">Return value</span></span>

<span data-ttu-id="b301c-113">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="b301c-113">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b301c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b301c-114">Requirements</span></span>



| <span data-ttu-id="b301c-115">需求</span><span class="sxs-lookup"><span data-stu-id="b301c-115">Requirement</span></span> | <span data-ttu-id="b301c-116">值</span><span class="sxs-lookup"><span data-stu-id="b301c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b301c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b301c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b301c-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b301c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b301c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b301c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b301c-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b301c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b301c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b301c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b301c-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b301c-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b301c-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b301c-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b301c-124">**TBN \_GETDISPINFOW** (Unicode) 和 **TBN \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b301c-124">**TBN\_GETDISPINFOW** (Unicode) and **TBN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





