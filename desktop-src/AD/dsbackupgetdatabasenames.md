---
title: 'DsBackupGetDatabaseNames 函式 (Ntdsbcli) '
description: 取得要針對指定的備份內容備份的資料庫檔案清單。
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- DsBackupGetDatabaseNames 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465588"
---
# <a name="dsbackupgetdatabasenames-function"></a><span data-ttu-id="53438-104">DsBackupGetDatabaseNames 函式</span><span class="sxs-lookup"><span data-stu-id="53438-104">DsBackupGetDatabaseNames function</span></span>

<span data-ttu-id="53438-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="53438-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="53438-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="53438-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="53438-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="53438-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="53438-108">**DsBackupGetDatabaseNames** 函式會取得要針對指定的備份內容備份的資料庫檔案清單。</span><span class="sxs-lookup"><span data-stu-id="53438-108">The **DsBackupGetDatabaseNames** function obtains the list of database files to be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="53438-109">語法</span><span class="sxs-lookup"><span data-stu-id="53438-109">Syntax</span></span>


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="53438-110">參數</span><span class="sxs-lookup"><span data-stu-id="53438-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53438-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53438-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53438-112">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="53438-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="53438-113">*pszAttachmentInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53438-113">*pszAttachmentInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53438-114">字串指標的指標，該指標會以 UNC 路徑的形式接收資料庫檔案名的清單。</span><span class="sxs-lookup"><span data-stu-id="53438-114">Pointer to a string pointer that receives the list of database file names as UNC paths.</span></span> <span data-ttu-id="53438-115">在呼叫 **DsBackupGetDatabaseNames** 之前，必須將此值初始化為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="53438-115">This value must be initialized to **NULL** prior to calling **DsBackupGetDatabaseNames**.</span></span>

<span data-ttu-id="53438-116">這份清單會接收以雙 null 結束的單一 null 結束字串清單。</span><span class="sxs-lookup"><span data-stu-id="53438-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="53438-117">這個緩衝區是由 **DsBackupGetDatabaseNames** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。</span><span class="sxs-lookup"><span data-stu-id="53438-117">This buffer is allocated by the **DsBackupGetDatabaseNames** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="53438-118">每個檔案名的第一個字元都包含一個識別名稱類型的 [**BFT 常數**](bft-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="53438-118">The first character of each file name contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span> <span data-ttu-id="53438-119">[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函數只會提供下列類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="53438-119">The [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function only supplies the following types of names.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="53438-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**</span><span class="sxs-lookup"><span data-stu-id="53438-120"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="53438-121">檔案是 NTDS 資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="53438-121">The file is an NTDS database file.</span></span> <span data-ttu-id="53438-122">當還原資料時，應該將此檔案複製到識別為 **BFT \_ NTDS \_ 資料庫** 的檔案。</span><span class="sxs-lookup"><span data-stu-id="53438-122">This file should be copied to the file identified as **BFT\_NTDS\_DATABASE** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span data-ttu-id="53438-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="53438-123"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>


</dt> <dd>

<span data-ttu-id="53438-124">檔案是記錄檔。</span><span class="sxs-lookup"><span data-stu-id="53438-124">The file is a log file.</span></span> <span data-ttu-id="53438-125">還原資料時，會將所有記錄檔複製到識別為 **BFT \_ 記錄 \_** 檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="53438-125">All log files are copied to the directory identified as **BFT\_LOG\_DIR** when the data is restored.</span></span>

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span data-ttu-id="53438-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ 修補 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="53438-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>


</dt> <dd>

<span data-ttu-id="53438-127">檔案是修補檔案。</span><span class="sxs-lookup"><span data-stu-id="53438-127">The file is a patch file.</span></span> <span data-ttu-id="53438-128">還原資料時，會將所有修補檔案複製到識別為 **BFT \_ 檢查點 \_** 目錄的目錄。</span><span class="sxs-lookup"><span data-stu-id="53438-128">All patch files are copied to the directory identified as **BFT\_CHECKPOINT\_DIR** when the data is restored.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="53438-129">*pcbSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53438-129">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53438-130">**DWORD** 值的指標，此值會接收 *pszAttachmentInfo* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="53438-130">Pointer to **DWORD** value that receives the size, in bytes, of the *pszAttachmentInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53438-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="53438-131">Return value</span></span>

<span data-ttu-id="53438-132">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53438-132">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="53438-133">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="53438-133">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="53438-134">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="53438-134">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="53438-135">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53438-135">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="53438-136">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="53438-136">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="53438-137">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="53438-137">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="53438-138">*hbc*、 *pszAttachmentInfo* 或 *pcbSize* 無效。</span><span class="sxs-lookup"><span data-stu-id="53438-138">*hbc*, *pszAttachmentInfo*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53438-139">**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="53438-139">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="53438-140">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="53438-140">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53438-141">備註</span><span class="sxs-lookup"><span data-stu-id="53438-141">Remarks</span></span>

<span data-ttu-id="53438-142">**DsBackupGetDatabaseNames** 函數會提供備份所需的資料庫檔案清單。</span><span class="sxs-lookup"><span data-stu-id="53438-142">The **DsBackupGetDatabaseNames** function provides a list of the database files necessary for a backup.</span></span> <span data-ttu-id="53438-143">完整備份是由 [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) 函數所提供的資料庫檔案和記錄檔所組成。</span><span class="sxs-lookup"><span data-stu-id="53438-143">A full backup consists of the database files and the log files provided by the [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) function.</span></span> <span data-ttu-id="53438-144">不支援 Active Directory 伺服器的增量備份。</span><span class="sxs-lookup"><span data-stu-id="53438-144">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="53438-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="53438-145">Requirements</span></span>



| <span data-ttu-id="53438-146">需求</span><span class="sxs-lookup"><span data-stu-id="53438-146">Requirement</span></span> | <span data-ttu-id="53438-147">值</span><span class="sxs-lookup"><span data-stu-id="53438-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53438-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53438-148">Minimum supported client</span></span><br/> | <span data-ttu-id="53438-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53438-149">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="53438-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53438-150">Minimum supported server</span></span><br/> | <span data-ttu-id="53438-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53438-151">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="53438-152">標頭</span><span class="sxs-lookup"><span data-stu-id="53438-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="53438-153"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="53438-153"><dt>Ntdsbcli.h</dt></span></span> </dl>       |
| <span data-ttu-id="53438-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="53438-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="53438-155"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="53438-155"><dt>Ntdsbcli.lib</dt></span></span> </dl>     |
| <span data-ttu-id="53438-156">DLL</span><span class="sxs-lookup"><span data-stu-id="53438-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53438-157"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53438-157"><dt>Ntdsbcli.dll</dt></span></span> </dl>     |
| <span data-ttu-id="53438-158">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="53438-158">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53438-159">**DsBackupGetDatabaseNamesW** (Unicode) 和 **DsBackupGetDatabaseNamesA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="53438-159">**DsBackupGetDatabaseNamesW** (Unicode) and **DsBackupGetDatabaseNamesA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53438-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53438-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53438-161">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="53438-161">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="53438-162">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="53438-162">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="53438-163">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="53438-163">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="53438-164">**BFT 常數**</span><span class="sxs-lookup"><span data-stu-id="53438-164">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="53438-165">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="53438-165">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="53438-166">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="53438-166">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

