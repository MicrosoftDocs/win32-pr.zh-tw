---
title: 'MPEXECUTION_STATUS 列舉 (MpClient .h) '
description: 可能的威脅執行狀態。
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS 列舉舊版 Windows 環境功能
- PMPEXECUTION_STATUS 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843368"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="b1d59-105">MPEXECUTION \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="b1d59-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="b1d59-106">可能的威脅執行狀態。</span><span class="sxs-lookup"><span data-stu-id="b1d59-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d59-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d59-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="b1d59-108">常數</span><span class="sxs-lookup"><span data-stu-id="b1d59-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1d59-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP \_ 執行 \_ 狀態 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="b1d59-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b1d59-110">執行狀態未知。</span><span class="sxs-lookup"><span data-stu-id="b1d59-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="b1d59-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP \_ 執行 \_ 狀態已 \_ 封鎖**</span><span class="sxs-lookup"><span data-stu-id="b1d59-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="b1d59-112">由迷你篩選封鎖執行。</span><span class="sxs-lookup"><span data-stu-id="b1d59-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="b1d59-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_允許 MP 執行 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="b1d59-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="b1d59-114">允許由迷你篩選執行。</span><span class="sxs-lookup"><span data-stu-id="b1d59-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="b1d59-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**執行中的 MP \_ 執行 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="b1d59-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="b1d59-116">威脅正在執行。</span><span class="sxs-lookup"><span data-stu-id="b1d59-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="b1d59-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP \_ 執行 \_ 狀態 \_ 未 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="b1d59-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="b1d59-118">威脅並未執行，而且只能在修復期間從引擎使用。</span><span class="sxs-lookup"><span data-stu-id="b1d59-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1d59-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1d59-119">Requirements</span></span>



| <span data-ttu-id="b1d59-120">需求</span><span class="sxs-lookup"><span data-stu-id="b1d59-120">Requirement</span></span> | <span data-ttu-id="b1d59-121">值</span><span class="sxs-lookup"><span data-stu-id="b1d59-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d59-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1d59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d59-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d59-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b1d59-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1d59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d59-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d59-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1d59-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b1d59-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1d59-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1d59-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





