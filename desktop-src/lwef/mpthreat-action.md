---
title: 'MPTHREAT_ACTION 列舉 (MpClient .h) '
description: 可能的威脅動作。
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION 列舉舊版 Windows 環境功能
- PMPTHREAT_ACTION 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094511"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="f97c7-105">MPTHREAT \_ 動作列舉</span><span class="sxs-lookup"><span data-stu-id="f97c7-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="f97c7-106">可能的威脅動作。</span><span class="sxs-lookup"><span data-stu-id="f97c7-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f97c7-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="f97c7-108">常數</span><span class="sxs-lookup"><span data-stu-id="f97c7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f97c7-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP \_ 威脅 \_ 動作 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="f97c7-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP \_ 威脅 \_ 動作 \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="f97c7-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP \_ 威脅 \_ 動作 \_ 隔離**</span><span class="sxs-lookup"><span data-stu-id="f97c7-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP \_ 威脅 \_ 動作 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="f97c7-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP \_ 威脅 \_ 動作 \_ 允許**</span><span class="sxs-lookup"><span data-stu-id="f97c7-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**使用者管理的 MP \_ 威脅 \_ 動作 \_**</span><span class="sxs-lookup"><span data-stu-id="f97c7-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP \_ 威脅 \_ 動作 \_ NOACTION**</span><span class="sxs-lookup"><span data-stu-id="f97c7-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP \_ 威脅 \_ 動作 \_ 區塊**</span><span class="sxs-lookup"><span data-stu-id="f97c7-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f97c7-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP \_ 威脅 \_ 動作 \_ 最大 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="f97c7-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="f97c7-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f97c7-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f97c7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f97c7-119">Requirements</span></span>



| <span data-ttu-id="f97c7-120">需求</span><span class="sxs-lookup"><span data-stu-id="f97c7-120">Requirement</span></span> | <span data-ttu-id="f97c7-121">值</span><span class="sxs-lookup"><span data-stu-id="f97c7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f97c7-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f97c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f97c7-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f97c7-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f97c7-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f97c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f97c7-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f97c7-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f97c7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f97c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f97c7-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f97c7-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





