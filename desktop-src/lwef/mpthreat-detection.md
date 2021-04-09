---
title: 'MPTHREAT_DETECTION 列舉 (MpClient .h) '
description: 可能是已知的錯誤威脅偵測類型。
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION 列舉舊版 Windows 環境功能
- PMPTHREAT_DETECTION 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685784"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="0349f-105">MPTHREAT \_ 偵測列舉</span><span class="sxs-lookup"><span data-stu-id="0349f-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="0349f-106">可能是已知的錯誤威脅偵測類型。</span><span class="sxs-lookup"><span data-stu-id="0349f-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="0349f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0349f-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="0349f-108">常數</span><span class="sxs-lookup"><span data-stu-id="0349f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0349f-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP \_ 威脅 \_ 偵測 \_ 實體**</span><span class="sxs-lookup"><span data-stu-id="0349f-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="0349f-110">經由具體簽章偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="0349f-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="0349f-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP \_ 威脅 \_ 偵測 \_ 啟發學習法**</span><span class="sxs-lookup"><span data-stu-id="0349f-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="0349f-112">透過啟發學習法偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="0349f-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="0349f-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP \_ 威脅 \_ 偵測 \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="0349f-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="0349f-114">透過泛型簽章偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="0349f-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="0349f-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP \_ 威脅 \_ 偵測 \_ 可疑**</span><span class="sxs-lookup"><span data-stu-id="0349f-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="0349f-116">透過行為監視偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="0349f-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="0349f-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ 威脅 \_ 偵測 \_ FASTPATH**</span><span class="sxs-lookup"><span data-stu-id="0349f-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="0349f-118">透過 fastpath 偵測到威脅。</span><span class="sxs-lookup"><span data-stu-id="0349f-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0349f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0349f-119">Requirements</span></span>



| <span data-ttu-id="0349f-120">需求</span><span class="sxs-lookup"><span data-stu-id="0349f-120">Requirement</span></span> | <span data-ttu-id="0349f-121">值</span><span class="sxs-lookup"><span data-stu-id="0349f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0349f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0349f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0349f-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0349f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0349f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0349f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0349f-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0349f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0349f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0349f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0349f-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="0349f-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





