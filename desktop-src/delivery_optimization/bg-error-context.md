---
title: 'BG_ERROR_CONTEXT 列舉 (>deliveryoptimization .h) '
description: BG_ERROR_CONTEXT 列舉會定義常數值，以指定發生錯誤的內容。
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- BG_ERROR_CONTEXT 列舉
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464948"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="ddb6c-104">BG_ERROR_CONTEXT 列舉</span><span class="sxs-lookup"><span data-stu-id="ddb6c-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="ddb6c-105">**BG_ERROR_CONTEXT** 列舉會定義常數值，以指定發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb6c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb6c-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="ddb6c-107">常數</span><span class="sxs-lookup"><span data-stu-id="ddb6c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ddb6c-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-109">未發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-111">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-113">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-115">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-117">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-119">錯誤與指定的遠端檔案相關。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="ddb6c-120">例如，URL 無法存取。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-122">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb6c-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="ddb6c-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="ddb6c-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddb6c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddb6c-125">Requirements</span></span>



| <span data-ttu-id="ddb6c-126">需求</span><span class="sxs-lookup"><span data-stu-id="ddb6c-126">Requirement</span></span> | <span data-ttu-id="ddb6c-127">值</span><span class="sxs-lookup"><span data-stu-id="ddb6c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb6c-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ddb6c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb6c-129">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddb6c-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ddb6c-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ddb6c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb6c-131">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ddb6c-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ddb6c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ddb6c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddb6c-133"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb6c-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb6c-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddb6c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb6c-135">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="ddb6c-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





