---
title: 'SB_GETTIPTEXT 訊息 (Commctrl .h) '
description: 抓取狀態列中某部分的工具提示文字。 您必須使用 SBT \_ 工具提示樣式來建立狀態列，才能啟用工具提示。
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844000"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="28e78-105">SB \_ GETTIPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="28e78-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="28e78-106">抓取狀態列中某部分的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="28e78-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="28e78-107">您必須使用 [**SBT \_ 工具提示**](status-bar-styles.md) 樣式來建立狀態列，才能啟用工具提示。</span><span class="sxs-lookup"><span data-stu-id="28e78-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="28e78-108">參數</span><span class="sxs-lookup"><span data-stu-id="28e78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28e78-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28e78-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定接收工具提示文字之部分的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="28e78-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="28e78-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定 *lParam* 的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="28e78-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="28e78-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28e78-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28e78-113">接收工具提示文字之字元緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="28e78-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e78-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="28e78-114">Return value</span></span>

<span data-ttu-id="28e78-115">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="28e78-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e78-116">備註</span><span class="sxs-lookup"><span data-stu-id="28e78-116">Remarks</span></span>

<span data-ttu-id="28e78-117">**安全性警告：** 不當使用此訊息可能會導致您的應用程式發生問題。</span><span class="sxs-lookup"><span data-stu-id="28e78-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="28e78-118">例如，如果文字對 *lParam* 緩衝區來說太大，可能會造成緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="28e78-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="28e78-119">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="28e78-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e78-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="28e78-120">Requirements</span></span>



| <span data-ttu-id="28e78-121">需求</span><span class="sxs-lookup"><span data-stu-id="28e78-121">Requirement</span></span> | <span data-ttu-id="28e78-122">值</span><span class="sxs-lookup"><span data-stu-id="28e78-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28e78-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28e78-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28e78-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28e78-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28e78-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28e78-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28e78-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28e78-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28e78-127">標頭</span><span class="sxs-lookup"><span data-stu-id="28e78-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e78-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="28e78-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="28e78-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="28e78-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28e78-130">**SB \_GETTIPTEXTW** (Unicode) 和 **SB \_ GETTIPTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="28e78-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

