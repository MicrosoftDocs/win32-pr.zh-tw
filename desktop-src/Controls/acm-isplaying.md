---
title: 'ACM_ISPLAYING 訊息 (Commctrl .h) '
description: 檢查 Audio-Video 交錯 (AVI) 剪輯是否現正播放。 您可以明確地傳送此訊息，或使用動畫 \_ >isplaying 宏。
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024805"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="c1e8f-105">\_>isplaying 訊息</span><span class="sxs-lookup"><span data-stu-id="c1e8f-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="c1e8f-106">檢查 Audio-Video 交錯 (AVI) 剪輯是否現正播放。</span><span class="sxs-lookup"><span data-stu-id="c1e8f-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="c1e8f-107">您可以明確地傳送此訊息，或使用 [**動畫 \_ >isplaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) 宏。</span><span class="sxs-lookup"><span data-stu-id="c1e8f-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1e8f-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1e8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1e8f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e8f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c1e8f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e8f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1e8f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e8f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c1e8f-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e8f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1e8f-113">Return value</span></span>

<span data-ttu-id="c1e8f-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="c1e8f-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e8f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1e8f-115">Requirements</span></span>



| <span data-ttu-id="c1e8f-116">需求</span><span class="sxs-lookup"><span data-stu-id="c1e8f-116">Requirement</span></span> | <span data-ttu-id="c1e8f-117">值</span><span class="sxs-lookup"><span data-stu-id="c1e8f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e8f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1e8f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e8f-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1e8f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1e8f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e8f-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1e8f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1e8f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c1e8f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e8f-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





