---
title: 'MPCALLBACK_TYPE 列舉 (MpClient .h) '
description: 可能的回呼類型。
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE 列舉舊版 Windows 環境功能
- PMPCALLBACK_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464912"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="65482-105">MPCALLBACK \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="65482-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="65482-106">可能的回呼類型。</span><span class="sxs-lookup"><span data-stu-id="65482-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="65482-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="65482-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="65482-108">常數</span><span class="sxs-lookup"><span data-stu-id="65482-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="65482-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="65482-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="65482-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK \_ 威脅**</span><span class="sxs-lookup"><span data-stu-id="65482-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK \_ 掃描**</span><span class="sxs-lookup"><span data-stu-id="65482-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ CLEAN**</span><span class="sxs-lookup"><span data-stu-id="65482-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="65482-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="65482-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="65482-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="65482-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK \_ 設定 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="65482-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**</span><span class="sxs-lookup"><span data-stu-id="65482-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK \_ 產品 \_ 到期**</span><span class="sxs-lookup"><span data-stu-id="65482-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ 私用**</span><span class="sxs-lookup"><span data-stu-id="65482-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK \_ 健全狀況**</span><span class="sxs-lookup"><span data-stu-id="65482-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="65482-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="65482-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="65482-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="65482-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="65482-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="65482-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="65482-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="65482-127">Requirements</span></span>



| <span data-ttu-id="65482-128">需求</span><span class="sxs-lookup"><span data-stu-id="65482-128">Requirement</span></span> | <span data-ttu-id="65482-129">值</span><span class="sxs-lookup"><span data-stu-id="65482-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65482-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65482-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65482-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65482-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="65482-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65482-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65482-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65482-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65482-134">標頭</span><span class="sxs-lookup"><span data-stu-id="65482-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="65482-135"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="65482-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





