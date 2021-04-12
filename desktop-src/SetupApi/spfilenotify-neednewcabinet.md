---
description: SPFILENOTIFY \_ NEEDNEWCABINET 通知是由 SetupIterateCabinet 傳送，以指出目前的檔案繼續在另一個封包中。
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: 'SPFILENOTIFY_NEEDNEWCABINET 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194919"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="66cfd-103">SPFILENOTIFY \_ NEEDNEWCABINET 訊息</span><span class="sxs-lookup"><span data-stu-id="66cfd-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="66cfd-104">**SPFILENOTIFY \_ NEEDNEWCABINET** 通知是由 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)傳送，以指出目前的檔案繼續在另一個封包中。</span><span class="sxs-lookup"><span data-stu-id="66cfd-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="66cfd-105">您的回呼常式接著可以呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)，或建立自己的對話方塊來提示使用者插入下一個磁片。</span><span class="sxs-lookup"><span data-stu-id="66cfd-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="66cfd-106">參數</span><span class="sxs-lookup"><span data-stu-id="66cfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66cfd-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="66cfd-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="66cfd-108">封 [**包 \_ 資訊**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) 結構的指標，其中包含要解壓縮的封包和檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="66cfd-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="66cfd-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="66cfd-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="66cfd-110">如果回呼不會傳回任何 \_ 錯誤，這個參數就是以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="66cfd-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="66cfd-111">如果字串不是空的，它會指定封包的新路徑。</span><span class="sxs-lookup"><span data-stu-id="66cfd-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66cfd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="66cfd-112">Return value</span></span>

<span data-ttu-id="66cfd-113">您的常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="66cfd-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="66cfd-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="66cfd-114">Return code</span></span>                                                                                 | <span data-ttu-id="66cfd-115">Description</span><span class="sxs-lookup"><span data-stu-id="66cfd-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66cfd-116"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="66cfd-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="66cfd-117">未發生任何錯誤，請繼續處理封包。</span><span class="sxs-lookup"><span data-stu-id="66cfd-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="66cfd-118"><dt>\**錯誤 \_* XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="66cfd-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="66cfd-119">發生指定的類型時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="66cfd-119">An error of the specified type occurred.</span></span> <span data-ttu-id="66cfd-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式會傳回 **FALSE**，而指定的錯誤碼會由對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="66cfd-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="66cfd-121">沒有預設的封包回呼常式;因此，您必須提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="66cfd-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="66cfd-122">備註</span><span class="sxs-lookup"><span data-stu-id="66cfd-122">Remarks</span></span>

<span data-ttu-id="66cfd-123">如果回呼常式未傳回任何 \_ 錯誤， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 會檢查 *Param2* 所指向的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="66cfd-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="66cfd-124">如果緩衝區不是空的，則它會包含新的來源路徑。</span><span class="sxs-lookup"><span data-stu-id="66cfd-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="66cfd-125">如果緩衝區是空的，則會假設來源路徑不會變更。</span><span class="sxs-lookup"><span data-stu-id="66cfd-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="66cfd-126">如果需要插入新媒體，您的回呼函式應該確保封包在傳回之前可以存取，呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) 函式。</span><span class="sxs-lookup"><span data-stu-id="66cfd-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cfd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="66cfd-127">Requirements</span></span>



| <span data-ttu-id="66cfd-128">需求</span><span class="sxs-lookup"><span data-stu-id="66cfd-128">Requirement</span></span> | <span data-ttu-id="66cfd-129">值</span><span class="sxs-lookup"><span data-stu-id="66cfd-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66cfd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66cfd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="66cfd-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66cfd-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="66cfd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66cfd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="66cfd-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66cfd-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66cfd-134">標頭</span><span class="sxs-lookup"><span data-stu-id="66cfd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="66cfd-135"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="66cfd-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66cfd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66cfd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66cfd-137">概觀</span><span class="sxs-lookup"><span data-stu-id="66cfd-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="66cfd-138">通知</span><span class="sxs-lookup"><span data-stu-id="66cfd-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="66cfd-139">**封包 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="66cfd-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="66cfd-140">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="66cfd-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

