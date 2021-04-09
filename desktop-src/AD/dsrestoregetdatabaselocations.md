---
title: 'DsRestoreGetDatabaseLocations 函式 (Ntdsbcli) '
description: 取得還原作業期間應該複本備份檔的位置。
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- DsRestoreGetDatabaseLocations 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843904"
---
# <a name="dsrestoregetdatabaselocations-function"></a><span data-ttu-id="53bd6-104">DsRestoreGetDatabaseLocations 函式</span><span class="sxs-lookup"><span data-stu-id="53bd6-104">DsRestoreGetDatabaseLocations function</span></span>

<span data-ttu-id="53bd6-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="53bd6-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="53bd6-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="53bd6-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="53bd6-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="53bd6-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="53bd6-108">**DsRestoreGetDatabaseLocations** 函式會取得還原作業期間應該複本備份檔的位置。</span><span class="sxs-lookup"><span data-stu-id="53bd6-108">The **DsRestoreGetDatabaseLocations** function obtains the locations where backup files should be copied during a restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="53bd6-109">語法</span><span class="sxs-lookup"><span data-stu-id="53bd6-109">Syntax</span></span>


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="53bd6-110">參數</span><span class="sxs-lookup"><span data-stu-id="53bd6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53bd6-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53bd6-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-112">包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="53bd6-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="53bd6-113">*pszDatabaseLocationList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53bd6-113">*pszDatabaseLocationList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-114">字串指標的指標，該指標會以 UNC 路徑的形式接收資料庫位置清單。</span><span class="sxs-lookup"><span data-stu-id="53bd6-114">Pointer to a string pointer that receives the list of database locations as UNC paths.</span></span> <span data-ttu-id="53bd6-115">這份清單會接收以雙 null 結束的單一 null 結束字串清單。</span><span class="sxs-lookup"><span data-stu-id="53bd6-115">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="53bd6-116">這個緩衝區是由 **DsRestoreGetDatabaseLocations** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。</span><span class="sxs-lookup"><span data-stu-id="53bd6-116">This buffer is allocated by the **DsRestoreGetDatabaseLocations** function and must be freed when it is no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="53bd6-117">每個檔案名的第一個字元都包含識別名稱類型的其中一個 [**BFT 常數**](bft-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="53bd6-117">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the name type.</span></span> <span data-ttu-id="53bd6-118">**DsRestoreGetDatabaseLocations** 函式只會提供下列名稱類型。</span><span class="sxs-lookup"><span data-stu-id="53bd6-118">The **DsRestoreGetDatabaseLocations** function only supplies the following name types.</span></span>

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span data-ttu-id="53bd6-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**</span><span class="sxs-lookup"><span data-stu-id="53bd6-119"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>


</dt> <dd>

<span data-ttu-id="53bd6-120">應該將 NTDS 資料庫檔案複製到此檔案。</span><span class="sxs-lookup"><span data-stu-id="53bd6-120">The NTDS database file should be copied to this file.</span></span> <span data-ttu-id="53bd6-121">這是在執行備份時識別為 **BFT \_ NTDS \_ 資料庫** 的檔案。</span><span class="sxs-lookup"><span data-stu-id="53bd6-121">This is the file that was identified as **BFT\_NTDS\_DATABASE** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span data-ttu-id="53bd6-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ 記錄檔 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="53bd6-122"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="53bd6-123">所有記錄檔都會複製到這個目錄。</span><span class="sxs-lookup"><span data-stu-id="53bd6-123">All log files are copied to this directory.</span></span> <span data-ttu-id="53bd6-124">執行備份時，會將記錄檔識別為 **BFT \_ 記錄** 檔。</span><span class="sxs-lookup"><span data-stu-id="53bd6-124">The log files were identified as **BFT\_LOG** when the backup was performed.</span></span>

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span data-ttu-id="53bd6-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ 檢查點 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="53bd6-125"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>


</dt> <dd>

<span data-ttu-id="53bd6-126">所有修補檔都會複製到這個目錄。</span><span class="sxs-lookup"><span data-stu-id="53bd6-126">All patch files are copied to this directory.</span></span> <span data-ttu-id="53bd6-127">執行備份時，會將修補檔案識別為 **BFT \_ 修補程式 \_** 檔案。</span><span class="sxs-lookup"><span data-stu-id="53bd6-127">The patch files were identified as **BFT\_PATCH\_FILE** when the backup was performed.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="53bd6-128">*pcbSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53bd6-128">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-129">**DWORD** 值的指標，此值會接收 *pszDatabaseLocationList* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="53bd6-129">Pointer to **DWORD** value that receives the size, in bytes, of the *pszDatabaseLocationList* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53bd6-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="53bd6-130">Return value</span></span>

<span data-ttu-id="53bd6-131">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53bd6-131">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="53bd6-132">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="53bd6-132">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="53bd6-133">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="53bd6-133">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-134">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="53bd6-134">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="53bd6-135">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="53bd6-135">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="53bd6-136">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="53bd6-136">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-137">*hbc*、 *pszDatabaseLocationList* 或 *pcbSize* 無效。</span><span class="sxs-lookup"><span data-stu-id="53bd6-137">*hbc*, *pszDatabaseLocationList*, or *pcbSize* are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53bd6-138">**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="53bd6-138">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="53bd6-139">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="53bd6-139">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53bd6-140">備註</span><span class="sxs-lookup"><span data-stu-id="53bd6-140">Remarks</span></span>

<span data-ttu-id="53bd6-141">**DsRestoreGetDatabaseLocations** 函數可以用來取得還原目錄，而不需要存取備份的資料。</span><span class="sxs-lookup"><span data-stu-id="53bd6-141">The **DsRestoreGetDatabaseLocations** function can be used to obtain the restoration directories without access to the backed up data.</span></span> <span data-ttu-id="53bd6-142">若要這樣做，請使用 **Null** 來呼叫 *PvExpiryToken* 參數的 [**DsRestorePrepare**](dsrestoreprepare.md) 。</span><span class="sxs-lookup"><span data-stu-id="53bd6-142">To do this, call [**DsRestorePrepare**](dsrestoreprepare.md) with **NULL** for the *pvExpiryToken* parameter.</span></span> <span data-ttu-id="53bd6-143">這會導致 **DsRestorePrepare** 傳回受限的內容控制碼，此控制碼只能與 **DsRestoreGetDatabaseLocations** 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="53bd6-143">This causes **DsRestorePrepare** to return a restricted context handle which can only be used with the **DsRestoreGetDatabaseLocations** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="53bd6-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="53bd6-144">Requirements</span></span>



| <span data-ttu-id="53bd6-145">需求</span><span class="sxs-lookup"><span data-stu-id="53bd6-145">Requirement</span></span> | <span data-ttu-id="53bd6-146">值</span><span class="sxs-lookup"><span data-stu-id="53bd6-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53bd6-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53bd6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="53bd6-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53bd6-148">Windows Vista</span></span><br/>                                                                              |
| <span data-ttu-id="53bd6-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53bd6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="53bd6-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53bd6-150">Windows Server 2008</span></span><br/>                                                                        |
| <span data-ttu-id="53bd6-151">標頭</span><span class="sxs-lookup"><span data-stu-id="53bd6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="53bd6-152"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="53bd6-152"><dt>Ntdsbcli.h</dt></span></span> </dl>                 |
| <span data-ttu-id="53bd6-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="53bd6-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="53bd6-154"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="53bd6-154"><dt>Ntdsbcli.lib</dt></span></span> </dl>               |
| <span data-ttu-id="53bd6-155">DLL</span><span class="sxs-lookup"><span data-stu-id="53bd6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53bd6-156"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53bd6-156"><dt>Ntdsbcli.dll</dt></span></span> </dl>               |
| <span data-ttu-id="53bd6-157">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="53bd6-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53bd6-158">**DsRestoreGetDatabaseLocationsW** (Unicode) 和 **DsRestoreGetDatabaseLocationsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="53bd6-158">**DsRestoreGetDatabaseLocationsW** (Unicode) and **DsRestoreGetDatabaseLocationsA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53bd6-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53bd6-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53bd6-160">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="53bd6-160">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="53bd6-161">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="53bd6-161">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="53bd6-162">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="53bd6-162">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="53bd6-163">還原 Active Directory</span><span class="sxs-lookup"><span data-stu-id="53bd6-163">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> </dl>

 

