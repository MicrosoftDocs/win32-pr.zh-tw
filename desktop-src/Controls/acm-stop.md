---
title: 'ACM_STOP 訊息 (Commctrl .h) '
description: 停止在動畫控制項中播放 AVI 剪輯。 您可以明確地傳送此訊息，或使用動畫 \_ 停用宏來傳送。
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- ACM_STOP message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094087"
---
# <a name="acm_stop-message"></a><span data-ttu-id="6e56b-105">未通過的 \_ 停止訊息</span><span class="sxs-lookup"><span data-stu-id="6e56b-105">ACM\_STOP message</span></span>

<span data-ttu-id="6e56b-106">停止在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="6e56b-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="6e56b-107">您可以明確地傳送此訊息，或使用 [**動畫 \_ 停**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) 用宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6e56b-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e56b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e56b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e56b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e56b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e56b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6e56b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e56b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e56b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6e56b-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6e56b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e56b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e56b-113">Return value</span></span>

<span data-ttu-id="6e56b-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="6e56b-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e56b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e56b-115">Requirements</span></span>



| <span data-ttu-id="6e56b-116">需求</span><span class="sxs-lookup"><span data-stu-id="6e56b-116">Requirement</span></span> | <span data-ttu-id="6e56b-117">值</span><span class="sxs-lookup"><span data-stu-id="6e56b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e56b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e56b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e56b-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e56b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e56b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e56b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e56b-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e56b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e56b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6e56b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e56b-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e56b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





