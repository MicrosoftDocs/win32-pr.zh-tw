---
description: '\_當佇列完成刪除作業時，會將 SPFILENOTIFY ENDDELETE 通知傳回回回呼常式。 即使使用者取消或發生錯誤，也會傳送此通知。'
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: 'SPFILENOTIFY_ENDDELETE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984742"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="b2f36-104">SPFILENOTIFY \_ ENDDELETE 訊息</span><span class="sxs-lookup"><span data-stu-id="b2f36-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="b2f36-105">當佇列完成刪除作業時，會將 **SPFILENOTIFY \_ ENDDELETE** 通知傳回回回呼常式。</span><span class="sxs-lookup"><span data-stu-id="b2f36-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="b2f36-106">即使使用者取消或發生錯誤，也會傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="b2f36-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="b2f36-107">參數</span><span class="sxs-lookup"><span data-stu-id="b2f36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f36-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b2f36-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f36-109">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b2f36-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="b2f36-110">**FILEPATHS** 結構的 **Win32Error** 成員指出複製作業的結果。</span><span class="sxs-lookup"><span data-stu-id="b2f36-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="b2f36-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b2f36-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f36-112">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b2f36-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f36-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2f36-113">Return value</span></span>

<span data-ttu-id="b2f36-114">傳回碼會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b2f36-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f36-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2f36-115">Requirements</span></span>



| <span data-ttu-id="b2f36-116">需求</span><span class="sxs-lookup"><span data-stu-id="b2f36-116">Requirement</span></span> | <span data-ttu-id="b2f36-117">值</span><span class="sxs-lookup"><span data-stu-id="b2f36-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f36-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2f36-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f36-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2f36-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b2f36-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2f36-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f36-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2f36-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2f36-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b2f36-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f36-123"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f36-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f36-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2f36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f36-125">概觀</span><span class="sxs-lookup"><span data-stu-id="b2f36-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b2f36-126">通知</span><span class="sxs-lookup"><span data-stu-id="b2f36-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b2f36-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="b2f36-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="b2f36-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="b2f36-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="b2f36-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="b2f36-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




