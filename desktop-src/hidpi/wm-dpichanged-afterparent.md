---
title: 'WM_DPICHANGED_AFTERPARENT 訊息 (Winuser .h) '
description: '針對每個監視器 v2 的最上層視窗，此訊息會傳送至正在進行 DPI 變更之視窗的子 HWDN 樹狀目錄中的所有 Hwnd。 |WM_DPICHANGED_AFTERPARENT 訊息 (Winuser .h) '
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989172"
---
# <a name="wm_dpichanged_afterparent-message"></a><span data-ttu-id="7fd53-105">WM \_ DPICHANGED \_ AFTERPARENT 訊息</span><span class="sxs-lookup"><span data-stu-id="7fd53-105">WM\_DPICHANGED\_AFTERPARENT message</span></span>

<span data-ttu-id="7fd53-106">針對 [每個監視器 v2](dpi-awareness-context.md) 的最上層視窗，此訊息會傳送至正在進行 DPI 變更之視窗的子 HWDN 樹狀目錄中的所有 hwnd。</span><span class="sxs-lookup"><span data-stu-id="7fd53-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="7fd53-107">這則訊息會在最上層視窗接收到 [**WM \_ DPICHANGED**](wm-dpichanged.md)之後發生，並從上往下往下遍歷子樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="7fd53-107">This message occurs after the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the top down.</span></span>


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a><span data-ttu-id="7fd53-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fd53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fd53-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fd53-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd53-110">此值未使用且將為零。</span><span class="sxs-lookup"><span data-stu-id="7fd53-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7fd53-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fd53-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fd53-112">此值未使用且將為零。</span><span class="sxs-lookup"><span data-stu-id="7fd53-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fd53-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fd53-113">Return value</span></span>

<span data-ttu-id="7fd53-114">系統不會使用並忽略此值。</span><span class="sxs-lookup"><span data-stu-id="7fd53-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd53-115">備註</span><span class="sxs-lookup"><span data-stu-id="7fd53-115">Remarks</span></span>

<span data-ttu-id="7fd53-116">在 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)中沒有這則訊息的預設處理方式。</span><span class="sxs-lookup"><span data-stu-id="7fd53-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="7fd53-117">只有在最上層視窗具有 PMv2 的 DPI 感知內容時，才會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="7fd53-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd53-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fd53-118">Requirements</span></span>



| <span data-ttu-id="7fd53-119">需求</span><span class="sxs-lookup"><span data-stu-id="7fd53-119">Requirement</span></span> | <span data-ttu-id="7fd53-120">值</span><span class="sxs-lookup"><span data-stu-id="7fd53-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd53-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fd53-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd53-122">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fd53-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7fd53-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fd53-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd53-124">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fd53-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7fd53-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7fd53-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fd53-126"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fd53-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd53-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fd53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd53-128">**WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="7fd53-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="7fd53-129">**WM \_ DPICHANGED \_ BEFOREPARENT**</span><span class="sxs-lookup"><span data-stu-id="7fd53-129">**WM\_DPICHANGED\_BEFOREPARENT**</span></span>](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

