---
title: 'TBM_SETTICFREQ 訊息 (Commctrl .h) '
description: 設定在 [標記] 中刻度的間隔頻率。
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024846"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="2eafa-104">TBM \_ SETTICFREQ 訊息</span><span class="sxs-lookup"><span data-stu-id="2eafa-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="2eafa-105">設定在 [標記] 中刻度的間隔頻率。</span><span class="sxs-lookup"><span data-stu-id="2eafa-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="2eafa-106">例如，如果 [頻率] 設定為 [二]，則會在 [顯示區] 範圍中顯示每個其他增量的刻度。</span><span class="sxs-lookup"><span data-stu-id="2eafa-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="2eafa-107">頻率的預設設定為 1;亦即，範圍中的每個遞增都會與刻度相關聯。</span><span class="sxs-lookup"><span data-stu-id="2eafa-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="2eafa-108">參數</span><span class="sxs-lookup"><span data-stu-id="2eafa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eafa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2eafa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eafa-110">刻度的頻率。</span><span class="sxs-lookup"><span data-stu-id="2eafa-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="2eafa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eafa-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2eafa-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2eafa-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eafa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2eafa-113">Return value</span></span>

<span data-ttu-id="2eafa-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2eafa-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eafa-115">備註</span><span class="sxs-lookup"><span data-stu-id="2eafa-115">Remarks</span></span>

<span data-ttu-id="2eafa-116">您必須要有 [**TBS \_ AUTOTICKS**](trackbar-control-styles.md) 樣式才能使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="2eafa-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eafa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eafa-117">Requirements</span></span>



| <span data-ttu-id="2eafa-118">需求</span><span class="sxs-lookup"><span data-stu-id="2eafa-118">Requirement</span></span> | <span data-ttu-id="2eafa-119">值</span><span class="sxs-lookup"><span data-stu-id="2eafa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eafa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eafa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2eafa-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eafa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eafa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eafa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2eafa-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eafa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eafa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2eafa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eafa-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2eafa-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





