---
title: 'TB_PRESSBUTTON 訊息 (Commctrl .h) '
description: 在工具列中按下或放開指定的按鈕。
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105042"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="3cb4d-104">TB \_ PRESSBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="3cb4d-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="3cb4d-105">在工具列中按下或放開指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cb4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cb4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb4d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cb4d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb4d-108">要按或放開之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="3cb4d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cb4d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cb4d-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要按下或放開指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="3cb4d-111">若 **為 TRUE**，則會按下按鈕。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="3cb4d-112">如果 **為 FALSE**，則表示按鈕已釋放。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="3cb4d-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb4d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cb4d-114">Return value</span></span>

<span data-ttu-id="3cb4d-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3cb4d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb4d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cb4d-116">Requirements</span></span>



| <span data-ttu-id="3cb4d-117">需求</span><span class="sxs-lookup"><span data-stu-id="3cb4d-117">Requirement</span></span> | <span data-ttu-id="3cb4d-118">值</span><span class="sxs-lookup"><span data-stu-id="3cb4d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb4d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cb4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb4d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cb4d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cb4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb4d-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cb4d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cb4d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3cb4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb4d-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb4d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

