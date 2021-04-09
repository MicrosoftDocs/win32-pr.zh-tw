---
title: 'DsBackupGetBackupLogs 函式 (Ntdsbcli) '
description: 取得必須針對指定的備份內容備份的記錄檔清單。
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- DsBackupGetBackupLogs 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934496"
---
# <a name="dsbackupgetbackuplogs-function"></a><span data-ttu-id="b369f-104">DsBackupGetBackupLogs 函式</span><span class="sxs-lookup"><span data-stu-id="b369f-104">DsBackupGetBackupLogs function</span></span>

<span data-ttu-id="b369f-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b369f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b369f-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b369f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b369f-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="b369f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b369f-108">**DsBackupGetBackupLogs** 函數會取得必須針對指定的備份內容備份的記錄檔清單。</span><span class="sxs-lookup"><span data-stu-id="b369f-108">The **DsBackupGetBackupLogs** function obtains the list of log files that must be backed up for the given backup context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b369f-109">語法</span><span class="sxs-lookup"><span data-stu-id="b369f-109">Syntax</span></span>


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="b369f-110">參數</span><span class="sxs-lookup"><span data-stu-id="b369f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b369f-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b369f-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b369f-112">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="b369f-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b369f-113">*pszBackupLogFiles* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b369f-113">*pszBackupLogFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b369f-114">字串指標的指標，該指標會以 UNC 路徑的形式接收記錄檔名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="b369f-114">Pointer to a string pointer that receives the list of log file names as UNC paths.</span></span> <span data-ttu-id="b369f-115">在呼叫 **DsBackupGetBackupLogs** 之前，將此值初始化為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b369f-115">Initialize this value to **NULL** before calling **DsBackupGetBackupLogs**.</span></span>

<span data-ttu-id="b369f-116">這份清單會接收以雙 null 結束的單一 null 結束字串清單。</span><span class="sxs-lookup"><span data-stu-id="b369f-116">This list receives a double null-terminated list of single null-terminated strings.</span></span>

<span data-ttu-id="b369f-117">這個緩衝區是由 **DsBackupGetBackupLogs** 函式所配置，且必須在呼叫 [**DsBackupFree**](dsbackupfree.md) 函式不再需要時釋放。</span><span class="sxs-lookup"><span data-stu-id="b369f-117">This buffer is allocated by the **DsBackupGetBackupLogs** function and must be freed when no longer required by calling the [**DsBackupFree**](dsbackupfree.md) function.</span></span>

<span data-ttu-id="b369f-118">每個檔案名的第一個字元都包含識別名稱類型的其中一個 [**BFT 常數**](bft-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="b369f-118">The first character of each of the file names contains one of the [**BFT Constants**](bft-constants.md) that identifies the type of name.</span></span>

</dd> <dt>

<span data-ttu-id="b369f-119">*pcbSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b369f-119">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b369f-120">**DWORD** 值的指標，此值會接收 *pszBackupLogFiles* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b369f-120">Pointer to **DWORD** value that receives the size, in bytes, of the *pszBackupLogFiles* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b369f-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="b369f-121">Return value</span></span>

<span data-ttu-id="b369f-122">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b369f-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="b369f-123">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="b369f-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="b369f-124">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="b369f-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="b369f-125">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="b369f-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="b369f-126">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="b369f-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="b369f-127">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="b369f-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b369f-128">*hbc*、 *pszBackupLogFiles* 或 *pcbSize* 無效。</span><span class="sxs-lookup"><span data-stu-id="b369f-128">*hbc*, *pszBackupLogFiles*, or *pcbSize* is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b369f-129">**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="b369f-129">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="b369f-130">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="b369f-130">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b369f-131">備註</span><span class="sxs-lookup"><span data-stu-id="b369f-131">Remarks</span></span>

<span data-ttu-id="b369f-132">**DsBackupGetBackupLogs** 函數會提供備份所需的記錄檔清單。</span><span class="sxs-lookup"><span data-stu-id="b369f-132">The **DsBackupGetBackupLogs** function provides a list of the log files necessary for a backup.</span></span> <span data-ttu-id="b369f-133">完整備份是由 [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) 函數和記錄檔所提供的資料庫檔案所組成。</span><span class="sxs-lookup"><span data-stu-id="b369f-133">A full backup consists of the database files provided by the [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) function and the log files.</span></span> <span data-ttu-id="b369f-134">不支援 Active Directory 伺服器的增量備份。</span><span class="sxs-lookup"><span data-stu-id="b369f-134">Incremental backups of Active Directory servers are not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b369f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="b369f-135">Requirements</span></span>



| <span data-ttu-id="b369f-136">需求</span><span class="sxs-lookup"><span data-stu-id="b369f-136">Requirement</span></span> | <span data-ttu-id="b369f-137">值</span><span class="sxs-lookup"><span data-stu-id="b369f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b369f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b369f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b369f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b369f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b369f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b369f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b369f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b369f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b369f-142">標頭</span><span class="sxs-lookup"><span data-stu-id="b369f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b369f-143"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="b369f-143"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="b369f-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="b369f-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b369f-145"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b369f-145"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="b369f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b369f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b369f-147"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b369f-147"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="b369f-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b369f-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b369f-149">**DsBackupGetBackupLogsW** (Unicode) 和 **DsBackupGetBackupLogsA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b369f-149">**DsBackupGetBackupLogsW** (Unicode) and **DsBackupGetBackupLogsA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="b369f-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b369f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b369f-151">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="b369f-151">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="b369f-152">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="b369f-152">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="b369f-153">**BFT 常數**</span><span class="sxs-lookup"><span data-stu-id="b369f-153">**BFT Constants**</span></span>](bft-constants.md)
</dt> <dt>

[<span data-ttu-id="b369f-154">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="b369f-154">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="b369f-155">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="b369f-155">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

