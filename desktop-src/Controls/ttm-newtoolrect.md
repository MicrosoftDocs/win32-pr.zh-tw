---
title: 'TTM_NEWTOOLRECT 訊息 (Commctrl .h) '
description: 設定工具的新周框矩形。
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465349"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="5e0c9-104">TTM \_ NEWTOOLRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="5e0c9-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="5e0c9-105">設定工具的新周框矩形。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e0c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e0c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e0c9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e0c9-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e0c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e0c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e0c9-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="5e0c9-111">**Hwnd** 和 **uId** 成員會識別工具，而 **rect** 成員會指定新的周框。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="5e0c9-112">傳送此訊息之前，必須先填入此結構的 **cbSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0c9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e0c9-113">Return value</span></span>

<span data-ttu-id="5e0c9-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5e0c9-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0c9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e0c9-115">Requirements</span></span>



| <span data-ttu-id="5e0c9-116">需求</span><span class="sxs-lookup"><span data-stu-id="5e0c9-116">Requirement</span></span> | <span data-ttu-id="5e0c9-117">值</span><span class="sxs-lookup"><span data-stu-id="5e0c9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0c9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e0c9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0c9-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e0c9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e0c9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e0c9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0c9-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e0c9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e0c9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5e0c9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e0c9-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e0c9-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5e0c9-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5e0c9-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5e0c9-125">**TTM \_NEWTOOLRECTW** (Unicode) 和 **TTM \_ NEWTOOLRECTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5e0c9-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





