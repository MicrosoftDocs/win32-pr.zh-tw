---
description: '\_當佇列開始處理刪除、重新命名或複製子佇列中的作業時，會將 SPFILENOTIFY STARTSUBQUEUE 通知傳送至回呼函數。'
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: 'SPFILENOTIFY_STARTSUBQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985356"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="d63c6-103">SPFILENOTIFY \_ STARTSUBQUEUE 訊息</span><span class="sxs-lookup"><span data-stu-id="d63c6-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="d63c6-104">當佇列開始處理刪除、重新命名或複製子佇列中的作業時，會將 **SPFILENOTIFY \_ STARTSUBQUEUE** 通知傳送至回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d63c6-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="d63c6-105">參數</span><span class="sxs-lookup"><span data-stu-id="d63c6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63c6-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="d63c6-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d63c6-107">已啟動的子佇列。</span><span class="sxs-lookup"><span data-stu-id="d63c6-107">Subqueue that has been started.</span></span> <span data-ttu-id="d63c6-108">此參數可以是任何一個值 FILEOP \_ DELETE、FILEOP \_ RENAME 或 FILEOP \_ COPY。</span><span class="sxs-lookup"><span data-stu-id="d63c6-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="d63c6-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d63c6-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d63c6-110">子佇列中的檔案複製、重新命名或刪除作業的數目。</span><span class="sxs-lookup"><span data-stu-id="d63c6-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d63c6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d63c6-111">Return value</span></span>

<span data-ttu-id="d63c6-112">如果發生錯誤，回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)，並指定錯誤，然後傳回零。</span><span class="sxs-lookup"><span data-stu-id="d63c6-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="d63c6-113">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函式會傳回 **FALSE** ，而後續對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫將會傳回回呼常式所設定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d63c6-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="d63c6-114">如果未發生任何錯誤，回呼常式應該會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d63c6-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63c6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d63c6-115">Requirements</span></span>



| <span data-ttu-id="d63c6-116">需求</span><span class="sxs-lookup"><span data-stu-id="d63c6-116">Requirement</span></span> | <span data-ttu-id="d63c6-117">值</span><span class="sxs-lookup"><span data-stu-id="d63c6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d63c6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d63c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d63c6-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63c6-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d63c6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d63c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d63c6-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63c6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d63c6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d63c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63c6-123"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="d63c6-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63c6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d63c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63c6-125">概觀</span><span class="sxs-lookup"><span data-stu-id="d63c6-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d63c6-126">通知</span><span class="sxs-lookup"><span data-stu-id="d63c6-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d63c6-127">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d63c6-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d63c6-128">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="d63c6-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

