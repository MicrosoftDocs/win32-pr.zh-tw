---
description: '[安全性設定] 嵌入式管理單元會呼叫 SceSvcAttachmentUpdate 函式，以將設定變更傳遞至安全性資料庫。'
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: SceSvcAttachmentUpdate 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690111"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="1f6a3-103">SceSvcAttachmentUpdate 回呼函式</span><span class="sxs-lookup"><span data-stu-id="1f6a3-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="1f6a3-104">[安全性設定] 嵌入式管理單元會呼叫 **SceSvcAttachmentUpdate** 函式，以將設定變更傳遞至安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f6a3-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1f6a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f6a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6a3-107">*pSceCbInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f6a3-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6a3-108">[**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的指標，其中包含 SCE 的回呼控制碼和函式指標。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="1f6a3-109">*ServiceInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f6a3-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f6a3-110">更新的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-110">Updated configuration information.</span></span> <span data-ttu-id="1f6a3-111">這項資訊所使用的資料結構是 [**SCESVC 設定 \_ \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6a3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f6a3-112">Return value</span></span>

<span data-ttu-id="1f6a3-113">如果此函式成功，則會傳回 SCESTATUS \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="1f6a3-114">否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="1f6a3-115">如需有關安全性設定錯誤碼的詳細資訊，請參閱 [附件傳回值](management-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6a3-116">備註</span><span class="sxs-lookup"><span data-stu-id="1f6a3-116">Remarks</span></span>

<span data-ttu-id="1f6a3-117">**SceSvcAttachmentUpdate** 函數必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1f6a3-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="1f6a3-118">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo >pfQueryInfo) ，從安全性資料庫取出目前的基本設定資訊。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="1f6a3-119">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfQueryInfo** 成員所指向的回呼函式 (pSceCbInfo->pfQueryInfo) ，以從安全性資料庫 (分析) 資訊最後一組差異。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="1f6a3-120">使用提供的服務資訊 (查看 *ServiceInfo*) 來計算新的基本設定。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="1f6a3-121">使用提供的服務資訊 (查看 *ServiceInfo*) 和分析，以計算新的差異資訊。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="1f6a3-122">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo >pfSetInfo) ，以在安全性資料庫中設定新的基底設定。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="1f6a3-123">呼叫 [**SCESVC \_ 回呼 \_ 資訊**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)結構的 **pfSetInfo** 成員所指向的回呼函式 (pSceCbInfo->pfSetInfo) ，在安全性資料庫中設定新的分析資訊。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="1f6a3-124">如需詳細資訊，請參閱[執行 SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f6a3-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6a3-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f6a3-125">Requirements</span></span>



| <span data-ttu-id="1f6a3-126">需求</span><span class="sxs-lookup"><span data-stu-id="1f6a3-126">Requirement</span></span> | <span data-ttu-id="1f6a3-127">值</span><span class="sxs-lookup"><span data-stu-id="1f6a3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1f6a3-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f6a3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6a3-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f6a3-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1f6a3-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6a3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6a3-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f6a3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f6a3-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f6a3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6a3-133">**SCESVC \_ 回呼 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1f6a3-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="1f6a3-134">**SCESVC \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1f6a3-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




