---
description: 如果檔案 \_ 複製作業期間發生錯誤，則會將 SPFILENOTIFY COPYERROR 通知傳送至回呼常式。
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: 'SPFILENOTIFY_COPYERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849599"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="fe0a5-103">SPFILENOTIFY \_ COPYERROR 訊息</span><span class="sxs-lookup"><span data-stu-id="fe0a5-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="fe0a5-104">如果檔案複製作業期間發生錯誤，則會將 **SPFILENOTIFY \_ COPYERROR** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="fe0a5-105">參數</span><span class="sxs-lookup"><span data-stu-id="fe0a5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0a5-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="fe0a5-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0a5-107">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe0a5-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="fe0a5-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0a5-109">緩衝區大小上限路徑字元的指標，可 \_ 儲存使用者指定的新路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0a5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe0a5-110">Return value</span></span>

<span data-ttu-id="fe0a5-111">回呼應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="fe0a5-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fe0a5-112">Return code</span></span>                                                                                    | <span data-ttu-id="fe0a5-113">Description</span><span class="sxs-lookup"><span data-stu-id="fe0a5-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe0a5-114"><dt>**FILEOP \_ 中止**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a5-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="fe0a5-115">應取消佇列處理。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-115">Queue processing should be canceled.</span></span> <span data-ttu-id="fe0a5-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回擴充的錯誤資訊，例如 \_ ，如果使用者取消) 或錯誤 \_ 記憶體不足，則會傳回錯誤 (\_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="fe0a5-117"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a5-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="fe0a5-118">使用回呼函式放在 *Param2* 參數所指向之緩衝區中的路徑，以重試複製作業。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="fe0a5-119">回呼常式應確定路徑不會溢位最大路徑元素之 TCHAR 陣列的緩衝區大小 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="fe0a5-120"><dt>**FILEOP \_ 重試**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a5-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="fe0a5-121">使用者正在嘗試複製操作。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="fe0a5-122"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a5-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="fe0a5-123">使用者即將略過檔案複製作業。</span><span class="sxs-lookup"><span data-stu-id="fe0a5-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="fe0a5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe0a5-124">Requirements</span></span>



| <span data-ttu-id="fe0a5-125">需求</span><span class="sxs-lookup"><span data-stu-id="fe0a5-125">Requirement</span></span> | <span data-ttu-id="fe0a5-126">值</span><span class="sxs-lookup"><span data-stu-id="fe0a5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0a5-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe0a5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0a5-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe0a5-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe0a5-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe0a5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0a5-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe0a5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe0a5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="fe0a5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0a5-132"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a5-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0a5-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe0a5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0a5-134">概觀</span><span class="sxs-lookup"><span data-stu-id="fe0a5-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="fe0a5-135">通知</span><span class="sxs-lookup"><span data-stu-id="fe0a5-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="fe0a5-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="fe0a5-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="fe0a5-137">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="fe0a5-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="fe0a5-138">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="fe0a5-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

