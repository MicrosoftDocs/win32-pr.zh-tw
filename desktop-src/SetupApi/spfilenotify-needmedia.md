---
description: '\_當需要新媒體或新的封包檔時，會將 SPFILENOTIFY NEEDMEDIA 通知傳送至回呼常式。'
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: 'SPFILENOTIFY_NEEDMEDIA 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982141"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="0b650-103">SPFILENOTIFY \_ NEEDMEDIA 訊息</span><span class="sxs-lookup"><span data-stu-id="0b650-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="0b650-104">當需要新媒體或新的封包檔時，會將 **SPFILENOTIFY \_ NEEDMEDIA** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="0b650-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="0b650-105">參數</span><span class="sxs-lookup"><span data-stu-id="0b650-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b650-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="0b650-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b650-107">[**來源 \_ 媒體**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0b650-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0b650-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0b650-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b650-109">字元陣列的指標，用以儲存使用者提供的新路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="0b650-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="0b650-110">緩衝區大小是最大路徑元素的 **TCHAR** 陣列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0b650-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="0b650-111">安裝應用程式所傳回的路徑資訊不應超過此大小。</span><span class="sxs-lookup"><span data-stu-id="0b650-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b650-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b650-112">Return value</span></span>

<span data-ttu-id="0b650-113">回呼常式應該會傳回下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="0b650-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="0b650-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0b650-114">Return code</span></span>                                                                                    | <span data-ttu-id="0b650-115">Description</span><span class="sxs-lookup"><span data-stu-id="0b650-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b650-116"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="0b650-117">媒體存在，而且要求的檔案可在 *Param2* 所指向的緩衝區中指定的路徑上取得。</span><span class="sxs-lookup"><span data-stu-id="0b650-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="0b650-118"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="0b650-119">略過要求的檔案</span><span class="sxs-lookup"><span data-stu-id="0b650-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="0b650-120"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="0b650-121">中止佇列處理。</span><span class="sxs-lookup"><span data-stu-id="0b650-121">Abort queue processing.</span></span> <span data-ttu-id="0b650-122">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函數會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0b650-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="0b650-123">GetLastError 會傳回擴充的錯誤資訊，例如， \_ 如果使用者取消，則會取消錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b650-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="0b650-124"><dt>**FILEOP-DOIT R**</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="0b650-125">媒體可供使用。</span><span class="sxs-lookup"><span data-stu-id="0b650-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="0b650-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b650-126">Requirements</span></span>



| <span data-ttu-id="0b650-127">需求</span><span class="sxs-lookup"><span data-stu-id="0b650-127">Requirement</span></span> | <span data-ttu-id="0b650-128">值</span><span class="sxs-lookup"><span data-stu-id="0b650-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b650-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b650-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0b650-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b650-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0b650-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b650-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0b650-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b650-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b650-133">標頭</span><span class="sxs-lookup"><span data-stu-id="0b650-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b650-134"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b650-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b650-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b650-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b650-136">概觀</span><span class="sxs-lookup"><span data-stu-id="0b650-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0b650-137">通知</span><span class="sxs-lookup"><span data-stu-id="0b650-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0b650-138">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="0b650-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="0b650-139">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="0b650-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="0b650-140">**來源 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="0b650-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




