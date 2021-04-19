---
title: 'PGM_GETPOS 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetPos 宏。
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969184"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="2eece-105">PGM \_ GETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="2eece-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="2eece-106">抓取呼機控制項目前的滾動位置。</span><span class="sxs-lookup"><span data-stu-id="2eece-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="2eece-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) 宏。</span><span class="sxs-lookup"><span data-stu-id="2eece-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2eece-108">參數</span><span class="sxs-lookup"><span data-stu-id="2eece-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eece-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2eece-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2eece-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2eece-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2eece-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eece-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2eece-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2eece-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eece-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2eece-113">Return value</span></span>

<span data-ttu-id="2eece-114">傳回包含目前滾動位置的 INT 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2eece-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eece-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eece-115">Requirements</span></span>



| <span data-ttu-id="2eece-116">需求</span><span class="sxs-lookup"><span data-stu-id="2eece-116">Requirement</span></span> | <span data-ttu-id="2eece-117">值</span><span class="sxs-lookup"><span data-stu-id="2eece-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eece-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eece-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eece-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eece-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eece-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eece-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eece-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eece-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eece-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2eece-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eece-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eece-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





