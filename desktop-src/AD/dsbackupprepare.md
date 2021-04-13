---
title: 'DsBackupPrepare 函式 (Ntdsbcli) '
description: 準備指定伺服器上的目錄以進行線上備份，並傳回後續呼叫其他備份函式時所使用的備份內容控制碼。
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- DsBackupPrepare 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465585"
---
# <a name="dsbackupprepare-function"></a><span data-ttu-id="b596a-104">DsBackupPrepare 函式</span><span class="sxs-lookup"><span data-stu-id="b596a-104">DsBackupPrepare function</span></span>

<span data-ttu-id="b596a-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b596a-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b596a-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b596a-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b596a-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="b596a-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b596a-108">**DsBackupPrepare** 函式會在指定的伺服器上準備線上備份的目錄，並傳回後續呼叫其他備份函式時所使用的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="b596a-108">The **DsBackupPrepare** function prepares the directory on the specified server for the online backup and returns a backup context handle used in subsequent calls to other backup functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b596a-109">語法</span><span class="sxs-lookup"><span data-stu-id="b596a-109">Syntax</span></span>


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="b596a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b596a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b596a-111">*szBackupServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b596a-111">*szBackupServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-112">以 null 終止的字串指標，其中包含要備份的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b596a-112">Pointer to a null-terminated string that contains the name of the server to backup.</span></span> <span data-ttu-id="b596a-113">前面的反斜線是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b596a-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="b596a-114">伺服器必須是呼叫此函式的同一部電腦。</span><span class="sxs-lookup"><span data-stu-id="b596a-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="b596a-115">伺服器名稱不能包含底線 (\_) 字元。</span><span class="sxs-lookup"><span data-stu-id="b596a-115">The server name cannot contain an underscore (\_) character.</span></span> <span data-ttu-id="b596a-116">伺服器名稱的範例是「server1」 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="b596a-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="b596a-117">*grbit* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b596a-117">*grbit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-118">判斷是否會備份記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b596a-118">Determines if the log files will be backed up.</span></span> <span data-ttu-id="b596a-119">此值應該一律為0，因為不支援增量備份。</span><span class="sxs-lookup"><span data-stu-id="b596a-119">This value should always be 0 because incremental backups are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-120">*btBackupType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b596a-120">*btBackupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-121">指定備份的類型。</span><span class="sxs-lookup"><span data-stu-id="b596a-121">Specifies the type of backup.</span></span> <span data-ttu-id="b596a-122">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b596a-122">This can be one of the following values.</span></span>

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span data-ttu-id="b596a-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**備份 \_ 類型已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="b596a-123"><span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP\_TYPE\_FULL**</span></span>


</dt> <dd>

<span data-ttu-id="b596a-124">指定完整備份。</span><span class="sxs-lookup"><span data-stu-id="b596a-124">Specifies a full backup.</span></span> <span data-ttu-id="b596a-125">備份) 的完整目錄 (DIT、記錄檔和更新檔案。</span><span class="sxs-lookup"><span data-stu-id="b596a-125">The complete directory (DIT, log files, and update files) are backed up.</span></span> <span data-ttu-id="b596a-126">備份所有資料，並截斷交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b596a-126">All data is backed up and transaction log files are truncated.</span></span> <span data-ttu-id="b596a-127">只支援完整備份。</span><span class="sxs-lookup"><span data-stu-id="b596a-127">Only full backups are supported.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span data-ttu-id="b596a-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_僅備份類型 \_ 記錄 \_**</span><span class="sxs-lookup"><span data-stu-id="b596a-128"><span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**BACKUP\_TYPE\_LOGS\_ONLY**</span></span>


</dt> <dd>

<span data-ttu-id="b596a-129">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="b596a-129">This value is not supported.</span></span> <span data-ttu-id="b596a-130">指定只備份資料庫記錄，而不是資料庫本身。</span><span class="sxs-lookup"><span data-stu-id="b596a-130">Specifies that only the database logs, and not the database itself, will be backed up.</span></span> <span data-ttu-id="b596a-131">這通常會在執行差異或增量備份時使用。</span><span class="sxs-lookup"><span data-stu-id="b596a-131">This is normally used when performing a differential or incremental backup.</span></span>

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span data-ttu-id="b596a-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**備份 \_ 類型 \_ 增量**</span><span class="sxs-lookup"><span data-stu-id="b596a-132"><span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP\_TYPE\_INCREMENTAL**</span></span>


</dt> <dd>

<span data-ttu-id="b596a-133">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="b596a-133">This value is not supported.</span></span> <span data-ttu-id="b596a-134">**DsBackupPrepare** 傳回 **錯誤 \_ 不正確 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="b596a-134">**DsBackupPrepare** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b596a-135">*ppvExpiryToken* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b596a-135">*ppvExpiryToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-136">**PVOID** 值的指標，此值會接收與此備份相關聯的到期權杖指標。</span><span class="sxs-lookup"><span data-stu-id="b596a-136">Pointer to a **PVOID** value that receives a pointer to an expiry token associated with this backup.</span></span> <span data-ttu-id="b596a-137">*pcbExpiryTokenSize* 會接收此資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b596a-137">*pcbExpiryTokenSize* receives the size, in bytes, of this data.</span></span> <span data-ttu-id="b596a-138">呼叫端必須儲存此權杖的內容與備份，因為在嘗試還原資料時，權杖必須傳遞至 [**DsRestorePrepare**](dsrestoreprepare.md) 。</span><span class="sxs-lookup"><span data-stu-id="b596a-138">The caller must save the contents of this token with the backup because the token must be passed to [**DsRestorePrepare**](dsrestoreprepare.md) when attempting to restore data.</span></span> <span data-ttu-id="b596a-139">儲存並不再需要權杖之後，呼叫端應該使用 [**DsBackupFree**](dsbackupfree.md)釋放配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b596a-139">After the token has been stored and is no longer required, the caller should free the allocated memory using [**DsBackupFree**](dsbackupfree.md).</span></span>

</dd> <dt>

<span data-ttu-id="b596a-140">*pcbExpiryTokenSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b596a-140">*pcbExpiryTokenSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-141">**DWORD** 值的指標，此值會接收 *ppvExpiryToken* 中權杖的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b596a-141">Pointer to a **DWORD** value that receives the size, in bytes, of the token in *ppvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-142">*phbc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b596a-142">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b596a-143">**HBC** 值的指標，此值會接收備份的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b596a-143">Pointer to an **HBC** value that receives the handle for the backup.</span></span> <span data-ttu-id="b596a-144">呼叫其他目錄服務備份功能（例如 [**DsBackupOpenFile**](dsbackupopenfile.md) 和 [**DsBackupEnd**](dsbackupend.md)）時，會使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="b596a-144">This handle is used when calling other Directory Service backup functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsBackupEnd**](dsbackupend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b596a-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="b596a-145">Return value</span></span>

<span data-ttu-id="b596a-146">如果函式成功，則傳回 **S \_ OK** ，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b596a-146">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="b596a-147">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="b596a-147">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="b596a-148">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="b596a-148">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-149">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="b596a-149">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="b596a-150">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="b596a-150">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-151">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="b596a-151">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-152">*szBackupServer* 或 *phbcBackupCoNtext* 無效。</span><span class="sxs-lookup"><span data-stu-id="b596a-152">*szBackupServer* or *phbcBackupContext* are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-153">**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="b596a-153">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-154">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="b596a-154">A memory allocation failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-155">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="b596a-155">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-156">找不到 *szBackupServer* 中的伺服器、不是網域控制站，或 *szBackupServer* 的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="b596a-156">The server in *szBackupServer* could not be found, is not a domain controller or *szBackupServer* is not formatted correctly.</span></span> <span data-ttu-id="b596a-157">此值定義于 ntdsbmsg 中。</span><span class="sxs-lookup"><span data-stu-id="b596a-157">This value is defined in ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-158">**hrInvalidParam**</span><span class="sxs-lookup"><span data-stu-id="b596a-158">**hrInvalidParam**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-159">*ppvExpiryToken* 和/或 *pcbExpiryTokenSize* 無效。</span><span class="sxs-lookup"><span data-stu-id="b596a-159">*ppvExpiryToken* and/or *pcbExpiryTokenSize* are invalid.</span></span> <span data-ttu-id="b596a-160">此值定義于 Ntdsbmsg 中。</span><span class="sxs-lookup"><span data-stu-id="b596a-160">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="b596a-161">**RPC \_ S \_ 不正確系結 \_**</span><span class="sxs-lookup"><span data-stu-id="b596a-161">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="b596a-162">此函數會從遠端呼叫，或 *szServerName* 中的伺服器不是網域控制站。</span><span class="sxs-lookup"><span data-stu-id="b596a-162">The function is called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b596a-163">備註</span><span class="sxs-lookup"><span data-stu-id="b596a-163">Remarks</span></span>

<span data-ttu-id="b596a-164">此函式需要呼叫端具有 **SE \_ 備份 \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="b596a-164">This function requires that the caller has the **SE\_BACKUP\_NAME** privilege.</span></span> <span data-ttu-id="b596a-165">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來變更用來呼叫此函數的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="b596a-165">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to change the security context under which this function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="b596a-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="b596a-166">Requirements</span></span>



| <span data-ttu-id="b596a-167">需求</span><span class="sxs-lookup"><span data-stu-id="b596a-167">Requirement</span></span> | <span data-ttu-id="b596a-168">值</span><span class="sxs-lookup"><span data-stu-id="b596a-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b596a-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b596a-169">Minimum supported client</span></span><br/> | <span data-ttu-id="b596a-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b596a-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b596a-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b596a-171">Minimum supported server</span></span><br/> | <span data-ttu-id="b596a-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b596a-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b596a-173">標頭</span><span class="sxs-lookup"><span data-stu-id="b596a-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="b596a-174"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="b596a-174"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="b596a-175">程式庫</span><span class="sxs-lookup"><span data-stu-id="b596a-175">Library</span></span><br/>                  | <dl> <span data-ttu-id="b596a-176"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b596a-176"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="b596a-177">DLL</span><span class="sxs-lookup"><span data-stu-id="b596a-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b596a-178"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b596a-178"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="b596a-179">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b596a-179">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b596a-180">**DsBackupPrepareW** (Unicode) 和 **DsBackupPrepareA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b596a-180">**DsBackupPrepareW** (Unicode) and **DsBackupPrepareA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b596a-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b596a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b596a-182">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="b596a-182">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="b596a-183">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="b596a-183">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="b596a-184">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="b596a-184">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="b596a-185">**DsBackupEnd**</span><span class="sxs-lookup"><span data-stu-id="b596a-185">**DsBackupEnd**</span></span>](dsbackupend.md)
</dt> <dt>

[<span data-ttu-id="b596a-186">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="b596a-186">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="b596a-187">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="b596a-187">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="b596a-188">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="b596a-188">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

