---
description: '\_SetupIterateCabinet 會將 SPFILENOTIFY FILEEXTRACTED 通知傳送至回呼常式，表示檔案已從封包解壓縮，或是解壓縮失敗，並已取消封包處理。'
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: 'SPFILENOTIFY_FILEEXTRACTED 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980682"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="02b28-103">SPFILENOTIFY \_ FILEEXTRACTED 訊息</span><span class="sxs-lookup"><span data-stu-id="02b28-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="02b28-104">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)會將 **SPFILENOTIFY \_ FILEEXTRACTED** 通知傳送至回呼常式，表示檔案已從封包解壓縮，或是解壓縮失敗，並已取消封包處理。</span><span class="sxs-lookup"><span data-stu-id="02b28-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="02b28-105">參數</span><span class="sxs-lookup"><span data-stu-id="02b28-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b28-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="02b28-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="02b28-107">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含解壓縮檔案的路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="02b28-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="02b28-108">**FILEPATHS** 結構的 **SourceFile** 成員包含封包的完整來源路徑。</span><span class="sxs-lookup"><span data-stu-id="02b28-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="02b28-109">**TargetFile** 成員會提供要安裝在系統上之檔案的完整目標路徑。</span><span class="sxs-lookup"><span data-stu-id="02b28-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="02b28-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="02b28-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="02b28-111">未使用的。</span><span class="sxs-lookup"><span data-stu-id="02b28-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b28-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="02b28-112">Return value</span></span>

<span data-ttu-id="02b28-113">封包回呼常式應該會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="02b28-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="02b28-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="02b28-114">Return code</span></span>                                                                               | <span data-ttu-id="02b28-115">Description</span><span class="sxs-lookup"><span data-stu-id="02b28-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02b28-116"><dt>**沒有 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="02b28-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="02b28-117">未發生任何錯誤，請繼續處理封包。</span><span class="sxs-lookup"><span data-stu-id="02b28-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="02b28-118"><dt>**錯誤 \_ XXX**</dt></span><span class="sxs-lookup"><span data-stu-id="02b28-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="02b28-119">發生指定的類型時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b28-119">An error of the specified type occurred.</span></span> <span data-ttu-id="02b28-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="02b28-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="02b28-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 將會傳回指定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="02b28-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="02b28-122">安裝程式 API 未提供預設的封包回呼常式。</span><span class="sxs-lookup"><span data-stu-id="02b28-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="02b28-123">您的安裝應用程式應該提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 函式所傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="02b28-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02b28-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="02b28-124">Requirements</span></span>



| <span data-ttu-id="02b28-125">需求</span><span class="sxs-lookup"><span data-stu-id="02b28-125">Requirement</span></span> | <span data-ttu-id="02b28-126">值</span><span class="sxs-lookup"><span data-stu-id="02b28-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02b28-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02b28-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02b28-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02b28-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="02b28-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02b28-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02b28-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02b28-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02b28-131">標頭</span><span class="sxs-lookup"><span data-stu-id="02b28-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b28-132"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="02b28-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b28-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02b28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b28-134">概觀</span><span class="sxs-lookup"><span data-stu-id="02b28-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="02b28-135">通知</span><span class="sxs-lookup"><span data-stu-id="02b28-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="02b28-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="02b28-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="02b28-137">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="02b28-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

