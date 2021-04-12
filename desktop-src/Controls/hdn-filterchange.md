---
title: 'HDN_FILTERCHANGE (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，標題控制項篩選的屬性正在變更或編輯。 此通知碼以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464416"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="1cbe2-105">HDN \_ FILTERCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="1cbe2-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="1cbe2-106">通知標題控制項的父視窗，標題控制項篩選的屬性正在變更或編輯。</span><span class="sxs-lookup"><span data-stu-id="1cbe2-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="1cbe2-107">此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1cbe2-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1cbe2-108">參數</span><span class="sxs-lookup"><span data-stu-id="1cbe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbe2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cbe2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cbe2-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項和標頭專案的相關資訊，包括即將變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="1cbe2-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cbe2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cbe2-111">Return value</span></span>

<span data-ttu-id="1cbe2-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1cbe2-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbe2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cbe2-113">Requirements</span></span>



| <span data-ttu-id="1cbe2-114">需求</span><span class="sxs-lookup"><span data-stu-id="1cbe2-114">Requirement</span></span> | <span data-ttu-id="1cbe2-115">值</span><span class="sxs-lookup"><span data-stu-id="1cbe2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbe2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cbe2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbe2-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cbe2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cbe2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cbe2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbe2-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cbe2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cbe2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1cbe2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cbe2-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbe2-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbe2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cbe2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbe2-123">**HDM \_ SETFILTERCHANGETIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="1cbe2-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





