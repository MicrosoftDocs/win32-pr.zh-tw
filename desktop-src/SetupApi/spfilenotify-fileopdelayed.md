---
description: 當檔案作業因為檔案正在 \_ 使用中而延遲時，SetupInstallFileEx 或 SetupCommitFileQueue 會將 SPFILENOTIFY FILEOPDELAYED 通知傳送至回呼常式。 下次重新開機系統時，就會處理此作業。
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: 'SPFILENOTIFY_FILEOPDELAYED 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848828"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="dbed1-104">SPFILENOTIFY \_ FILEOPDELAYED 訊息</span><span class="sxs-lookup"><span data-stu-id="dbed1-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="dbed1-105">當檔案作業因為檔案正在使用中而延遲時， [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)或 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)會將 **SPFILENOTIFY \_ FILEOPDELAYED** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="dbed1-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="dbed1-106">下次重新開機系統時，就會處理此作業。</span><span class="sxs-lookup"><span data-stu-id="dbed1-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="dbed1-107">參數</span><span class="sxs-lookup"><span data-stu-id="dbed1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbed1-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="dbed1-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="dbed1-109">[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dbed1-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="dbed1-110">如果延遲的作業是檔案複製作業， [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) 結構會包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="dbed1-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="dbed1-111">FILEPATHS 成員</span><span class="sxs-lookup"><span data-stu-id="dbed1-111">FILEPATHS member</span></span> | <span data-ttu-id="dbed1-112">值</span><span class="sxs-lookup"><span data-stu-id="dbed1-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="dbed1-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="dbed1-113">**Win32Error**</span></span>   | <span data-ttu-id="dbed1-114">沒有 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="dbed1-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="dbed1-115">**旗標**</span><span class="sxs-lookup"><span data-stu-id="dbed1-115">**Flags**</span></span>        | <span data-ttu-id="dbed1-116">FILEOP \_ 複製</span><span class="sxs-lookup"><span data-stu-id="dbed1-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="dbed1-117">**來源**</span><span class="sxs-lookup"><span data-stu-id="dbed1-117">**Source**</span></span>       | <span data-ttu-id="dbed1-118">暫存檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dbed1-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="dbed1-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="dbed1-119">**Target**</span></span>       | <span data-ttu-id="dbed1-120">實際目標檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dbed1-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="dbed1-121">當系統重新開機時，此暫存檔案將會複製到目標目錄。</span><span class="sxs-lookup"><span data-stu-id="dbed1-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="dbed1-122">安裝函式會自動產生暫存檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="dbed1-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="dbed1-123">如果延遲的作業是檔案刪除作業， [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) 結構會包含下列資訊。</span><span class="sxs-lookup"><span data-stu-id="dbed1-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="dbed1-124">FILEPATHS 成員</span><span class="sxs-lookup"><span data-stu-id="dbed1-124">FILEPATHS member</span></span> | <span data-ttu-id="dbed1-125">值</span><span class="sxs-lookup"><span data-stu-id="dbed1-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="dbed1-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="dbed1-126">**Win32Error**</span></span>   | <span data-ttu-id="dbed1-127">沒有 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="dbed1-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="dbed1-128">**旗標**</span><span class="sxs-lookup"><span data-stu-id="dbed1-128">**Flags**</span></span>        | <span data-ttu-id="dbed1-129">FILEOP \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="dbed1-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="dbed1-130">**來源**</span><span class="sxs-lookup"><span data-stu-id="dbed1-130">**Source**</span></span>       | <span data-ttu-id="dbed1-131">NULL</span><span class="sxs-lookup"><span data-stu-id="dbed1-131">NULL</span></span>                                 |
| <span data-ttu-id="dbed1-132">**Target**</span><span class="sxs-lookup"><span data-stu-id="dbed1-132">**Target**</span></span>       | <span data-ttu-id="dbed1-133">要刪除之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dbed1-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="dbed1-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="dbed1-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="dbed1-135">未使用。</span><span class="sxs-lookup"><span data-stu-id="dbed1-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbed1-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbed1-136">Return value</span></span>

<span data-ttu-id="dbed1-137">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="dbed1-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbed1-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbed1-138">Requirements</span></span>



| <span data-ttu-id="dbed1-139">需求</span><span class="sxs-lookup"><span data-stu-id="dbed1-139">Requirement</span></span> | <span data-ttu-id="dbed1-140">值</span><span class="sxs-lookup"><span data-stu-id="dbed1-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbed1-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbed1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="dbed1-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbed1-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dbed1-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbed1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="dbed1-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbed1-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbed1-145">標頭</span><span class="sxs-lookup"><span data-stu-id="dbed1-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbed1-146"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbed1-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbed1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbed1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbed1-148">概觀</span><span class="sxs-lookup"><span data-stu-id="dbed1-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="dbed1-149">通知</span><span class="sxs-lookup"><span data-stu-id="dbed1-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="dbed1-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="dbed1-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="dbed1-151">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="dbed1-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="dbed1-152">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="dbed1-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="dbed1-153">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="dbed1-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="dbed1-154">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="dbed1-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




