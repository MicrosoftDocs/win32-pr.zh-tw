---
title: 'PGM_RECALCSIZE 訊息 (Commctrl .h) '
description: 強制呼機控制項重新計算包含視窗的大小。 傳送此訊息將會產生 PGN \_ CALCSIZE 通知。 您可以明確地傳送此訊息，或使用呼叫器 \_ RecalcSize 宏。
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465037"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="0cc9c-106">PGM \_ RECALCSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="0cc9c-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="0cc9c-107">強制呼機控制項重新計算包含視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="0cc9c-108">傳送此訊息將會產生 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="0cc9c-109">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cc9c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0cc9c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cc9c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cc9c-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0cc9c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0cc9c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cc9c-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0cc9c-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cc9c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cc9c-115">Return value</span></span>

<span data-ttu-id="0cc9c-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="0cc9c-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc9c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cc9c-117">Requirements</span></span>



| <span data-ttu-id="0cc9c-118">需求</span><span class="sxs-lookup"><span data-stu-id="0cc9c-118">Requirement</span></span> | <span data-ttu-id="0cc9c-119">值</span><span class="sxs-lookup"><span data-stu-id="0cc9c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc9c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cc9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc9c-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cc9c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cc9c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cc9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc9c-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cc9c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cc9c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0cc9c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc9c-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





