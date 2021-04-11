---
title: 'EM_SETBKGNDCOLOR 訊息 (Richedit .h) '
description: EM \_ SETBKGNDCOLOR 訊息會設定 rich edit 控制項的背景色彩。
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- EM_SETBKGNDCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844132"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="aefb3-104">EM \_ SETBKGNDCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="aefb3-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="aefb3-105">**EM \_ SETBKGNDCOLOR** 訊息會設定 rich edit 控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="aefb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="aefb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aefb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefb3-108">指定是否使用系統色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="aefb3-109">如果此參數為非零值，則背景會設定為視窗背景系統色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="aefb3-110">否則，背景會設定為指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="aefb3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aefb3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aefb3-112">[**COLORREF**](/windows/desktop/gdi/colorref)結構，指定 *wParam* 為零時的色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="aefb3-113">若要產生 **COLORREF**，請使用 [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) 宏。</span><span class="sxs-lookup"><span data-stu-id="aefb3-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aefb3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aefb3-114">Return value</span></span>

<span data-ttu-id="aefb3-115">此訊息會傳回原始的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="aefb3-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefb3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="aefb3-116">Requirements</span></span>



| <span data-ttu-id="aefb3-117">需求</span><span class="sxs-lookup"><span data-stu-id="aefb3-117">Requirement</span></span> | <span data-ttu-id="aefb3-118">值</span><span class="sxs-lookup"><span data-stu-id="aefb3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aefb3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aefb3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aefb3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aefb3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aefb3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aefb3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aefb3-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aefb3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aefb3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="aefb3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aefb3-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="aefb3-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aefb3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aefb3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="aefb3-126">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="aefb3-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="aefb3-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="aefb3-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="aefb3-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="aefb3-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

