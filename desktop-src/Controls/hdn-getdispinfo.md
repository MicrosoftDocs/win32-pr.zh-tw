---
title: 'HDN_GETDISPINFO (Commctrl 的通知碼) '
description: 當控制項需要回呼標頭專案的相關資訊時，傳送至標題控制項的擁有者。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024669"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="87b2c-105">HDN \_ GETDISPINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="87b2c-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="87b2c-106">當控制項需要回呼標頭專案的相關資訊時，傳送至標題控制項的擁有者。</span><span class="sxs-lookup"><span data-stu-id="87b2c-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="87b2c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="87b2c-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="87b2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="87b2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b2c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87b2c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87b2c-110">[**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="87b2c-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="87b2c-111">在輸入時，結構的欄位會指定所需的資訊，以及感興趣的專案。</span><span class="sxs-lookup"><span data-stu-id="87b2c-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b2c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="87b2c-112">Return value</span></span>

<span data-ttu-id="87b2c-113">傳回 LRESULT。</span><span class="sxs-lookup"><span data-stu-id="87b2c-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b2c-114">備註</span><span class="sxs-lookup"><span data-stu-id="87b2c-114">Remarks</span></span>

<span data-ttu-id="87b2c-115">填入適當的結構成員，以將要求的資訊傳回至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="87b2c-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="87b2c-116">如果您的訊息處理常式將 [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa)結構的 **遮罩** 成員設定為 HDI \_ DI \_ SETITEM，則標頭控制項會儲存資訊，而不會再次要求它。</span><span class="sxs-lookup"><span data-stu-id="87b2c-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="87b2c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="87b2c-117">Requirements</span></span>



| <span data-ttu-id="87b2c-118">需求</span><span class="sxs-lookup"><span data-stu-id="87b2c-118">Requirement</span></span> | <span data-ttu-id="87b2c-119">值</span><span class="sxs-lookup"><span data-stu-id="87b2c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87b2c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87b2c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87b2c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87b2c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87b2c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87b2c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87b2c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87b2c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87b2c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="87b2c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87b2c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="87b2c-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="87b2c-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="87b2c-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87b2c-127">**HDN \_GETDISPINFOW** (Unicode) 和 **HDN \_ GETDISPINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="87b2c-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





