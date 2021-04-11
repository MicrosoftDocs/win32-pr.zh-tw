---
title: 'SisCreateRestoreStructure 函式 (Sisbkup) '
description: 根據提供的資訊建立 SIS 還原結構。
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- SisCreateRestoreStructure 函式備份
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843307"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="42523-104">SisCreateRestoreStructure 函式</span><span class="sxs-lookup"><span data-stu-id="42523-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="42523-105">**SisCreateRestoreStructure** 函式會根據所提供的資訊建立 SIS 還原結構。</span><span class="sxs-lookup"><span data-stu-id="42523-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="42523-106">語法</span><span class="sxs-lookup"><span data-stu-id="42523-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="42523-107">參數</span><span class="sxs-lookup"><span data-stu-id="42523-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42523-108">*volumeRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42523-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42523-109">要備份之磁片區的磁片區根目錄（不含尾端反斜線）的檔案名。</span><span class="sxs-lookup"><span data-stu-id="42523-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="42523-110">例如，指定 "C：" 而非 "C： \\ "。</span><span class="sxs-lookup"><span data-stu-id="42523-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="42523-111">磁片區不能是系統或開機磁碟區。</span><span class="sxs-lookup"><span data-stu-id="42523-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="42523-112">*sisRestoreStructure* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42523-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42523-113">傳回 SIS 還原結構。</span><span class="sxs-lookup"><span data-stu-id="42523-113">Returned SIS restore structure.</span></span> <span data-ttu-id="42523-114">呼叫端應該將此結構視為不透明。</span><span class="sxs-lookup"><span data-stu-id="42523-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="42523-115">*commonStoreRootPathname* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42523-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42523-116">指定之磁片區通用存放區的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="42523-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="42523-117">例如 "c： \\ SIS Common Store"。</span><span class="sxs-lookup"><span data-stu-id="42523-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="42523-118">*countOfCommonStoreFilesToRestore* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42523-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42523-119">*CommonStoreFilesToRestore* 參數中列出的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="42523-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="42523-120">*commonStoreFilesToRestore* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42523-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42523-121">檔案名陣列的指標，指定 SIS 用來管理指定磁片區的內部檔案清單。</span><span class="sxs-lookup"><span data-stu-id="42523-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="42523-122">這些檔案應該與 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)所要求的一般存放區檔案相同的時間還原。</span><span class="sxs-lookup"><span data-stu-id="42523-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42523-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="42523-123">Return value</span></span>

<span data-ttu-id="42523-124">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="42523-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="42523-125">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="42523-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="42523-126">備註</span><span class="sxs-lookup"><span data-stu-id="42523-126">Remarks</span></span>

<span data-ttu-id="42523-127">此函數會以 [**SisCreateBackupStructure**](siscreatebackupstructure.md) 在指定磁片區上建立備份環境的方式，在指定的磁片區上建立還原環境。</span><span class="sxs-lookup"><span data-stu-id="42523-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="42523-128">請注意，如果通用存放區檔案或檔案仍存在於磁片上，則此函式不一定會識別備份媒體上的一組 SIS 連結所對應的通用存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="42523-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="42523-129">一般存放區檔案資料流程的內容永遠不會在建立後變更，因此如果該檔案已經存在於磁片上，就不需要將它還原。</span><span class="sxs-lookup"><span data-stu-id="42523-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="42523-130">一般存放區檔案名是全域唯一的，可確保還原作業的完整性，即使它不是在備份作業已存取的相同 SIS 啟用磁片區上。</span><span class="sxs-lookup"><span data-stu-id="42523-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="42523-131">還原作業完成之後，請呼叫 [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)，將 *commonStoreFilesToRestore* 字串陣列所使用的記憶體解除配置。</span><span class="sxs-lookup"><span data-stu-id="42523-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42523-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="42523-132">Requirements</span></span>



| <span data-ttu-id="42523-133">需求</span><span class="sxs-lookup"><span data-stu-id="42523-133">Requirement</span></span> | <span data-ttu-id="42523-134">值</span><span class="sxs-lookup"><span data-stu-id="42523-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42523-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42523-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42523-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42523-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="42523-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42523-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42523-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42523-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="42523-139">標頭</span><span class="sxs-lookup"><span data-stu-id="42523-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="42523-140"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="42523-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="42523-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="42523-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="42523-142"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42523-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="42523-143">DLL</span><span class="sxs-lookup"><span data-stu-id="42523-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42523-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42523-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42523-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42523-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42523-146">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="42523-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="42523-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="42523-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="42523-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="42523-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="42523-149">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="42523-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

