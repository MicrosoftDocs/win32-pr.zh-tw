---
title: 'PBM_STEPIT 訊息 (Commctrl .h) '
description: 將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。 應用程式會藉由傳送 PBM SETSTEP 訊息來設定步驟增量 \_ 。
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934716"
---
# <a name="pbm_stepit-message"></a><span data-ttu-id="10b9f-105">PBM \_ STEPIT 訊息</span><span class="sxs-lookup"><span data-stu-id="10b9f-105">PBM\_STEPIT message</span></span>

<span data-ttu-id="10b9f-106">將進度列的目前位置往前移，並重新繪製橫條以反映新的位置。</span><span class="sxs-lookup"><span data-stu-id="10b9f-106">Advances the current position for a progress bar by the step increment and redraws the bar to reflect the new position.</span></span> <span data-ttu-id="10b9f-107">應用程式會藉由傳送 [**PBM \_ SETSTEP**](pbm-setstep.md) 訊息來設定步驟增量。</span><span class="sxs-lookup"><span data-stu-id="10b9f-107">An application sets the step increment by sending the [**PBM\_SETSTEP**](pbm-setstep.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="10b9f-108">參數</span><span class="sxs-lookup"><span data-stu-id="10b9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b9f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10b9f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="10b9f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="10b9f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="10b9f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b9f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10b9f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="10b9f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b9f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="10b9f-113">Return value</span></span>

<span data-ttu-id="10b9f-114">傳回先前的位置。</span><span class="sxs-lookup"><span data-stu-id="10b9f-114">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b9f-115">備註</span><span class="sxs-lookup"><span data-stu-id="10b9f-115">Remarks</span></span>

<span data-ttu-id="10b9f-116">當位置超過最大範圍值時，此訊息會重設目前的位置，使進度指示器會從頭開始。</span><span class="sxs-lookup"><span data-stu-id="10b9f-116">When the position exceeds the maximum range value, this message resets the current position so that the progress indicator starts over again from the beginning.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b9f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="10b9f-117">Requirements</span></span>



| <span data-ttu-id="10b9f-118">需求</span><span class="sxs-lookup"><span data-stu-id="10b9f-118">Requirement</span></span> | <span data-ttu-id="10b9f-119">值</span><span class="sxs-lookup"><span data-stu-id="10b9f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b9f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10b9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10b9f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10b9f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b9f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10b9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10b9f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10b9f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b9f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="10b9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b9f-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="10b9f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





