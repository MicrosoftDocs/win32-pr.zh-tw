---
title: 'TDM_SET_PROGRESS_BAR_STATE 訊息 (Commctrl .h) '
description: 在工作對話方塊中設定進度列的狀態。
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/08/2021
ms.locfileid: "104321791"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="a31e6-104">TDM \_ 設定 \_ 進度 \_ 列 \_ 狀態訊息</span><span class="sxs-lookup"><span data-stu-id="a31e6-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="a31e6-105">在工作對話方塊中設定進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="a31e6-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="a31e6-106">參數</span><span class="sxs-lookup"><span data-stu-id="a31e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a31e6-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a31e6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31e6-108">指定進度列狀態的 **int** 。</span><span class="sxs-lookup"><span data-stu-id="a31e6-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="a31e6-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a31e6-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a31e6-110">值</span><span class="sxs-lookup"><span data-stu-id="a31e6-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a31e6-111">意義</span><span class="sxs-lookup"><span data-stu-id="a31e6-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="a31e6-112"><dt>**PBST \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e6-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="a31e6-113">將進度列設定為正常狀態。</span><span class="sxs-lookup"><span data-stu-id="a31e6-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="a31e6-114"><dt>**PBST 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e6-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="a31e6-115">將進度列設定為暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="a31e6-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="a31e6-116"><dt>**PBST \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e6-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="a31e6-117">將進度列設定為錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="a31e6-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a31e6-118">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a31e6-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31e6-119">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a31e6-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31e6-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a31e6-120">Return value</span></span>

<span data-ttu-id="a31e6-121">如果函式成功，則傳回值為非零。</span><span class="sxs-lookup"><span data-stu-id="a31e6-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="a31e6-122">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="a31e6-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="a31e6-123">若要取得擴充的錯誤資訊，請呼叫 GetLastError。</span><span class="sxs-lookup"><span data-stu-id="a31e6-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31e6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a31e6-124">Requirements</span></span>



| <span data-ttu-id="a31e6-125">需求</span><span class="sxs-lookup"><span data-stu-id="a31e6-125">Requirement</span></span> | <span data-ttu-id="a31e6-126">值</span><span class="sxs-lookup"><span data-stu-id="a31e6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a31e6-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a31e6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a31e6-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31e6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a31e6-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a31e6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a31e6-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a31e6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a31e6-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a31e6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a31e6-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a31e6-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





