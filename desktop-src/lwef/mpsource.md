---
title: 'MPSOURCE 列舉 (MpClient) '
description: 來源的可能類別。
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- MPSOURCE 列舉舊版 Windows 環境功能
- PMPSOURCE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9255029512499a0e2948a44701ef4482aff4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934642"
---
# <a name="mpsource-enumeration"></a><span data-ttu-id="0f72e-105">MPSOURCE 列舉</span><span class="sxs-lookup"><span data-stu-id="0f72e-105">MPSOURCE enumeration</span></span>

<span data-ttu-id="0f72e-106">來源的可能類別。</span><span class="sxs-lookup"><span data-stu-id="0f72e-106">Possible category of source.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f72e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f72e-107">Syntax</span></span>


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a><span data-ttu-id="0f72e-108">常數</span><span class="sxs-lookup"><span data-stu-id="0f72e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0f72e-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="0f72e-109"><span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-110">來源不明。</span><span class="sxs-lookup"><span data-stu-id="0f72e-110">Source unknown.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="0f72e-111"><span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**MPSOURCE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-112">使用者起始。</span><span class="sxs-lookup"><span data-stu-id="0f72e-112">User initiated.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="0f72e-113"><span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**MPSOURCE\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-114">系統起始。</span><span class="sxs-lookup"><span data-stu-id="0f72e-114">system initiated.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**\_即時 MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="0f72e-115"><span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE\_REALTIME**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-116">即時啟動的元件。</span><span class="sxs-lookup"><span data-stu-id="0f72e-116">Realtime component initiated.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE \_ IOAV**</span><span class="sxs-lookup"><span data-stu-id="0f72e-117"><span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE\_IOAV**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-118">IE 下載和 Outlook Express 附件已起始。</span><span class="sxs-lookup"><span data-stu-id="0f72e-118">IE Downloads and Outlook Express Attachments initiated.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="0f72e-119"><span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-120">網路檢查系統。</span><span class="sxs-lookup"><span data-stu-id="0f72e-120">Network inspection system.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE \_ BHO**</span><span class="sxs-lookup"><span data-stu-id="0f72e-121"><span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE\_BHO**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-122">BHO-web 腳本 (已淘汰的) 。</span><span class="sxs-lookup"><span data-stu-id="0f72e-122">BHO - web script (deprecated).</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE \_ IEPROTECT**</span><span class="sxs-lookup"><span data-stu-id="0f72e-123"><span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE\_IEPROTECT**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-124">IE-IExtensionValidation。</span><span class="sxs-lookup"><span data-stu-id="0f72e-124">IE - IExtensionValidation.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE \_ ELAM**</span><span class="sxs-lookup"><span data-stu-id="0f72e-125"><span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE\_ELAM**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-126">ELAM</span><span class="sxs-lookup"><span data-stu-id="0f72e-126">ELAM</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE \_ 本機 \_ 證明**</span><span class="sxs-lookup"><span data-stu-id="0f72e-127"><span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**MPSOURCE\_LOCAL\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-128">本機證明。</span><span class="sxs-lookup"><span data-stu-id="0f72e-128">Local attestation.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE \_ 遠端 \_ 證明**</span><span class="sxs-lookup"><span data-stu-id="0f72e-129"><span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**MPSOURCE\_REMOTE\_ATTESTATION**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-130">遠端證明。</span><span class="sxs-lookup"><span data-stu-id="0f72e-130">Remote attestation.</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE \_ AMSI**</span><span class="sxs-lookup"><span data-stu-id="0f72e-131"><span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE\_AMSI**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-132">AMSI</span><span class="sxs-lookup"><span data-stu-id="0f72e-132">AMSI</span></span>

</dd> <dt>

<span data-ttu-id="0f72e-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP \_ 來源 \_ TIMESPAN.MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="0f72e-133"><span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**MP\_SOURCE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="0f72e-134">可能的最大值。</span><span class="sxs-lookup"><span data-stu-id="0f72e-134">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f72e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f72e-135">Requirements</span></span>



| <span data-ttu-id="0f72e-136">需求</span><span class="sxs-lookup"><span data-stu-id="0f72e-136">Requirement</span></span> | <span data-ttu-id="0f72e-137">值</span><span class="sxs-lookup"><span data-stu-id="0f72e-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f72e-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f72e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0f72e-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f72e-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0f72e-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f72e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0f72e-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f72e-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f72e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="0f72e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f72e-143"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f72e-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





