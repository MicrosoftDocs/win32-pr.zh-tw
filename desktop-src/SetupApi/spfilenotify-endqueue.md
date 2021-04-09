---
description: '\_當所有已排入佇列的作業都完成時，會將 SPFILENOTIFY ENDQUEUE 通知傳送至回呼常式。'
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: 'SPFILENOTIFY_ENDQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945243"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="7d4b6-103">SPFILENOTIFY \_ ENDQUEUE 訊息</span><span class="sxs-lookup"><span data-stu-id="7d4b6-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="7d4b6-104">當所有已排入佇列的作業都完成時，會將 **SPFILENOTIFY \_ ENDQUEUE** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="7d4b6-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="7d4b6-105">參數</span><span class="sxs-lookup"><span data-stu-id="7d4b6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d4b6-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="7d4b6-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4b6-107">如果已成功處理佇列，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7d4b6-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="7d4b6-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="7d4b6-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d4b6-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="7d4b6-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d4b6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d4b6-110">Return value</span></span>

<span data-ttu-id="7d4b6-111">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7d4b6-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d4b6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d4b6-112">Requirements</span></span>



| <span data-ttu-id="7d4b6-113">需求</span><span class="sxs-lookup"><span data-stu-id="7d4b6-113">Requirement</span></span> | <span data-ttu-id="7d4b6-114">值</span><span class="sxs-lookup"><span data-stu-id="7d4b6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d4b6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d4b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d4b6-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d4b6-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d4b6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d4b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d4b6-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d4b6-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d4b6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7d4b6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d4b6-120"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d4b6-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d4b6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d4b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4b6-122">概觀</span><span class="sxs-lookup"><span data-stu-id="7d4b6-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="7d4b6-123">通知</span><span class="sxs-lookup"><span data-stu-id="7d4b6-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="7d4b6-124">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7d4b6-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="7d4b6-125">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="7d4b6-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




