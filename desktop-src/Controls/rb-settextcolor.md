---
title: 'RB_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的預設文字色彩。
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466069"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="05b84-104">RB \_ SETTEXTCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="05b84-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="05b84-105">設定 Rebar 控制項的預設文字色彩。</span><span class="sxs-lookup"><span data-stu-id="05b84-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="05b84-106">參數</span><span class="sxs-lookup"><span data-stu-id="05b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05b84-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="05b84-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="05b84-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="05b84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05b84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05b84-110">[**COLORREF**](/windows/desktop/gdi/colorref) 值，表示新的預設文字色彩。</span><span class="sxs-lookup"><span data-stu-id="05b84-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b84-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="05b84-111">Return value</span></span>

<span data-ttu-id="05b84-112">傳回代表先前預設文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="05b84-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b84-113">備註</span><span class="sxs-lookup"><span data-stu-id="05b84-113">Remarks</span></span>

<span data-ttu-id="05b84-114">Rebar 控制項的預設文字色彩用來繪製 Rebar 控制項中的文字，以及在傳送此訊息之後加入的所有群組。</span><span class="sxs-lookup"><span data-stu-id="05b84-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="05b84-115">藉由在 \_ **fMask** 中設定 RBBIM 色彩旗標，並在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構中設定 **clrBack** ，即可覆寫特定頻外的預設文字色彩。</span><span class="sxs-lookup"><span data-stu-id="05b84-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b84-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="05b84-116">Requirements</span></span>



| <span data-ttu-id="05b84-117">需求</span><span class="sxs-lookup"><span data-stu-id="05b84-117">Requirement</span></span> | <span data-ttu-id="05b84-118">值</span><span class="sxs-lookup"><span data-stu-id="05b84-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05b84-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05b84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05b84-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05b84-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05b84-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05b84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05b84-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05b84-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05b84-123">標頭</span><span class="sxs-lookup"><span data-stu-id="05b84-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b84-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="05b84-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b84-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05b84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b84-126">**RB \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="05b84-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

