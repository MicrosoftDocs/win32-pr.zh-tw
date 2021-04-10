---
title: 'LVM_GETTEXTBKCOLOR 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的文字背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ GetTextBkColor 宏來傳送。
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- LVM_GETTEXTBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934893"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="f3a74-105">LVM \_ GETTEXTBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="f3a74-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="f3a74-106">抓取清單視圖控制項的文字背景色彩。</span><span class="sxs-lookup"><span data-stu-id="f3a74-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="f3a74-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="f3a74-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3a74-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3a74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3a74-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f3a74-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3a74-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f3a74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3a74-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f3a74-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3a74-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3a74-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3a74-113">Return value</span></span>

<span data-ttu-id="f3a74-114">傳回文字的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="f3a74-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a74-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3a74-115">Requirements</span></span>



| <span data-ttu-id="f3a74-116">需求</span><span class="sxs-lookup"><span data-stu-id="f3a74-116">Requirement</span></span> | <span data-ttu-id="f3a74-117">值</span><span class="sxs-lookup"><span data-stu-id="f3a74-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a74-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3a74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a74-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a74-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3a74-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3a74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a74-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3a74-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3a74-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f3a74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3a74-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3a74-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





