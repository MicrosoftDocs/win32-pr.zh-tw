---
title: 'PBM_SETMARQUEE 訊息 (Commctrl .h) '
description: 設定捲軸模式的進度列。 這會使進度列像字幕一樣移動。
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934719"
---
# <a name="pbm_setmarquee-message"></a><span data-ttu-id="f3adb-105">PBM \_ SETMARQUEE 訊息</span><span class="sxs-lookup"><span data-stu-id="f3adb-105">PBM\_SETMARQUEE message</span></span>

<span data-ttu-id="f3adb-106">設定捲軸模式的進度列。</span><span class="sxs-lookup"><span data-stu-id="f3adb-106">Sets the progress bar to marquee mode.</span></span> <span data-ttu-id="f3adb-107">這會使進度列像字幕一樣移動。</span><span class="sxs-lookup"><span data-stu-id="f3adb-107">This causes the progress bar to move like a marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3adb-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3adb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3adb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3adb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3adb-110">指出是否開啟或關閉滾動字幕模式。</span><span class="sxs-lookup"><span data-stu-id="f3adb-110">Indicates whether to turn the marquee mode on or off.</span></span>

</dd> <dt>

<span data-ttu-id="f3adb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3adb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f3adb-112">字幕動畫更新之間的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3adb-112">Time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="f3adb-113">如果此參數為零，則會每隔30毫秒更新字幕動畫。</span><span class="sxs-lookup"><span data-stu-id="f3adb-113">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3adb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3adb-114">Return value</span></span>

<span data-ttu-id="f3adb-115">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f3adb-115">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3adb-116">備註</span><span class="sxs-lookup"><span data-stu-id="f3adb-116">Remarks</span></span>

<span data-ttu-id="f3adb-117">如果您不知道要完成的進度量，但想要指出正在進行的進度，請使用此訊息。</span><span class="sxs-lookup"><span data-stu-id="f3adb-117">Use this message when you do not know the amount of progress toward completion but wish to indicate that progress is being made.</span></span>

<span data-ttu-id="f3adb-118">傳送 **PBM \_ SETMARQUEE** 訊息以啟動或停止動畫。</span><span class="sxs-lookup"><span data-stu-id="f3adb-118">Send the **PBM\_SETMARQUEE** message to start or stop the animation.</span></span>

> [!Note]  
> <span data-ttu-id="f3adb-119">您必須在嘗試開始動畫之前，將控制項樣式設定為 [**PBS \_ 字幕**](progress-bar-control-styles.md) 。</span><span class="sxs-lookup"><span data-stu-id="f3adb-119">You must set the control style to [**PBS\_MARQUEE**](progress-bar-control-styles.md) before attempting to start the animation.</span></span>

 

> [!Note]  
> <span data-ttu-id="f3adb-120">此訊息需要 ComCtl32.dll 6.00 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f3adb-120">This message requires ComCtl32.dll version 6.00 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3adb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3adb-121">Requirements</span></span>



| <span data-ttu-id="f3adb-122">需求</span><span class="sxs-lookup"><span data-stu-id="f3adb-122">Requirement</span></span> | <span data-ttu-id="f3adb-123">值</span><span class="sxs-lookup"><span data-stu-id="f3adb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3adb-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3adb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3adb-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3adb-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3adb-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3adb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3adb-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3adb-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3adb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f3adb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3adb-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3adb-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





