---
title: 'TB_HIDEBUTTON 訊息 (Commctrl .h) '
description: 在工具列中隱藏或顯示指定的按鈕。
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- TB_HIDEBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934196"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="0cf8f-104">TB \_ HIDEBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="0cf8f-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="0cf8f-105">在工具列中隱藏或顯示指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cf8f-106">參數</span><span class="sxs-lookup"><span data-stu-id="0cf8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf8f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cf8f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf8f-108">要隱藏或顯示之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="0cf8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cf8f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf8f-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要隱藏或顯示指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="0cf8f-111">若 **為 TRUE**，則會隱藏按鈕。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="0cf8f-112">如果 **為 FALSE**，則會顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="0cf8f-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf8f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cf8f-114">Return value</span></span>

<span data-ttu-id="0cf8f-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0cf8f-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf8f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cf8f-116">Requirements</span></span>



| <span data-ttu-id="0cf8f-117">需求</span><span class="sxs-lookup"><span data-stu-id="0cf8f-117">Requirement</span></span> | <span data-ttu-id="0cf8f-118">值</span><span class="sxs-lookup"><span data-stu-id="0cf8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf8f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cf8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf8f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cf8f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cf8f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cf8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf8f-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cf8f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cf8f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0cf8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cf8f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cf8f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

