---
description: '\_當佇列啟動檔案重新命名作業時，會將 SPFILENOTIFY STARTRENAME 通知傳送至回呼函數。'
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: 'SPFILENOTIFY_STARTRENAME 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987301"
---
# <a name="spfilenotify_startrename-message"></a><span data-ttu-id="03d64-103">SPFILENOTIFY \_ STARTRENAME 訊息</span><span class="sxs-lookup"><span data-stu-id="03d64-103">SPFILENOTIFY\_STARTRENAME message</span></span>

<span data-ttu-id="03d64-104">當佇列啟動檔案重新命名作業時，會將 **SPFILENOTIFY \_ STARTRENAME** 通知傳送至回呼函數。</span><span class="sxs-lookup"><span data-stu-id="03d64-104">The **SPFILENOTIFY\_STARTRENAME** notification is sent to the callback function when the queue starts a file rename operation.</span></span>


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="03d64-105">參數</span><span class="sxs-lookup"><span data-stu-id="03d64-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d64-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="03d64-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="03d64-107">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="03d64-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="03d64-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="03d64-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="03d64-109">一律具有值 FILEOP \_ RENAME。</span><span class="sxs-lookup"><span data-stu-id="03d64-109">Always has the value FILEOP\_RENAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d64-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="03d64-110">Return value</span></span>

<span data-ttu-id="03d64-111">回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="03d64-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="03d64-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="03d64-112">Return code</span></span>                                                                                  | <span data-ttu-id="03d64-113">Description</span><span class="sxs-lookup"><span data-stu-id="03d64-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03d64-114"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="03d64-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="03d64-115">中止佇列認可。</span><span class="sxs-lookup"><span data-stu-id="03d64-115">Abort the queue commit.</span></span> <span data-ttu-id="03d64-116">回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 來指出終止的原因。</span><span class="sxs-lookup"><span data-stu-id="03d64-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="03d64-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回 **FALSE** ，而後續的 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 呼叫會傳回回呼常式在呼叫 **SetLastError** 期間所設定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="03d64-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="03d64-118"><dt>**FILEOP \_ DOIT R**</dt></span><span class="sxs-lookup"><span data-stu-id="03d64-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="03d64-119">執行檔案複製作業。</span><span class="sxs-lookup"><span data-stu-id="03d64-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="03d64-120"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="03d64-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="03d64-121">略過目前的複製操作。</span><span class="sxs-lookup"><span data-stu-id="03d64-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="03d64-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="03d64-122">Requirements</span></span>



| <span data-ttu-id="03d64-123">需求</span><span class="sxs-lookup"><span data-stu-id="03d64-123">Requirement</span></span> | <span data-ttu-id="03d64-124">值</span><span class="sxs-lookup"><span data-stu-id="03d64-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03d64-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03d64-125">Minimum supported client</span></span><br/> | <span data-ttu-id="03d64-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03d64-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03d64-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03d64-127">Minimum supported server</span></span><br/> | <span data-ttu-id="03d64-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03d64-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03d64-129">標頭</span><span class="sxs-lookup"><span data-stu-id="03d64-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d64-130"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="03d64-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d64-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03d64-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d64-132">概觀</span><span class="sxs-lookup"><span data-stu-id="03d64-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="03d64-133">通知</span><span class="sxs-lookup"><span data-stu-id="03d64-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="03d64-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="03d64-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="03d64-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="03d64-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="03d64-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="03d64-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

