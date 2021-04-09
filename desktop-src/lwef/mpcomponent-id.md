---
title: 'MPCOMPONENT_ID 列舉 (MpClient .h) '
description: 惡意程式碼防護管理員可能的元件。
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID 列舉舊版 Windows 環境功能
- PMPCOMPONENT_ID 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094335"
---
# <a name="mpcomponent_id-enumeration"></a><span data-ttu-id="996d1-105">MPCOMPONENT \_ 識別碼列舉</span><span class="sxs-lookup"><span data-stu-id="996d1-105">MPCOMPONENT\_ID enumeration</span></span>

<span data-ttu-id="996d1-106">惡意程式碼防護管理員可能的元件。</span><span class="sxs-lookup"><span data-stu-id="996d1-106">Possible components for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="996d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="996d1-107">Syntax</span></span>


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a><span data-ttu-id="996d1-108">常數</span><span class="sxs-lookup"><span data-stu-id="996d1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="996d1-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ 為簽章 \_**</span><span class="sxs-lookup"><span data-stu-id="996d1-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT\_AS\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**MPCOMPONENT \_ AV 簽章 \_**</span><span class="sxs-lookup"><span data-stu-id="996d1-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**MPCOMPONENT\_AV\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MPCOMPONENT \_ 即時 \_ 監視**</span><span class="sxs-lookup"><span data-stu-id="996d1-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MPCOMPONENT\_REALTIME\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**MPCOMPONENT \_ ONACCESS \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="996d1-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**MPCOMPONENT\_ONACCESS\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**MPCOMPONENT \_ IOAV \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="996d1-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**MPCOMPONENT\_IOAV\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**MPCOMPONENT \_ 行為 \_ 監視**</span><span class="sxs-lookup"><span data-stu-id="996d1-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**MPCOMPONENT\_BEHAVIOR\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**MPCOMPONENT \_ 自動 \_ 掃描**</span><span class="sxs-lookup"><span data-stu-id="996d1-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**MPCOMPONENT\_AUTO\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT \_ 自動 \_ SIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="996d1-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT\_AUTO\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**MPCOMPONENT \_ IPC**</span><span class="sxs-lookup"><span data-stu-id="996d1-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**MPCOMPONENT\_IPC**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="996d1-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT\_NIS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT \_ ELAM**</span><span class="sxs-lookup"><span data-stu-id="996d1-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT\_ELAM**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="996d1-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="996d1-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT\_MAXVALUE**</span></span>
<span data-ttu-id="996d1-121"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="996d1-121"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="996d1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="996d1-122">Requirements</span></span>



| <span data-ttu-id="996d1-123">需求</span><span class="sxs-lookup"><span data-stu-id="996d1-123">Requirement</span></span> | <span data-ttu-id="996d1-124">值</span><span class="sxs-lookup"><span data-stu-id="996d1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="996d1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="996d1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="996d1-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="996d1-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="996d1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="996d1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="996d1-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="996d1-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="996d1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="996d1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="996d1-130"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="996d1-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





