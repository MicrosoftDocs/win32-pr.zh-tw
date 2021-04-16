---
title: 'CBEN_GETDISPINFO (Commctrl 的通知碼) '
description: 傳送以取得回呼專案的顯示資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508312"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="6c8e7-105">CBEN \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="6c8e7-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="6c8e7-106">傳送以取得回呼專案的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="6c8e7-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c8e7-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c8e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c8e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8e7-110">[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8e7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c8e7-111">Return value</span></span>

<span data-ttu-id="6c8e7-112">處理此通知程式碼的應用程式必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8e7-113">備註</span><span class="sxs-lookup"><span data-stu-id="6c8e7-113">Remarks</span></span>

<span data-ttu-id="6c8e7-114">[**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa)結構包含 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="6c8e7-115">**遮罩** 成員會指定控制項所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="6c8e7-116">填入適當的結構成員，以將要求的資訊傳回給控制項。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="6c8e7-117">如果您的訊息處理常式將 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **遮罩** 成員設定為 CBEIF \_ DI \_ SETITEM，則該控制項會儲存資訊，而且不會再次要求它。</span><span class="sxs-lookup"><span data-stu-id="6c8e7-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8e7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c8e7-118">Requirements</span></span>



| <span data-ttu-id="6c8e7-119">需求</span><span class="sxs-lookup"><span data-stu-id="6c8e7-119">Requirement</span></span> | <span data-ttu-id="6c8e7-120">值</span><span class="sxs-lookup"><span data-stu-id="6c8e7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8e7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c8e7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8e7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8e7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c8e7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c8e7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8e7-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8e7-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c8e7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6c8e7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8e7-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8e7-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6c8e7-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6c8e7-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c8e7-128">**CBEN \_GETDISPINFOW** (Unicode) 和 **CBEN \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6c8e7-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





