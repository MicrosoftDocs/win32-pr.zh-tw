---
title: 'PGM_SETCHILD 訊息 (Commctrl .h) '
description: 設定呼機控制項的包含視窗。
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094424"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="6deb7-104">PGM \_ SETCHILD 訊息</span><span class="sxs-lookup"><span data-stu-id="6deb7-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="6deb7-105">設定呼機控制項的包含視窗。</span><span class="sxs-lookup"><span data-stu-id="6deb7-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="6deb7-106">此訊息不會變更包含視窗的父系;它只會將視窗控制碼指派給呼機控制項以供滾動。</span><span class="sxs-lookup"><span data-stu-id="6deb7-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="6deb7-107">在大部分的情況下，包含的視窗將會是子視窗。</span><span class="sxs-lookup"><span data-stu-id="6deb7-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="6deb7-108">如果是這種情況，則包含的視窗應該是呼機控制項的子系。</span><span class="sxs-lookup"><span data-stu-id="6deb7-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="6deb7-109">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) 宏。</span><span class="sxs-lookup"><span data-stu-id="6deb7-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6deb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="6deb7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6deb7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6deb7-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6deb7-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6deb7-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6deb7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6deb7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6deb7-114">要包含的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="6deb7-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6deb7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6deb7-115">Return value</span></span>

<span data-ttu-id="6deb7-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="6deb7-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6deb7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6deb7-117">Requirements</span></span>



| <span data-ttu-id="6deb7-118">需求</span><span class="sxs-lookup"><span data-stu-id="6deb7-118">Requirement</span></span> | <span data-ttu-id="6deb7-119">值</span><span class="sxs-lookup"><span data-stu-id="6deb7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6deb7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6deb7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6deb7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6deb7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6deb7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6deb7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6deb7-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6deb7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6deb7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6deb7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6deb7-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6deb7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





