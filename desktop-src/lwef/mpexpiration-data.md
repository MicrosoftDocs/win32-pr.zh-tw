---
title: 'MPEXPIRATION_DATA 結構 (MpClient .h) '
description: 產品到期狀態通知。
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA 結構舊版 Windows 環境功能
- PMPEXPIRATION_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980286"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="8c0ac-105">MPEXPIRATION \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="8c0ac-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="8c0ac-106">產品到期狀態通知。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0ac-107">語法</span><span class="sxs-lookup"><span data-stu-id="8c0ac-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="8c0ac-108">成員</span><span class="sxs-lookup"><span data-stu-id="8c0ac-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c0ac-109">**原因**</span><span class="sxs-lookup"><span data-stu-id="8c0ac-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="8c0ac-110">類型： **MP \_ 過期 \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="8c0ac-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="8c0ac-111">到期原因。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-111">Expiration reason.</span></span> <span data-ttu-id="8c0ac-112">這是下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="8c0ac-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="8c0ac-113">值</span><span class="sxs-lookup"><span data-stu-id="8c0ac-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="8c0ac-114">意義</span><span class="sxs-lookup"><span data-stu-id="8c0ac-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="8c0ac-115"><dt>**MP \_過期的 \_ 未知**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8c0ac-116">不明。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="8c0ac-117"><dt>**MP \_過期的 \_ EVAL**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="8c0ac-118">評價。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="8c0ac-119"><dt>**MP \_過期的 \_ WAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="8c0ac-120">笏。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="8c0ac-121">**State**</span><span class="sxs-lookup"><span data-stu-id="8c0ac-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="8c0ac-122">類型： **MP \_ 過期 \_ 狀態 \_ 報告**</span><span class="sxs-lookup"><span data-stu-id="8c0ac-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="8c0ac-123">過期狀態。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-123">Expiration state.</span></span> <span data-ttu-id="8c0ac-124">這是下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="8c0ac-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="8c0ac-125">值</span><span class="sxs-lookup"><span data-stu-id="8c0ac-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="8c0ac-126">意義</span><span class="sxs-lookup"><span data-stu-id="8c0ac-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="8c0ac-127"><dt>**MP \_過期 \_ 狀態 \_ 報表 \_ 不明**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="8c0ac-128">未知的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="8c0ac-129"><dt>**MP \_過期 \_ 狀態 \_ 報告 \_ 有效**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="8c0ac-130">沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="8c0ac-131"><dt>**MP \_過期 \_ 狀態 \_ 報告 \_ 警告**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="8c0ac-132">即將到期。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="8c0ac-133"><dt>**MP \_過期 \_ 狀態 \_ 報告已 \_ 過期**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="8c0ac-134">過期。</span><span class="sxs-lookup"><span data-stu-id="8c0ac-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c0ac-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0ac-135">Requirements</span></span>



| <span data-ttu-id="8c0ac-136">需求</span><span class="sxs-lookup"><span data-stu-id="8c0ac-136">Requirement</span></span> | <span data-ttu-id="8c0ac-137">值</span><span class="sxs-lookup"><span data-stu-id="8c0ac-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0ac-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c0ac-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0ac-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0ac-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8c0ac-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c0ac-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0ac-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0ac-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c0ac-142">標頭</span><span class="sxs-lookup"><span data-stu-id="8c0ac-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c0ac-143"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c0ac-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





