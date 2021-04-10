---
title: 'SisRestoredLink 函式 (Sisbkup) '
description: 傳回指定的已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- SisRestoredLink 函式備份
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934103"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="ef0b6-104">SisRestoredLink 函式</span><span class="sxs-lookup"><span data-stu-id="ef0b6-104">SisRestoredLink function</span></span>

<span data-ttu-id="ef0b6-105">**SisRestoredLink** 函式會傳回指定之已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0b6-106">語法</span><span class="sxs-lookup"><span data-stu-id="ef0b6-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="ef0b6-107">參數</span><span class="sxs-lookup"><span data-stu-id="ef0b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0b6-108">*sisRestoreStructure* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-109">從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b6-110">*restoredFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-111">已還原之 SIS 連結檔的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b6-112">*reparseData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-113">SIS 重新分析點內容的指標。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="ef0b6-114">此重新分析點包含描述已還原之 SIS 連結的資料。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="ef0b6-115">若要取出檔案的重新分析點資料，請使用 [**FSCTL \_ 取得重新 \_ 分析 \_ 點**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b6-116">*reparseDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-117">*ReparseData* 所指向之 SIS 重新分析點的內容大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b6-118">*countOfCommonStoreFilesToRestore* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-119">*CommonStoreFilesToRestore* 參數中列出的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b6-120">*commonStoreFilesToRestore* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0b6-121">通用存放區檔案名陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="ef0b6-122">這些檔案應該與 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)所要求的一般存放區檔案相同的時間還原。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="ef0b6-123">如果 *countOfCommonStoreFilesToRestore* 參數的值不是0， *commonStoreFilesToRestore* 參數的值將會包含要在還原 SIS 連結後還原的通用存放區檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="ef0b6-124">如果值為0，則會傳回一般存放區檔案一次，或是磁片區上已有這些檔案。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef0b6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef0b6-125">Return value</span></span>

<span data-ttu-id="ef0b6-126">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="ef0b6-127">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef0b6-128">備註</span><span class="sxs-lookup"><span data-stu-id="ef0b6-128">Remarks</span></span>

<span data-ttu-id="ef0b6-129">您應該針對已還原的每個 SIS 連結呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="ef0b6-130">此函式會針對每個還原作業，最多傳回一次通用存放區檔案;任何嘗試還原其他會看到相同一般存放區檔案的 SIS 連結，都不會導致傳回該一般存放區的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="ef0b6-131">這項功能不會傳回一般存放區檔案，在備份作業期間不會傳回 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) 的呼叫，前提是儲存在媒體上的 SIS 重新分析資料尚未損毀。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="ef0b6-132">還原 SIS 連結時，您的還原作業應該只建立適當的稀疏檔案、將任何配置的範圍初始化，然後寫入與在備份作業期間讀取的 SIS 重新分析資料完全相同的資料。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="ef0b6-133">您的還原作業務必使用未配置的範圍建立稀疏檔案，而不是以零來初始化 (或非疏鬆檔案) 。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="ef0b6-134">請注意，如果通用存放區檔案仍存在於磁片上，則此函式不一定會識別備份媒體上的一組 SIS 連結所對應的通用存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="ef0b6-135">一般存放區檔案資料流程的內容永遠不會在建立後變更，因此如果該檔案已經存在於磁片上，就不需要將它還原。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="ef0b6-136">一般存放區檔案名是全域唯一的，可確保還原作業的完整性，即使它不是在備份作業已存取的相同 SIS 啟用磁片區上。</span><span class="sxs-lookup"><span data-stu-id="ef0b6-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0b6-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef0b6-137">Requirements</span></span>



| <span data-ttu-id="ef0b6-138">需求</span><span class="sxs-lookup"><span data-stu-id="ef0b6-138">Requirement</span></span> | <span data-ttu-id="ef0b6-139">值</span><span class="sxs-lookup"><span data-stu-id="ef0b6-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0b6-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef0b6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0b6-141">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ef0b6-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef0b6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0b6-143">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef0b6-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef0b6-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ef0b6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef0b6-145"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b6-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef0b6-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef0b6-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef0b6-147"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b6-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="ef0b6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0b6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0b6-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b6-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef0b6-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef0b6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0b6-151">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="ef0b6-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="ef0b6-152">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="ef0b6-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

