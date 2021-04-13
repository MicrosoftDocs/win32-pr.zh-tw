---
title: 'RB_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項的預設背景色彩。
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0c6f2348dfa54dc02ddc40658fd1289885ff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466080"
---
# <a name="rb_getbkcolor-message"></a><span data-ttu-id="9d304-104">RB \_ GETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="9d304-104">RB\_GETBKCOLOR message</span></span>

<span data-ttu-id="9d304-105">抓取 Rebar 控制項的預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="9d304-105">Retrieves a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d304-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d304-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d304-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d304-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9d304-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9d304-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9d304-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d304-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9d304-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9d304-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d304-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d304-111">Return value</span></span>

<span data-ttu-id="9d304-112">傳回代表目前預設背景色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="9d304-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represent the current default background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d304-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d304-113">Requirements</span></span>



| <span data-ttu-id="9d304-114">需求</span><span class="sxs-lookup"><span data-stu-id="9d304-114">Requirement</span></span> | <span data-ttu-id="9d304-115">值</span><span class="sxs-lookup"><span data-stu-id="9d304-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d304-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d304-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d304-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d304-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d304-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d304-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d304-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d304-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d304-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9d304-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d304-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d304-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d304-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d304-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d304-123">**RB \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9d304-123">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
</dt> </dl>

 

