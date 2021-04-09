---
title: 'TB_MARKBUTTON 訊息 (Commctrl .h) '
description: 在工具列控制項中設定指定按鈕的醒目提示狀態。
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025330"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="e4afb-104">TB \_ MARKBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="e4afb-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="e4afb-105">在工具列控制項中設定指定按鈕的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="e4afb-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4afb-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4afb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4afb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4afb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4afb-108">工具列按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4afb-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="e4afb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4afb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4afb-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，表示新的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="e4afb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="e4afb-111">若 **為 TRUE**，則會反白顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="e4afb-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="e4afb-112">如果 **為 FALSE**，則按鈕會設定為其預設狀態。</span><span class="sxs-lookup"><span data-stu-id="e4afb-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="e4afb-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="e4afb-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4afb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4afb-114">Return value</span></span>

<span data-ttu-id="e4afb-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="e4afb-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4afb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4afb-116">Requirements</span></span>



| <span data-ttu-id="e4afb-117">需求</span><span class="sxs-lookup"><span data-stu-id="e4afb-117">Requirement</span></span> | <span data-ttu-id="e4afb-118">值</span><span class="sxs-lookup"><span data-stu-id="e4afb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4afb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4afb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4afb-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4afb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4afb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4afb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4afb-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4afb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4afb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e4afb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4afb-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4afb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

