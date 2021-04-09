---
description: 分析系統時，安全性設定引擎會呼叫 SceSvcAttachmentAnalyze 函數。
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: SceSvcAttachmentAnalyze 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690115"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="7b4c6-103">SceSvcAttachmentAnalyze 回呼函式</span><span class="sxs-lookup"><span data-stu-id="7b4c6-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="7b4c6-104">分析系統時，安全性設定引擎會呼叫 **SceSvcAttachmentAnalyze** 函數。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b4c6-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7b4c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="7b4c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4c6-107">*pSceCbInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b4c6-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4c6-108">[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含不透明的資料庫控制碼，以及用來查詢、設定和釋放資訊的回呼函數指標。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4c6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b4c6-109">Return value</span></span>

<span data-ttu-id="7b4c6-110">如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="7b4c6-111">否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="7b4c6-112">如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4c6-113">備註</span><span class="sxs-lookup"><span data-stu-id="7b4c6-113">Remarks</span></span>

<span data-ttu-id="7b4c6-114">**SceSvcAttachmentAnalyze** 函數必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7b4c6-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="7b4c6-115">從服務直接查詢設定資訊。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="7b4c6-116">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo->pfQueryInfo) 以從安全性資料庫取出資訊。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="7b4c6-117">根據類型和語法計算資訊之間的差異。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="7b4c6-118">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo->pfSetInfo) ，以不同的抓取服務資訊來更新安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="7b4c6-119">如需詳細資訊，請參閱 [執行 SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)。</span><span class="sxs-lookup"><span data-stu-id="7b4c6-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4c6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b4c6-120">Requirements</span></span>



| <span data-ttu-id="7b4c6-121">需求</span><span class="sxs-lookup"><span data-stu-id="7b4c6-121">Requirement</span></span> | <span data-ttu-id="7b4c6-122">值</span><span class="sxs-lookup"><span data-stu-id="7b4c6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b4c6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b4c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4c6-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b4c6-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7b4c6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b4c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4c6-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b4c6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b4c6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b4c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4c6-128">執行 SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="7b4c6-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="7b4c6-129">**SCESVC \_ 回呼 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7b4c6-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="7b4c6-130">**SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="7b4c6-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




