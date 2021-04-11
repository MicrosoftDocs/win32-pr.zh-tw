---
title: 'PBM_GETSTATE 訊息 (Commctrl .h) '
description: 取得進度列的狀態。
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934721"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="c203a-104">PBM \_ >getstate 訊息</span><span class="sxs-lookup"><span data-stu-id="c203a-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="c203a-105">取得進度列的狀態。</span><span class="sxs-lookup"><span data-stu-id="c203a-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c203a-106">參數</span><span class="sxs-lookup"><span data-stu-id="c203a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c203a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c203a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c203a-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c203a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c203a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c203a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c203a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c203a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c203a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c203a-111">Return value</span></span>

<span data-ttu-id="c203a-112">傳回進度列的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c203a-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="c203a-113">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c203a-113">One of the following values.</span></span>



| <span data-ttu-id="c203a-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c203a-114">Return code</span></span>                                                                                 | <span data-ttu-id="c203a-115">Description</span><span class="sxs-lookup"><span data-stu-id="c203a-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="c203a-116"><dt>**PBST \_ 正常**</dt></span><span class="sxs-lookup"><span data-stu-id="c203a-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="c203a-117">進行中。</span><span class="sxs-lookup"><span data-stu-id="c203a-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="c203a-118"><dt>**PBST \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="c203a-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="c203a-119">錯誤。</span><span class="sxs-lookup"><span data-stu-id="c203a-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="c203a-120"><dt>**PBST 已 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="c203a-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="c203a-121">已暫停。</span><span class="sxs-lookup"><span data-stu-id="c203a-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="c203a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c203a-122">Requirements</span></span>



| <span data-ttu-id="c203a-123">需求</span><span class="sxs-lookup"><span data-stu-id="c203a-123">Requirement</span></span> | <span data-ttu-id="c203a-124">值</span><span class="sxs-lookup"><span data-stu-id="c203a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c203a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c203a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c203a-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c203a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c203a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c203a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c203a-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c203a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c203a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c203a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c203a-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c203a-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





