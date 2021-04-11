---
title: 'TTN_NEEDTEXT (Commctrl 的通知碼) '
description: 由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知碼與 TTN GETDISPINFO 相同 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104424"
---
# <a name="ttn_needtext-notification-code"></a><span data-ttu-id="fbb9a-106">TTN \_ NEEDTEXT 通知碼</span><span class="sxs-lookup"><span data-stu-id="fbb9a-106">TTN\_NEEDTEXT notification code</span></span>

<span data-ttu-id="fbb9a-107">由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-107">Sent by a tooltip control to retrieve information needed to display a tooltip window.</span></span> <span data-ttu-id="fbb9a-108">此通知碼與 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)相同。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-108">This notification code is identical to [TTN\_GETDISPINFO](ttn-getdispinfo.md).</span></span> <span data-ttu-id="fbb9a-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fbb9a-110">參數</span><span class="sxs-lookup"><span data-stu-id="fbb9a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb9a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbb9a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbb9a-112">[**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的指標，此結構會識別需要文字的工具，並接收要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-112">Pointer to an [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure that identifies the tool that needs text and receives the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb9a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb9a-113">Return value</span></span>

<span data-ttu-id="fbb9a-114">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbb9a-115">備註</span><span class="sxs-lookup"><span data-stu-id="fbb9a-115">Remarks</span></span>

<span data-ttu-id="fbb9a-116">填妥結構適當的成員，以將要求的資訊傳回給工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-116">Fill the structure's appropriate members to return the requested information to the tooltip control.</span></span> <span data-ttu-id="fbb9a-117">如果您的訊息處理常式將 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的 **uFlags** 成員設定為 TTF \_ DI \_ SETITEM，則工具提示控制項會儲存資訊，而不會再次要求它。</span><span class="sxs-lookup"><span data-stu-id="fbb9a-117">If your message handler sets the **uFlags** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure to TTF\_DI\_SETITEM, the tooltip control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb9a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb9a-118">Requirements</span></span>



| <span data-ttu-id="fbb9a-119">需求</span><span class="sxs-lookup"><span data-stu-id="fbb9a-119">Requirement</span></span> | <span data-ttu-id="fbb9a-120">值</span><span class="sxs-lookup"><span data-stu-id="fbb9a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb9a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbb9a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb9a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb9a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbb9a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbb9a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb9a-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb9a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbb9a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fbb9a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb9a-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb9a-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fbb9a-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="fbb9a-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fbb9a-128">**TTN \_NEEDTEXTW** (Unicode) 和 **TTN \_ NEEDTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="fbb9a-128">**TTN\_NEEDTEXTW** (Unicode) and **TTN\_NEEDTEXTA** (ANSI)</span></span><br/>                 |



 

 





