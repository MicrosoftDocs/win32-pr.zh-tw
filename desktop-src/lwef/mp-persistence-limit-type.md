---
title: 'MP_PERSISTENCE_LIMIT_TYPE 列舉 (MpClient .h) '
description: 持續性限制類型。
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE 列舉舊版 Windows 環境功能
- PMP_PERSISTENCE_LIMIT_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025408"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="023a3-105">MP \_ 持續性 \_ 限制 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="023a3-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="023a3-106">持續性限制類型。</span><span class="sxs-lookup"><span data-stu-id="023a3-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="023a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="023a3-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="023a3-108">常數</span><span class="sxs-lookup"><span data-stu-id="023a3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="023a3-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP \_ 持續性 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="023a3-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-110">不明。</span><span class="sxs-lookup"><span data-stu-id="023a3-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="023a3-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP \_ 持續性 \_ 無 \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="023a3-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-112">沒有限制。</span><span class="sxs-lookup"><span data-stu-id="023a3-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="023a3-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP \_ 持續 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="023a3-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-114">持續期間。</span><span class="sxs-lookup"><span data-stu-id="023a3-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="023a3-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP \_ 持續性的 \_ VDM \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="023a3-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-116">VDM 版本。</span><span class="sxs-lookup"><span data-stu-id="023a3-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="023a3-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP \_ 持續 \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="023a3-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-118">Timestamp：</span><span class="sxs-lookup"><span data-stu-id="023a3-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="023a3-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**強制執行 MP \_ 持續性 \_**</span><span class="sxs-lookup"><span data-stu-id="023a3-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="023a3-120">強迫。</span><span class="sxs-lookup"><span data-stu-id="023a3-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="023a3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="023a3-121">Requirements</span></span>



| <span data-ttu-id="023a3-122">需求</span><span class="sxs-lookup"><span data-stu-id="023a3-122">Requirement</span></span> | <span data-ttu-id="023a3-123">值</span><span class="sxs-lookup"><span data-stu-id="023a3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="023a3-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="023a3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="023a3-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="023a3-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="023a3-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="023a3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="023a3-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="023a3-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="023a3-128">標頭</span><span class="sxs-lookup"><span data-stu-id="023a3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="023a3-129"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="023a3-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





