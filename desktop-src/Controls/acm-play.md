---
title: 'ACM_PLAY 訊息 (Commctrl .h) '
description: 在動畫控制項中播放 AVI 剪輯。 當執行緒繼續執行時，控制項會在背景中播放剪輯。 您可以明確地傳送此訊息，或使用動畫 \_ 播放宏。
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- ACM_PLAY message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464669"
---
# <a name="acm_play-message"></a><span data-ttu-id="babcc-106">未通過的 \_ 播放訊息</span><span class="sxs-lookup"><span data-stu-id="babcc-106">ACM\_PLAY message</span></span>

<span data-ttu-id="babcc-107">在動畫控制項中播放 AVI 剪輯。</span><span class="sxs-lookup"><span data-stu-id="babcc-107">Plays an AVI clip in an animation control.</span></span> <span data-ttu-id="babcc-108">當執行緒繼續執行時，控制項會在背景中播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="babcc-108">The control plays the clip in the background while the thread continues executing.</span></span> <span data-ttu-id="babcc-109">您可以明確地傳送此訊息，或使用 [**動畫 \_ 播放**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) 宏。</span><span class="sxs-lookup"><span data-stu-id="babcc-109">You can send this message explicitly or by using the [**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="babcc-110">參數</span><span class="sxs-lookup"><span data-stu-id="babcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="babcc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="babcc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babcc-112">指定重播 AVI 剪輯次數的 **UINT** 。</span><span class="sxs-lookup"><span data-stu-id="babcc-112">A **UINT** that specifies the number of times to replay the AVI clip.</span></span> <span data-ttu-id="babcc-113">-1 值表示無限期地重新播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="babcc-113">A value of -1 means replay the clip indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="babcc-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="babcc-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="babcc-115">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是開始播放之框架的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="babcc-115">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the zero-based index of the frame where playing begins.</span></span> <span data-ttu-id="babcc-116">值必須小於65536。</span><span class="sxs-lookup"><span data-stu-id="babcc-116">The value must be less than 65,536.</span></span> <span data-ttu-id="babcc-117">值為零表示以 AVI 剪輯中的第一個框架為開頭。</span><span class="sxs-lookup"><span data-stu-id="babcc-117">A value of zero means begin with the first frame in the AVI clip.</span></span>

<span data-ttu-id="babcc-118">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是播放結束之框架的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="babcc-118">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the zero-based index of the frame where playing ends.</span></span> <span data-ttu-id="babcc-119">值必須小於65536。</span><span class="sxs-lookup"><span data-stu-id="babcc-119">The value must be less than 65,536.</span></span> <span data-ttu-id="babcc-120">值-1 表示以 AVI 剪輯中的最後一個框架結尾。</span><span class="sxs-lookup"><span data-stu-id="babcc-120">A value of -1 means end with the last frame in the AVI clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="babcc-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="babcc-121">Return value</span></span>

<span data-ttu-id="babcc-122">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="babcc-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="babcc-123">備註</span><span class="sxs-lookup"><span data-stu-id="babcc-123">Remarks</span></span>

<span data-ttu-id="babcc-124">您可以使用 [**動畫 \_ 搜尋**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) 來指示動畫控制項，以顯示 AVI 剪輯的特定框架。</span><span class="sxs-lookup"><span data-stu-id="babcc-124">You can use [**Animate\_Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) to direct the animation control to display a particular frame of the AVI clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="babcc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="babcc-125">Requirements</span></span>



| <span data-ttu-id="babcc-126">需求</span><span class="sxs-lookup"><span data-stu-id="babcc-126">Requirement</span></span> | <span data-ttu-id="babcc-127">值</span><span class="sxs-lookup"><span data-stu-id="babcc-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="babcc-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="babcc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="babcc-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="babcc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="babcc-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="babcc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="babcc-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="babcc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="babcc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="babcc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="babcc-133"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="babcc-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

