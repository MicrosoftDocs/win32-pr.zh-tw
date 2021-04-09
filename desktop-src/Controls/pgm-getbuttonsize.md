---
title: 'PGM_GETBUTTONSIZE 訊息 (Commctrl .h) '
description: 抓取頁面導航控制項目前的按鈕大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetButtonSize 宏。
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025285"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="93f8b-105">PGM \_ GETBUTTONSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="93f8b-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="93f8b-106">抓取頁面導航控制項目前的按鈕大小。</span><span class="sxs-lookup"><span data-stu-id="93f8b-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="93f8b-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="93f8b-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="93f8b-108">參數</span><span class="sxs-lookup"><span data-stu-id="93f8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f8b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93f8b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="93f8b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="93f8b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="93f8b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93f8b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="93f8b-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="93f8b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f8b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="93f8b-113">Return value</span></span>

<span data-ttu-id="93f8b-114">傳回包含目前按鈕大小的 INT 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="93f8b-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f8b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="93f8b-115">Requirements</span></span>



| <span data-ttu-id="93f8b-116">需求</span><span class="sxs-lookup"><span data-stu-id="93f8b-116">Requirement</span></span> | <span data-ttu-id="93f8b-117">值</span><span class="sxs-lookup"><span data-stu-id="93f8b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93f8b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93f8b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="93f8b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93f8b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93f8b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93f8b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="93f8b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93f8b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93f8b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="93f8b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="93f8b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="93f8b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f8b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93f8b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f8b-125">**PGM \_ SETBUTTONSIZE**</span><span class="sxs-lookup"><span data-stu-id="93f8b-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





