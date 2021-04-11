---
description: 如果檔案 \_ 刪除作業期間發生錯誤，則會將 SPFILENOTIFY DELETEERROR 通知傳送至回呼常式。
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: 'SPFILENOTIFY_DELETEERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027488"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="d2c1c-103">SPFILENOTIFY \_ DELETEERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="d2c1c-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="d2c1c-104">如果檔案刪除作業期間發生錯誤，則會將 **SPFILENOTIFY \_ DELETEERROR** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="d2c1c-105">參數</span><span class="sxs-lookup"><span data-stu-id="d2c1c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c1c-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="d2c1c-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c1c-107">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d2c1c-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d2c1c-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d2c1c-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c1c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2c1c-110">Return value</span></span>

<span data-ttu-id="d2c1c-111">回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="d2c1c-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d2c1c-112">Return code</span></span>                                                                                  | <span data-ttu-id="d2c1c-113">Description</span><span class="sxs-lookup"><span data-stu-id="d2c1c-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2c1c-114"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c1c-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="d2c1c-115">應取消佇列處理。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-115">Queue processing should be canceled.</span></span> <span data-ttu-id="d2c1c-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回擴充的錯誤資訊，例如 \_ ，如果使用者取消) 或錯誤 \_ 記憶體不足，則會傳回錯誤 (\_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="d2c1c-117"><dt>**FILEOP \_ 重試**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c1c-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="d2c1c-118">使用者正在嘗試刪除操作。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="d2c1c-119"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c1c-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="d2c1c-120">使用者即將略過檔案刪除操作。</span><span class="sxs-lookup"><span data-stu-id="d2c1c-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="d2c1c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2c1c-121">Requirements</span></span>



| <span data-ttu-id="d2c1c-122">需求</span><span class="sxs-lookup"><span data-stu-id="d2c1c-122">Requirement</span></span> | <span data-ttu-id="d2c1c-123">值</span><span class="sxs-lookup"><span data-stu-id="d2c1c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c1c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2c1c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c1c-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c1c-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2c1c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2c1c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c1c-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c1c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2c1c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d2c1c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c1c-129"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c1c-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2c1c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2c1c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c1c-131">概觀</span><span class="sxs-lookup"><span data-stu-id="d2c1c-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d2c1c-132">通知</span><span class="sxs-lookup"><span data-stu-id="d2c1c-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d2c1c-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="d2c1c-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="d2c1c-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d2c1c-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d2c1c-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="d2c1c-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

