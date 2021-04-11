---
title: 'ADSI 列印工作狀態常數 (Adssts .h) '
description: 下列常數是與 IADsPrintJobOperations. Status 屬性搭配使用，以指出列印工作的狀態。
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934822"
---
# <a name="adsi-print-job-status-constants"></a><span data-ttu-id="b6e6d-103">ADSI 列印工作狀態常數</span><span class="sxs-lookup"><span data-stu-id="b6e6d-103">ADSI Print Job Status Constants</span></span>

<span data-ttu-id="b6e6d-104">下列常數是與 [**IADsPrintJobOperations. Status**](iadsprintjoboperations-property-methods.md) 屬性搭配使用，以指出列印工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-104">The following constants are used with the [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) property to indicate the status of a print job.</span></span>

<dl> <dt>

<span data-ttu-id="b6e6d-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS \_ 作業已 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-105"><span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS\_JOB\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-106">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-107">列印工作已暫停。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-107">The print job is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS \_ 作業 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-108"><span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS\_JOB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-109">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-110">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-110">An error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**廣告 \_ 作業 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-111"><span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ADS\_JOB\_DELETING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-112">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-113">正在刪除列印工作。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-113">The print job is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS \_ 作業 \_ 幕後處理**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-114"><span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS\_JOB\_SPOOLING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-115">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-116">列印工作正在進行多工緩衝處理。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-116">The print job is being spooled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS \_ 工作 \_ 列印**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-117"><span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS\_JOB\_PRINTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-118">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-119">列印工作正在列印中。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-119">The print job is being printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS \_ 工作 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-120"><span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS\_JOB\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-121">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-121">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-122">印表機為離線。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-122">The printer is offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS \_ 作業 \_ PAPEROUT**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-123"><span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS\_JOB\_PAPEROUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-124">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-124">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-125">印表機紙張用完。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-125">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**廣告 \_ 作業 \_ 列印**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-126"><span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS\_JOB\_PRINTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-127">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="b6e6d-127">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-128">列印工作已列印。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-128">The print job has been printed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b6e6d-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_ \_ 已刪除 ADS 作業**</span><span class="sxs-lookup"><span data-stu-id="b6e6d-129"><span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS\_JOB\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6e6d-130">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="b6e6d-130">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="b6e6d-131">已刪除列印工作。</span><span class="sxs-lookup"><span data-stu-id="b6e6d-131">The print job has been deleted.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6e6d-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6e6d-132">Requirements</span></span>



| <span data-ttu-id="b6e6d-133">需求</span><span class="sxs-lookup"><span data-stu-id="b6e6d-133">Requirement</span></span> | <span data-ttu-id="b6e6d-134">值</span><span class="sxs-lookup"><span data-stu-id="b6e6d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e6d-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6e6d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e6d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6e6d-136">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="b6e6d-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6e6d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e6d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6e6d-138">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="b6e6d-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b6e6d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e6d-140"><dt>Adssts。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e6d-140"><dt>Adssts.h</dt></span></span> </dl> |



 

 





