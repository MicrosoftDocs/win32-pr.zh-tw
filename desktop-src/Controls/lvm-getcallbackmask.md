---
title: 'LVM_GETCALLBACKMASK 訊息 (Commctrl .h) '
description: 取得清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 ListView \_ GetCallbackMask 宏來傳送。
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464281"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="7ecaa-105">LVM \_ GETCALLBACKMASK 訊息</span><span class="sxs-lookup"><span data-stu-id="7ecaa-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="7ecaa-106">取得清單視圖控制項的回呼遮罩。</span><span class="sxs-lookup"><span data-stu-id="7ecaa-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="7ecaa-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="7ecaa-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ecaa-108">參數</span><span class="sxs-lookup"><span data-stu-id="7ecaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ecaa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ecaa-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7ecaa-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7ecaa-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7ecaa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ecaa-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7ecaa-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7ecaa-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ecaa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ecaa-113">Return value</span></span>

<span data-ttu-id="7ecaa-114">傳回回呼遮罩。</span><span class="sxs-lookup"><span data-stu-id="7ecaa-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ecaa-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ecaa-115">Requirements</span></span>



| <span data-ttu-id="7ecaa-116">需求</span><span class="sxs-lookup"><span data-stu-id="7ecaa-116">Requirement</span></span> | <span data-ttu-id="7ecaa-117">值</span><span class="sxs-lookup"><span data-stu-id="7ecaa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecaa-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ecaa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ecaa-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ecaa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7ecaa-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ecaa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ecaa-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ecaa-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ecaa-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7ecaa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ecaa-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ecaa-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





