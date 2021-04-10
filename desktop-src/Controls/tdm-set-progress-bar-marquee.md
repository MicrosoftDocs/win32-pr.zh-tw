---
title: 'TDM_SET_PROGRESS_BAR_MARQUEE 訊息 (Commctrl .h) '
description: 在 [工作] 對話方塊中啟動和停止捲軸顯示進度列，並設定字幕的速度。
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025432"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="a05c1-104">TDM \_ 設定 \_ 進度 \_ 列 \_ 捲軸訊息</span><span class="sxs-lookup"><span data-stu-id="a05c1-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="a05c1-105">在 [工作] 對話方塊中啟動和停止捲軸顯示進度列，並設定字幕的速度。</span><span class="sxs-lookup"><span data-stu-id="a05c1-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="a05c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="a05c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05c1-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a05c1-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05c1-108">**布林** 值，指出是否要開啟或關閉字幕。</span><span class="sxs-lookup"><span data-stu-id="a05c1-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="a05c1-109">使用 **TRUE** 來開啟字幕顯示，或使用 **FALSE** 關閉。</span><span class="sxs-lookup"><span data-stu-id="a05c1-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="a05c1-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a05c1-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a05c1-111">指定字幕動畫更新之間時間（以毫秒為單位）的 **UINT** 。</span><span class="sxs-lookup"><span data-stu-id="a05c1-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="a05c1-112">如果此參數為零，則會每隔30毫秒更新字幕動畫。</span><span class="sxs-lookup"><span data-stu-id="a05c1-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05c1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a05c1-113">Return value</span></span>

<span data-ttu-id="a05c1-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a05c1-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05c1-115">備註</span><span class="sxs-lookup"><span data-stu-id="a05c1-115">Remarks</span></span>

<span data-ttu-id="a05c1-116">如需捲軸模式的詳細資訊，請參閱 [進度列控制項](progress-bar-control.md)。</span><span class="sxs-lookup"><span data-stu-id="a05c1-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a05c1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a05c1-117">Requirements</span></span>



| <span data-ttu-id="a05c1-118">需求</span><span class="sxs-lookup"><span data-stu-id="a05c1-118">Requirement</span></span> | <span data-ttu-id="a05c1-119">值</span><span class="sxs-lookup"><span data-stu-id="a05c1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a05c1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a05c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a05c1-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a05c1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a05c1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a05c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a05c1-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a05c1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a05c1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a05c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05c1-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a05c1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





