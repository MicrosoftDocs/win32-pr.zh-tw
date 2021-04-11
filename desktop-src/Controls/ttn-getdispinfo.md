---
title: 'TTN_GETDISPINFO (Commctrl 的通知碼) '
description: 由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843880"
---
# <a name="ttn_getdispinfo-notification-code"></a><span data-ttu-id="7409c-105">TTN \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="7409c-105">TTN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="7409c-106">由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7409c-106">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="7409c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7409c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7409c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7409c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7409c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7409c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7409c-110">[**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的指標，此結構會識別需要文字的工具，並接收要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="7409c-110">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7409c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7409c-111">Return value</span></span>

<span data-ttu-id="7409c-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="7409c-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7409c-113">備註</span><span class="sxs-lookup"><span data-stu-id="7409c-113">Remarks</span></span>

<span data-ttu-id="7409c-114">填妥結構適當的成員，以將要求的資訊傳回給工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="7409c-114">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="7409c-115">如果您的訊息處理常式將 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的 **uFlags** 成員設定為 TTF \_ DI \_ SETITEM，則工具提示控制項會儲存資訊，而不會再次要求它。</span><span class="sxs-lookup"><span data-stu-id="7409c-115">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="7409c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7409c-116">Requirements</span></span>



| <span data-ttu-id="7409c-117">需求</span><span class="sxs-lookup"><span data-stu-id="7409c-117">Requirement</span></span> | <span data-ttu-id="7409c-118">值</span><span class="sxs-lookup"><span data-stu-id="7409c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7409c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7409c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7409c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7409c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7409c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7409c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7409c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7409c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7409c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7409c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7409c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7409c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7409c-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7409c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7409c-126">**TTN \_GETDISPINFOW** (Unicode) 和 **TTN \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7409c-126">**TTN\_GETDISPINFOW** (Unicode) and **TTN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





