---
title: 'WER 錯誤碼 (Werapi .h) '
description: 下表提供 Windows 錯誤報告所使用的自訂錯誤碼清單。
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965898"
---
# <a name="wer-error-codes"></a><span data-ttu-id="d49ae-103">WER 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d49ae-103">WER Error Codes</span></span>

<span data-ttu-id="d49ae-104">下表提供 Windows 錯誤報告所使用的自訂錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="d49ae-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="d49ae-105">常數</span><span class="sxs-lookup"><span data-stu-id="d49ae-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="d49ae-106">描述</span><span class="sxs-lookup"><span data-stu-id="d49ae-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="d49ae-107"><dt>**WER \_ E \_ \_ 緩衝區不足**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="d49ae-108">緩衝區太小，無法包含資料。</span><span class="sxs-lookup"><span data-stu-id="d49ae-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="d49ae-109"><dt>**WER \_ E \_ 不正確 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="d49ae-110">以不支援的方式呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="d49ae-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="d49ae-111"><dt>**\_超過 WER E \_ 長度 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="d49ae-112">超過長度限制的其中一個。</span><span class="sxs-lookup"><span data-stu-id="d49ae-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="d49ae-113"><dt>**WER \_ E \_ 遺失 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="d49ae-114">遺漏一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="d49ae-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="d49ae-115"><dt>**\_ \_ 找不到 WER E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="d49ae-116">Element not found.</span><span class="sxs-lookup"><span data-stu-id="d49ae-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="d49ae-117"><dt>**\_ \_ 已停用 WER E 存放區 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="d49ae-118">存放區已停用。</span><span class="sxs-lookup"><span data-stu-id="d49ae-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="d49ae-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d49ae-119">Requirements</span></span>



| <span data-ttu-id="d49ae-120">需求</span><span class="sxs-lookup"><span data-stu-id="d49ae-120">Requirement</span></span> | <span data-ttu-id="d49ae-121">值</span><span class="sxs-lookup"><span data-stu-id="d49ae-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d49ae-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d49ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d49ae-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d49ae-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d49ae-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d49ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d49ae-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d49ae-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d49ae-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d49ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d49ae-127"><dt>Werapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d49ae-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





