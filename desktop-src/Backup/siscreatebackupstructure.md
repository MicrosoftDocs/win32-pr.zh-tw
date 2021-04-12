---
title: 'SisCreateBackupStructure 函式 (Sisbkup) '
description: 根據提供的資訊建立 SIS 備份結構。
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- SisCreateBackupStructure 函式備份
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464781"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="5a777-104">SisCreateBackupStructure 函式</span><span class="sxs-lookup"><span data-stu-id="5a777-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="5a777-105">**SisCreateBackupStructure** 函式會根據所提供的資訊建立 SIS 備份結構。</span><span class="sxs-lookup"><span data-stu-id="5a777-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a777-106">語法</span><span class="sxs-lookup"><span data-stu-id="5a777-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="5a777-107">參數</span><span class="sxs-lookup"><span data-stu-id="5a777-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a777-108">*volumeRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a777-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a777-109">要備份之磁片區的磁片區根目錄（不含尾端反斜線）的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5a777-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="5a777-110">例如，指定 "C：" 而非 "C： \\ "。</span><span class="sxs-lookup"><span data-stu-id="5a777-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="5a777-111">*sisBackupStructure* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a777-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a777-112">傳回 SIS 備份結構。</span><span class="sxs-lookup"><span data-stu-id="5a777-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a777-113">*commonStoreRootPathname* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a777-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a777-114">指定之磁片區通用存放區的完整路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="5a777-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="5a777-115">例如 "c： \\ SIS Common Store"。</span><span class="sxs-lookup"><span data-stu-id="5a777-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="5a777-116">*countOfCommonStoreFilesToBackUp* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a777-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a777-117">*CommonStoreFilesToBackUp* 參數中列出的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="5a777-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5a777-118">*commonStoreFilesToBackUp* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a777-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a777-119">檔案名陣列的指標，指定 SIS 用來管理指定磁片區的內部檔案清單。</span><span class="sxs-lookup"><span data-stu-id="5a777-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="5a777-120">這些檔案應該同時以 SisCSFilesToBackupForLink 所要求的一般存放區檔案相同的方式進行備份。 [ ](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="5a777-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a777-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a777-121">Return value</span></span>

<span data-ttu-id="5a777-122">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5a777-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="5a777-123">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5a777-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a777-124">備註</span><span class="sxs-lookup"><span data-stu-id="5a777-124">Remarks</span></span>

<span data-ttu-id="5a777-125">此函式會建立 SIS 備份結構，由 SIS 備份 API 用來建立和維護磁片區上的檔案連結清單，以及連結所指向的原始檔案連結。</span><span class="sxs-lookup"><span data-stu-id="5a777-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="5a777-126">針對每個備份已啟用 SIS 的磁片區，應該只呼叫一次此函數。</span><span class="sxs-lookup"><span data-stu-id="5a777-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="5a777-127">指定磁片區中的所有檔案都應該視為一般存放區檔案，而且只有在 SIS 指出應該時，才會進行備份。</span><span class="sxs-lookup"><span data-stu-id="5a777-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="5a777-128">*CountOfCommonStoreFilesToBackUp* 和 *commonStoreFilesToBackUp* 參數會一起傳回必須備份的檔案清單，而不論備份的連結為何。</span><span class="sxs-lookup"><span data-stu-id="5a777-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="5a777-129">如果 *countOfCommonStoreFilesToBackUp* 為0，則 *CommonStoreFilesToBackUp* 可能是 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="5a777-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="5a777-130">應忽略 *commonStoreFilesToBackUp* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="5a777-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="5a777-131">備份作業完成之後，請呼叫 [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)，將 *commonStoreFilesToBackUp* 字串陣列所使用的記憶體解除配置。</span><span class="sxs-lookup"><span data-stu-id="5a777-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a777-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a777-132">Requirements</span></span>



| <span data-ttu-id="5a777-133">需求</span><span class="sxs-lookup"><span data-stu-id="5a777-133">Requirement</span></span> | <span data-ttu-id="5a777-134">值</span><span class="sxs-lookup"><span data-stu-id="5a777-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a777-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a777-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a777-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a777-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5a777-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a777-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a777-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a777-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a777-139">標頭</span><span class="sxs-lookup"><span data-stu-id="5a777-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a777-140"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a777-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a777-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a777-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a777-142"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a777-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a777-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5a777-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a777-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a777-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a777-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a777-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a777-146">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="5a777-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="5a777-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="5a777-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="5a777-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="5a777-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

