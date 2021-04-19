---
title: 'MPTHREAT_STATUS 列舉 (MpClient .h) '
description: 可能的威脅狀態。
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS 列舉舊版 Windows 環境功能
- PMPTHREAT_STATUS 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969157"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="bf925-105">MPTHREAT \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="bf925-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="bf925-106">可能的威脅狀態。</span><span class="sxs-lookup"><span data-stu-id="bf925-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf925-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf925-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="bf925-108">常數</span><span class="sxs-lookup"><span data-stu-id="bf925-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bf925-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP \_ 威脅 \_ 狀態 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="bf925-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**偵測 \_ 到 MP 威脅 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**已 \_ 清除 MP 威脅 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**已 \_ 隔離的 MP 威脅 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_ \_ 已移除 MP 威脅狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_允許 MP 威脅 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP \_ 威脅 \_ 狀態已 \_ 封鎖**</span><span class="sxs-lookup"><span data-stu-id="bf925-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP \_ 威脅 \_ 狀態 \_ 清除 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bf925-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP \_ 威脅 \_ 狀態 \_ 隔離 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bf925-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP \_ 威脅 \_ 狀態 \_ 移除 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bf925-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP \_ 威脅 \_ 狀態 \_ 允許 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bf925-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**已 \_ 放棄 MP 威脅 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="bf925-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bf925-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP \_ 威脅 \_ 狀態 \_ 區塊 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="bf925-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="bf925-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bf925-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bf925-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf925-123">Requirements</span></span>



| <span data-ttu-id="bf925-124">需求</span><span class="sxs-lookup"><span data-stu-id="bf925-124">Requirement</span></span> | <span data-ttu-id="bf925-125">值</span><span class="sxs-lookup"><span data-stu-id="bf925-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf925-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf925-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bf925-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf925-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bf925-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf925-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bf925-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf925-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf925-130">標頭</span><span class="sxs-lookup"><span data-stu-id="bf925-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf925-131"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf925-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





