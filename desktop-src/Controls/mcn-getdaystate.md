---
title: 'MCN_GETDAYSTATE (Commctrl 的通知碼) '
description: 由月曆控制項傳送，可要求有關如何顯示個別日期的資訊。 此通知碼只會由使用 MCS DAYSTATE 樣式的月曆控制項來傳送 \_ ，而且會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685955"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="403e7-105">MCN \_ GETDAYSTATE 通知碼</span><span class="sxs-lookup"><span data-stu-id="403e7-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="403e7-106">由月曆控制項傳送，可要求有關如何顯示個別日期的資訊。</span><span class="sxs-lookup"><span data-stu-id="403e7-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="403e7-107">此通知碼只會由使用 [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) 樣式的月曆控制項來傳送，而且會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="403e7-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="403e7-108">參數</span><span class="sxs-lookup"><span data-stu-id="403e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403e7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="403e7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="403e7-110">[**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="403e7-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="403e7-111">結構包含控制項需要資訊之時間範圍的相關資訊，並且會接收提供此資料的陣列位址。</span><span class="sxs-lookup"><span data-stu-id="403e7-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403e7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="403e7-112">Return value</span></span>

<span data-ttu-id="403e7-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="403e7-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="403e7-114">備註</span><span class="sxs-lookup"><span data-stu-id="403e7-114">Remarks</span></span>

<span data-ttu-id="403e7-115">處理此通知碼可讓您的應用程式藉由指定以粗體顯示特定日期，來自訂其顯示。</span><span class="sxs-lookup"><span data-stu-id="403e7-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="403e7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="403e7-116">Requirements</span></span>



| <span data-ttu-id="403e7-117">需求</span><span class="sxs-lookup"><span data-stu-id="403e7-117">Requirement</span></span> | <span data-ttu-id="403e7-118">值</span><span class="sxs-lookup"><span data-stu-id="403e7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="403e7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="403e7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="403e7-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="403e7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="403e7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="403e7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="403e7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="403e7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="403e7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="403e7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="403e7-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="403e7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





