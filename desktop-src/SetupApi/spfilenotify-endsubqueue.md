---
description: '\_當佇列完成刪除、重新命名或複製子佇列中的所有作業時，會將 SPFILENOTIFY ENDSUBQUEUE 通知傳送至回呼函數。'
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: 'SPFILENOTIFY_ENDSUBQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027486"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="7d2ad-103">SPFILENOTIFY \_ ENDSUBQUEUE 訊息</span><span class="sxs-lookup"><span data-stu-id="7d2ad-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="7d2ad-104">當佇列完成刪除、重新命名或複製子佇列中的所有作業時，會將 **SPFILENOTIFY \_ ENDSUBQUEUE** 通知傳送至回呼函數。</span><span class="sxs-lookup"><span data-stu-id="7d2ad-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="7d2ad-105">參數</span><span class="sxs-lookup"><span data-stu-id="7d2ad-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d2ad-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="7d2ad-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2ad-107">已完成的子佇列。</span><span class="sxs-lookup"><span data-stu-id="7d2ad-107">Subqueue that has been completed.</span></span> <span data-ttu-id="7d2ad-108">這個參數可以是下列其中一個值 FILEOP \_ DELETE、FILEOP \_ RENAME 或 FILEOP \_ COPY。</span><span class="sxs-lookup"><span data-stu-id="7d2ad-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="7d2ad-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="7d2ad-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2ad-110">未使用的。</span><span class="sxs-lookup"><span data-stu-id="7d2ad-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d2ad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d2ad-111">Return value</span></span>

<span data-ttu-id="7d2ad-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7d2ad-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d2ad-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d2ad-113">Requirements</span></span>



| <span data-ttu-id="7d2ad-114">需求</span><span class="sxs-lookup"><span data-stu-id="7d2ad-114">Requirement</span></span> | <span data-ttu-id="7d2ad-115">值</span><span class="sxs-lookup"><span data-stu-id="7d2ad-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d2ad-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d2ad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d2ad-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d2ad-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d2ad-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d2ad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d2ad-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d2ad-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d2ad-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7d2ad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d2ad-121"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d2ad-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d2ad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d2ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d2ad-123">概觀</span><span class="sxs-lookup"><span data-stu-id="7d2ad-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="7d2ad-124">通知</span><span class="sxs-lookup"><span data-stu-id="7d2ad-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="7d2ad-125">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7d2ad-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="7d2ad-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="7d2ad-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




