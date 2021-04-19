---
title: 'MPTHREAT_SEVERITY 列舉 (MpClient .h) '
description: 可能的威脅嚴重性。
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY 列舉舊版 Windows 環境功能
- PMPTHREAT_SEVERITY 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966924"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="f2c51-105">MPTHREAT \_ 嚴重性列舉</span><span class="sxs-lookup"><span data-stu-id="f2c51-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="f2c51-106">可能的威脅嚴重性。</span><span class="sxs-lookup"><span data-stu-id="f2c51-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c51-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c51-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="f2c51-108">常數</span><span class="sxs-lookup"><span data-stu-id="f2c51-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP \_ 威脅 \_ 嚴重性 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="f2c51-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2c51-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP \_ 威脅 \_ 嚴重性 \_ 低**</span><span class="sxs-lookup"><span data-stu-id="f2c51-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2c51-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP \_ 威脅 \_ 嚴重性 \_ 適中**</span><span class="sxs-lookup"><span data-stu-id="f2c51-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2c51-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP \_ 威脅 \_ 嚴重性 \_ 高**</span><span class="sxs-lookup"><span data-stu-id="f2c51-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2c51-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP \_ 威脅 \_ 嚴重性 \_ 嚴重**</span><span class="sxs-lookup"><span data-stu-id="f2c51-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f2c51-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP \_ 威脅 \_ 嚴重性 \_**</span><span class="sxs-lookup"><span data-stu-id="f2c51-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="f2c51-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f2c51-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f2c51-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2c51-116">Requirements</span></span>



| <span data-ttu-id="f2c51-117">需求</span><span class="sxs-lookup"><span data-stu-id="f2c51-117">Requirement</span></span> | <span data-ttu-id="f2c51-118">值</span><span class="sxs-lookup"><span data-stu-id="f2c51-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c51-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2c51-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c51-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2c51-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f2c51-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2c51-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c51-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2c51-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2c51-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f2c51-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c51-124"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c51-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





