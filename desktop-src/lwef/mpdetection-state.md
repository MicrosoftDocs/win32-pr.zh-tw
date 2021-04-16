---
title: 'MPDETECTION_STATE 列舉 (MpClient .h) '
description: 目前偵測到之威脅的狀態。
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE 列舉舊版 Windows 環境功能
- PMPDETECTION_STATE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464905"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="bfe6f-105">MPDETECTION \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="bfe6f-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="bfe6f-106">目前偵測到之威脅的狀態。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe6f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfe6f-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="bfe6f-108">常數</span><span class="sxs-lookup"><span data-stu-id="bfe6f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bfe6f-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION \_ 狀態 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-110">處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION \_ 狀態為 \_ 主動**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-112">作用中的威脅。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION \_ 狀態 \_ 已完成**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-114">暫止24小時到已清除的移動。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION \_ 狀態 \_ 其他 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-116">需要額外的動作。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION \_ 狀態 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-118">非重大補救失敗。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION \_ 狀態 \_ 嚴重 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-120">重大補救失敗。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="bfe6f-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**已 \_ 清除 MPDETECTION 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bfe6f-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="bfe6f-122">威脅不會顯示在狀態查詢中，只會顯示在歷程記錄中。</span><span class="sxs-lookup"><span data-stu-id="bfe6f-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfe6f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfe6f-123">Requirements</span></span>



| <span data-ttu-id="bfe6f-124">需求</span><span class="sxs-lookup"><span data-stu-id="bfe6f-124">Requirement</span></span> | <span data-ttu-id="bfe6f-125">值</span><span class="sxs-lookup"><span data-stu-id="bfe6f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfe6f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfe6f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe6f-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfe6f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bfe6f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfe6f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe6f-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfe6f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfe6f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="bfe6f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe6f-131"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe6f-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





