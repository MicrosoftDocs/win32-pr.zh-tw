---
title: 'TDM_SET_PROGRESS_BAR_RANGE 訊息 (Commctrl .h) '
description: 在工作對話方塊中設定進度列的最小值和最大值。
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844364"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="5e8eb-104">TDM \_ 設定 \_ 進度 \_ 列 \_ 範圍訊息</span><span class="sxs-lookup"><span data-stu-id="5e8eb-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="5e8eb-105">在工作對話方塊中設定進度列的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e8eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8eb-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8eb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e8eb-109">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8eb-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小值。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="5e8eb-111">根據預設，最小值為零。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="5e8eb-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大值。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="5e8eb-113">根據預設，最大值為100。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8eb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e8eb-114">Return value</span></span>

<span data-ttu-id="5e8eb-115">如果成功，則傳回先前的最小值和最大值，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="5e8eb-116">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含最小值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含最大值。</span><span class="sxs-lookup"><span data-stu-id="5e8eb-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8eb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e8eb-117">Requirements</span></span>



| <span data-ttu-id="5e8eb-118">需求</span><span class="sxs-lookup"><span data-stu-id="5e8eb-118">Requirement</span></span> | <span data-ttu-id="5e8eb-119">值</span><span class="sxs-lookup"><span data-stu-id="5e8eb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8eb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e8eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8eb-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e8eb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e8eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8eb-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e8eb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e8eb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5e8eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8eb-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8eb-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

