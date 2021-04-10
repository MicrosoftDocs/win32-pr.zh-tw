---
description: 設定系統時，安全性設定引擎會呼叫 SceSvcAttachmentConfig 函數。
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: SceSvcAttachmentConfig 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690112"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="471d1-103">SceSvcAttachmentConfig 回呼函式</span><span class="sxs-lookup"><span data-stu-id="471d1-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="471d1-104">設定系統時，安全性設定引擎會呼叫 **SceSvcAttachmentConfig** 函數。</span><span class="sxs-lookup"><span data-stu-id="471d1-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="471d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="471d1-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="471d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="471d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="471d1-107">*pSceCbInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="471d1-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="471d1-108">[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含資料庫控制碼，以及用來查詢、設定和釋放資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="471d1-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="471d1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="471d1-109">Return value</span></span>

<span data-ttu-id="471d1-110">如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="471d1-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="471d1-111">否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="471d1-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="471d1-112">如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="471d1-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="471d1-113">備註</span><span class="sxs-lookup"><span data-stu-id="471d1-113">Remarks</span></span>

<span data-ttu-id="471d1-114">在執行此函式時，請使用 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo >pfQueryInfo) 以取得設定資訊。</span><span class="sxs-lookup"><span data-stu-id="471d1-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="471d1-115">然後使用傳回的資訊來設定服務。</span><span class="sxs-lookup"><span data-stu-id="471d1-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="471d1-116">此函數必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="471d1-116">This function must do the following:</span></span>

-   <span data-ttu-id="471d1-117">使用 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式，從安全性設定工具中查詢設定資訊 (pSceCbInfo->pfQueryInfo) 。</span><span class="sxs-lookup"><span data-stu-id="471d1-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="471d1-118">使用設定資訊來設定服務。</span><span class="sxs-lookup"><span data-stu-id="471d1-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="471d1-119">如需詳細資訊，請參閱[執行 SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md) 。</span><span class="sxs-lookup"><span data-stu-id="471d1-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="471d1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="471d1-120">Requirements</span></span>



| <span data-ttu-id="471d1-121">需求</span><span class="sxs-lookup"><span data-stu-id="471d1-121">Requirement</span></span> | <span data-ttu-id="471d1-122">值</span><span class="sxs-lookup"><span data-stu-id="471d1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="471d1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="471d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="471d1-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="471d1-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="471d1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="471d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="471d1-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="471d1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471d1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="471d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471d1-128">**SCESVC \_ 回呼 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="471d1-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="471d1-129">**SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="471d1-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




