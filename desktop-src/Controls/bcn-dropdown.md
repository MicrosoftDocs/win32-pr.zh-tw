---
title: 'BCN_DROPDOWN (Winuser 的通知碼) '
description: 當使用者按一下按鈕上的下拉箭號時傳送。 控制項的父視窗會以 WM 通知訊息的形式接收此通知碼 \_ 。
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965292"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="3d91d-105">BCN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="3d91d-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="3d91d-106">當使用者按一下按鈕上的下拉箭號時傳送。</span><span class="sxs-lookup"><span data-stu-id="3d91d-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="3d91d-107">控制項的父視窗會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="3d91d-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3d91d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d91d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d91d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d91d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d91d-110">[**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3d91d-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="3d91d-111">**RcButton** 成員會設定為描述下拉式區域。</span><span class="sxs-lookup"><span data-stu-id="3d91d-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d91d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d91d-112">Return value</span></span>

<span data-ttu-id="3d91d-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3d91d-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d91d-114">備註</span><span class="sxs-lookup"><span data-stu-id="3d91d-114">Remarks</span></span>

<span data-ttu-id="3d91d-115">通知接收者會轉換 **LPARAM** 來取出 [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) 結構。</span><span class="sxs-lookup"><span data-stu-id="3d91d-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="3d91d-116">**WPARAM** 包含傳送此訊息之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d91d-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="3d91d-117">按鈕控制項必須要有下拉式按鈕樣式。</span><span class="sxs-lookup"><span data-stu-id="3d91d-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d91d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d91d-118">Requirements</span></span>



| <span data-ttu-id="3d91d-119">需求</span><span class="sxs-lookup"><span data-stu-id="3d91d-119">Requirement</span></span> | <span data-ttu-id="3d91d-120">值</span><span class="sxs-lookup"><span data-stu-id="3d91d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d91d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d91d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3d91d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d91d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d91d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d91d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3d91d-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d91d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d91d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3d91d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d91d-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3d91d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





