---
title: 'SisCSFilesToBackupForLink 函式 (Sisbkup) '
description: 傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- SisCSFilesToBackupForLink 函式備份
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969571"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="ce5a1-104">SisCSFilesToBackupForLink 函式</span><span class="sxs-lookup"><span data-stu-id="ce5a1-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="ce5a1-105">**SisCSFilesToBackupForLink** 函式會傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5a1-106">語法</span><span class="sxs-lookup"><span data-stu-id="ce5a1-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="ce5a1-107">參數</span><span class="sxs-lookup"><span data-stu-id="ce5a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5a1-108">*sisBackupStructure* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-109">從 [**SisCreateBackupStructure**](siscreatebackupstructure.md)傳回之 SIS 備份結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-110">*reparseData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-111">SIS 重新分析點內容的指標。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="ce5a1-112">此重新分析點包含描述 SIS 連結的資料。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="ce5a1-113">若要取出檔案的重新分析點資料，請使用 [**FSCTL \_ 取得重新 \_ 分析 \_ 點**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-114">*reparseDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-115">*ReparseData* 所指向之 SIS 重新分析點的內容大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-116">*thisFileCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-117">呼叫此函式的備份應用程式所提供的內容字串指標。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="ce5a1-118">此內容字串的內容完全由這個備份應用程式所決定，且不會由 SIS 備份 API 來解讀。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="ce5a1-119">這個參數是選擇性的;如果未使用，請將此參數的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ce5a1-120">在此情況下，將不會處理此參數的值。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-121">*matchingFileCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-122">在此函式的前四個參數中傳遞的資訊所識別之 SIS 連結的內容字串的雙向間接指標。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="ce5a1-123">這個參數是選擇性的;如果未提供內容字串做為 *thisFileCoNtext* 參數的值，請將此參數的值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="ce5a1-124">在此情況下，將不會處理此參數的值。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-125">*countOfCommonStoreFilesToBackUp* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-126">*CommonStoreFilesToBackUp* 參數中列出的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ce5a1-127">*commonStoreFilesToBackUp* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5a1-128">檔案名陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-128">Pointer to an array of file names.</span></span> <span data-ttu-id="ce5a1-129">這些檔案應該同時以 [**SisCreateBackupStructure**](siscreatebackupstructure.md)所要求的一般存放區檔案相同的方式進行備份。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5a1-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce5a1-130">Return value</span></span>

<span data-ttu-id="ce5a1-131">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="ce5a1-132">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5a1-133">備註</span><span class="sxs-lookup"><span data-stu-id="ce5a1-133">Remarks</span></span>

<span data-ttu-id="ce5a1-134">備份應用程式應該只針對每個要備份的 SIS 連結檔案呼叫此函數一次。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="ce5a1-135">備份應用程式可以依標記的 IO 重新 \_ 分析標記 sis 來識別 sis 重新分析點 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="ce5a1-136">此標記定義于 Winnt. h 中。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="ce5a1-137">如果由 *reparseData* 參數的值所識別的重新分析點描述要備份之檔案的第一個實例，此函式會傳回 **Null** 做為 *matchingFileCoNtext* 參數的值，並將字串的 *commonStoreFilesToBackUp* 陣列值初始化為通用存放區檔案的名稱，或要備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="ce5a1-138">否則，此函式會將 *matchingFileCoNtext* 參數的值設定為對應到指定檔案之第一個實例的內容字串，並將 *countOfCommonStoreFilesToBackUp* 參數的值設定為0。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="ce5a1-139">如果有多個通用存放區檔案對應到指定的連結， *thisFileCoNtext* 參數的值將會是對應于陣列中傳回的第一個通用存放區檔案（commonStoreFilesToBackUp 0）的內容字串 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="ce5a1-140">此函式的目前版本最多隻會傳回一個通用存放區檔案，但在未來的版本中，可能會有數個常見存放區檔案支援的單一連結，例如，檔案中的每個資料流程各有一個，因此您的備份應用程式應該在每次呼叫此函式時支援多個檔案。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="ce5a1-141">在任何情況下，每個備份階段最多會傳回一次通用存放區檔案。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="ce5a1-142">您的備份應用程式應該備份或還原一般存放區檔案，或是以 *commonStoreFilesToBackUp* 參數中所傳回的檔案名或檔案名所識別的檔案。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="ce5a1-143">無論是否有對應的一般存放區檔案，您的備份應用程式都應該備份存在於磁片上的 SIS 連結檔案，例如重新分析點和稀疏檔案，而且很可能不會填入任何範圍。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="ce5a1-144">您的備份應用程式可能會立即備份或還原一般存放區檔案、延遲備份，或視需要將它們組合在一起。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="ce5a1-145">備份作業完成之後，請呼叫 [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)，將 *commonStoreFilesToBackUp* 字串陣列所使用的記憶體解除配置。</span><span class="sxs-lookup"><span data-stu-id="ce5a1-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5a1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce5a1-146">Requirements</span></span>



| <span data-ttu-id="ce5a1-147">需求</span><span class="sxs-lookup"><span data-stu-id="ce5a1-147">Requirement</span></span> | <span data-ttu-id="ce5a1-148">值</span><span class="sxs-lookup"><span data-stu-id="ce5a1-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5a1-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce5a1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ce5a1-150">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ce5a1-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce5a1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ce5a1-152">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce5a1-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ce5a1-153">標頭</span><span class="sxs-lookup"><span data-stu-id="ce5a1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce5a1-154"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5a1-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce5a1-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce5a1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce5a1-156"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce5a1-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce5a1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ce5a1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce5a1-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce5a1-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5a1-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce5a1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5a1-160">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="ce5a1-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="ce5a1-161">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="ce5a1-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

