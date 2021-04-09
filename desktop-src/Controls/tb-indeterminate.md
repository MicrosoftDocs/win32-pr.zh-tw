---
title: 'TB_INDETERMINATE 訊息 (Commctrl .h) '
description: 在工具列中設定或清除指定之按鈕的不定狀態。
ms.assetid: 6a0f2b82-8241-4c2e-b349-606975ba1a24
keywords:
- TB_INDETERMINATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_INDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f1de35f9621de4f51d371bb50dbda637d720cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024921"
---
# <a name="tb_indeterminate-message"></a><span data-ttu-id="4f38b-104">TB \_ 不定訊息</span><span class="sxs-lookup"><span data-stu-id="4f38b-104">TB\_INDETERMINATE message</span></span>

<span data-ttu-id="4f38b-105">在工具列中設定或清除指定之按鈕的不定狀態。</span><span class="sxs-lookup"><span data-stu-id="4f38b-105">Sets or clears the indeterminate state of the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f38b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f38b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f38b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f38b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f38b-108">要設定或清除其不定狀態之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f38b-108">Command identifier of the button whose indeterminate state is to be set or cleared.</span></span>

</dd> <dt>

<span data-ttu-id="4f38b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f38b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f38b-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **布林** 值，指出是否要設定或清除不定狀態。</span><span class="sxs-lookup"><span data-stu-id="4f38b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to set or clear the indeterminate state.</span></span> <span data-ttu-id="4f38b-111">若 **為 TRUE**，則會設定不定狀態。</span><span class="sxs-lookup"><span data-stu-id="4f38b-111">If **TRUE**, the indeterminate state is set.</span></span> <span data-ttu-id="4f38b-112">如果 **為 FALSE**，則會清除狀態。</span><span class="sxs-lookup"><span data-stu-id="4f38b-112">If **FALSE**, the state is cleared.</span></span>

<span data-ttu-id="4f38b-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="4f38b-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f38b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f38b-114">Return value</span></span>

<span data-ttu-id="4f38b-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4f38b-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f38b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f38b-116">Requirements</span></span>



| <span data-ttu-id="4f38b-117">需求</span><span class="sxs-lookup"><span data-stu-id="4f38b-117">Requirement</span></span> | <span data-ttu-id="4f38b-118">值</span><span class="sxs-lookup"><span data-stu-id="4f38b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f38b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f38b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f38b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f38b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f38b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f38b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f38b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f38b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f38b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4f38b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f38b-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f38b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

