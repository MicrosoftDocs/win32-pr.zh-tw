---
title: 'RB_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的預設背景色彩。
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968173"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="49d7e-104">RB \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="49d7e-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="49d7e-105">設定 Rebar 控制項的預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="49d7e-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="49d7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="49d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d7e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49d7e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="49d7e-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="49d7e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="49d7e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49d7e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49d7e-110">[**COLORREF**](/windows/desktop/gdi/colorref) 值，表示新的預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="49d7e-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d7e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="49d7e-111">Return value</span></span>

<span data-ttu-id="49d7e-112">傳回代表先前預設背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="49d7e-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d7e-113">備註</span><span class="sxs-lookup"><span data-stu-id="49d7e-113">Remarks</span></span>

<span data-ttu-id="49d7e-114">Rebar 控制項的預設背景色彩用來繪製 Rebar 控制項中的背景，以及在傳送此訊息之後加入的所有群組。</span><span class="sxs-lookup"><span data-stu-id="49d7e-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="49d7e-115">藉由在 \_ **fMask** 中設定 RBBIM 色彩旗標，並在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構中設定 **clrBack** ，即可覆寫特定頻外的預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="49d7e-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="49d7e-116">啟用視覺化樣式時，此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="49d7e-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d7e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="49d7e-117">Requirements</span></span>



| <span data-ttu-id="49d7e-118">需求</span><span class="sxs-lookup"><span data-stu-id="49d7e-118">Requirement</span></span> | <span data-ttu-id="49d7e-119">值</span><span class="sxs-lookup"><span data-stu-id="49d7e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49d7e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49d7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49d7e-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49d7e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49d7e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49d7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49d7e-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49d7e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49d7e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="49d7e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49d7e-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="49d7e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d7e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49d7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d7e-127">**RB \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="49d7e-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

