---
title: 'TTM_GETDELAYTIME 訊息 (Commctrl .h) '
description: 抓取目前針對工具提示控制項設定的初始、快顯和 reshow 持續時間。
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967736"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="f3444-104">TTM \_ GETDELAYTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="f3444-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="f3444-105">抓取目前針對工具提示控制項設定的初始、快顯和 reshow 持續時間。</span><span class="sxs-lookup"><span data-stu-id="f3444-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3444-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3444-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3444-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3444-108">旗標，指定將取出的持續時間值。</span><span class="sxs-lookup"><span data-stu-id="f3444-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="f3444-109">這個參數的值可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="f3444-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="f3444-110">值</span><span class="sxs-lookup"><span data-stu-id="f3444-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="f3444-111">意義</span><span class="sxs-lookup"><span data-stu-id="f3444-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="f3444-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="f3444-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="f3444-113">如果指標在工具周框內是固定的，則取得工具提示視窗保持可見的時間量。</span><span class="sxs-lookup"><span data-stu-id="f3444-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="f3444-114"><dt>**TTDT \_ 初始**</dt></span><span class="sxs-lookup"><span data-stu-id="f3444-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="f3444-115">在出現工具提示視窗之前，取出指標在工具的周框中必須保持靜止的時間量。</span><span class="sxs-lookup"><span data-stu-id="f3444-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="f3444-116"><dt>**TTDT \_ RESHOW**</dt></span><span class="sxs-lookup"><span data-stu-id="f3444-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="f3444-117">取得當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間量。</span><span class="sxs-lookup"><span data-stu-id="f3444-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="f3444-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3444-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f3444-119">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3444-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3444-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3444-120">Return value</span></span>

<span data-ttu-id="f3444-121">使用指定的持續時間（以毫秒為單位）傳回和 INT 值。</span><span class="sxs-lookup"><span data-stu-id="f3444-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3444-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3444-122">Requirements</span></span>



| <span data-ttu-id="f3444-123">需求</span><span class="sxs-lookup"><span data-stu-id="f3444-123">Requirement</span></span> | <span data-ttu-id="f3444-124">值</span><span class="sxs-lookup"><span data-stu-id="f3444-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3444-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3444-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3444-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3444-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3444-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3444-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3444-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3444-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3444-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f3444-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3444-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3444-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3444-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3444-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3444-132">**TTM \_ SETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="f3444-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





