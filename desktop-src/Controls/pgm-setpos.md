---
title: 'PGM_SETPOS 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetPos 宏。
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685838"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="c3c5d-105">PGM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="c3c5d-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="c3c5d-106">設定呼機控制項目前的滾動位置。</span><span class="sxs-lookup"><span data-stu-id="c3c5d-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="c3c5d-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) 宏。</span><span class="sxs-lookup"><span data-stu-id="c3c5d-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3c5d-108">參數</span><span class="sxs-lookup"><span data-stu-id="c3c5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3c5d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3c5d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c3c5d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3c5d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3c5d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3c5d-112">**Int** 類型的值，其中包含新的捲軸位置（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c3c5d-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c5d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3c5d-113">Return value</span></span>

<span data-ttu-id="c3c5d-114">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3c5d-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c5d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3c5d-115">Requirements</span></span>



| <span data-ttu-id="c3c5d-116">需求</span><span class="sxs-lookup"><span data-stu-id="c3c5d-116">Requirement</span></span> | <span data-ttu-id="c3c5d-117">值</span><span class="sxs-lookup"><span data-stu-id="c3c5d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c5d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3c5d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c5d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3c5d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3c5d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3c5d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c5d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3c5d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3c5d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c3c5d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c5d-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c5d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





