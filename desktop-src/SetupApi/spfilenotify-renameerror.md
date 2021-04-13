---
description: 如果在檔案 \_ 重新命名作業期間發生錯誤，則會將 SPFILENOTIFY RENAMEERROR 通知傳送至回呼常式。
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: 'SPFILENOTIFY_RENAMEERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319875"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="5a298-103">SPFILENOTIFY \_ RENAMEERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="5a298-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="5a298-104">如果在檔案重新命名作業期間發生錯誤，則會將 **SPFILENOTIFY \_ RENAMEERROR** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="5a298-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="5a298-105">參數</span><span class="sxs-lookup"><span data-stu-id="5a298-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a298-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5a298-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a298-107">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5a298-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="5a298-108">**FILEPATHS** 結構的 **Win32Error** 成員會指定在重新命名作業期間發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a298-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a298-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="5a298-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a298-110">未使用的。</span><span class="sxs-lookup"><span data-stu-id="5a298-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a298-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a298-111">Return value</span></span>

<span data-ttu-id="5a298-112">回呼常式應該會傳回下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="5a298-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="5a298-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5a298-113">Return code</span></span>                                                                                  | <span data-ttu-id="5a298-114">Description</span><span class="sxs-lookup"><span data-stu-id="5a298-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a298-115"><dt>**FILEOP \_ 重試**</dt></span><span class="sxs-lookup"><span data-stu-id="5a298-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="5a298-116">使用者選擇再次嘗試重新命名操作。</span><span class="sxs-lookup"><span data-stu-id="5a298-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="5a298-117"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="5a298-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="5a298-118">使用者選擇略過檔案重新命名作業。</span><span class="sxs-lookup"><span data-stu-id="5a298-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="5a298-119"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="5a298-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="5a298-120">停止佇列認可。</span><span class="sxs-lookup"><span data-stu-id="5a298-120">Stop the queue commit.</span></span> <span data-ttu-id="5a298-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5a298-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="5a298-122">[](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) \_ 如果使用者取消) 或錯誤 \_ 記憶體不足，GetLastError 會傳回擴充的錯誤資訊，例如錯誤取消 (\_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="5a298-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a298-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a298-123">Requirements</span></span>



| <span data-ttu-id="5a298-124">需求</span><span class="sxs-lookup"><span data-stu-id="5a298-124">Requirement</span></span> | <span data-ttu-id="5a298-125">值</span><span class="sxs-lookup"><span data-stu-id="5a298-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a298-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a298-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a298-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a298-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5a298-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a298-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a298-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a298-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a298-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5a298-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a298-131"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a298-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a298-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a298-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a298-133">概觀</span><span class="sxs-lookup"><span data-stu-id="5a298-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5a298-134">通知</span><span class="sxs-lookup"><span data-stu-id="5a298-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5a298-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="5a298-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="5a298-136">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="5a298-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="5a298-137">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="5a298-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

