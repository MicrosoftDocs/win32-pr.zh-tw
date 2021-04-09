---
title: 'DsRestoreRegister 函式 (Ntdsbcli) '
description: 註冊還原作業。
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- DsRestoreRegister 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025215"
---
# <a name="dsrestoreregister-function"></a><span data-ttu-id="794fe-104">DsRestoreRegister 函式</span><span class="sxs-lookup"><span data-stu-id="794fe-104">DsRestoreRegister function</span></span>

<span data-ttu-id="794fe-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="794fe-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="794fe-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="794fe-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="794fe-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="794fe-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="794fe-108">**DsRestoreRegister** 函數會註冊還原作業。此函式會 interlocks 所有後續的還原作業，並防止還原目標啟動，直到呼叫 [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)函數為止。</span><span class="sxs-lookup"><span data-stu-id="794fe-108">The **DsRestoreRegister** function registers a restore operation.This function interlocks all subsequent restore operations and prevents the restore target from starting until the [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="794fe-109">語法</span><span class="sxs-lookup"><span data-stu-id="794fe-109">Syntax</span></span>


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a><span data-ttu-id="794fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="794fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794fe-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-112">包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="794fe-112">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-113">*szCheckPointFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-113">*szCheckPointFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-114">以 null 結束的字串指標，其中包含檢查點檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="794fe-114">Pointer to a null-terminated string that contains the path to the checkpoint file.</span></span> <span data-ttu-id="794fe-115">此路徑是由 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函式所提供，且具有 **BFT \_ 檢查點 \_ 目錄** 的 **BFT** 值。</span><span class="sxs-lookup"><span data-stu-id="794fe-115">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_CHECKPOINT\_DIR**.</span></span> <span data-ttu-id="794fe-116">這通常與系統資料庫路徑相同。</span><span class="sxs-lookup"><span data-stu-id="794fe-116">Typically this is the same as the system database path.</span></span> <span data-ttu-id="794fe-117">這是正確的備份還原功能所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="794fe-117">This path is required for proper backup restore function.</span></span> <span data-ttu-id="794fe-118">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="794fe-118">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="794fe-119">在此參數中傳遞 **Null** 會在還原過程中造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="794fe-119">Passing **NULL** in this parameter will cause an error during the restore process.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-120">*szLogPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-120">*szLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-121">以 null 結束的字串指標，其中包含將還原記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="794fe-121">Pointer to a null-terminated string that contains the path where the log files will be restored.</span></span> <span data-ttu-id="794fe-122">此路徑是由 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)函式所提供，且具有 **BFT 記錄檔 \_ \_ 目錄** 的 **BFT** 值。</span><span class="sxs-lookup"><span data-stu-id="794fe-122">This path is provided by the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function and has a **BFT** value of **BFT\_LOG\_DIR**.</span></span> <span data-ttu-id="794fe-123">如果路徑指向空白目錄，就會在該處建立新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="794fe-123">If the path points to an empty directory, new log files are created there.</span></span> <span data-ttu-id="794fe-124">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="794fe-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-125">*rgrstmap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-125">*rgrstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-126">[**EDB \_ RSTMAP**](edb-rstmap.md)結構的陣列，其中包含每個資料庫的舊路徑和新路徑。</span><span class="sxs-lookup"><span data-stu-id="794fe-126">An array of [**EDB\_RSTMAP**](edb-rstmap.md) structures that contains the old and new paths for each database.</span></span> <span data-ttu-id="794fe-127">每個資料庫都有一個結構。</span><span class="sxs-lookup"><span data-stu-id="794fe-127">There is one structure for each database.</span></span> <span data-ttu-id="794fe-128">針對目錄，有一個適用于系統資料庫的結構，還有另一個適用于目錄資料庫的結構。</span><span class="sxs-lookup"><span data-stu-id="794fe-128">For the directory, there is a structure for the system database and another structure for the directory database.</span></span> <span data-ttu-id="794fe-129">陣列中的元素順序並不重要。</span><span class="sxs-lookup"><span data-stu-id="794fe-129">The order of the elements in the array does not matter.</span></span> <span data-ttu-id="794fe-130">*Crstmap* 參數包含陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="794fe-130">The *crstmap* parameter contains the number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-131">*crstmap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-131">*crstmap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-132">包含 *rgrstmap* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="794fe-132">Contains the number of elements in the *rgrstmap* array.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-133">*szBackupLogPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-133">*szBackupLogPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-134">以 null 結束的字串指標，其中包含備份記錄檔目前所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="794fe-134">Pointer to a null-terminated string that contains the path where the backed up log files currently reside.</span></span> <span data-ttu-id="794fe-135">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="794fe-135">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-136">*genLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-136">*genLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-137">包含此還原會話中要還原的最低記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="794fe-137">Contains the lowest log number to restore in this restore session.</span></span> <span data-ttu-id="794fe-138">這是從0x00000 到0xFFFFF 的範圍內的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="794fe-138">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-139">*genHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="794fe-139">*genHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794fe-140">包含此還原會話中要還原的最高記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="794fe-140">Contains the highest log number to restore in this restore session.</span></span> <span data-ttu-id="794fe-141">這是從0x00000 到0xFFFFF 的範圍內的十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="794fe-141">This is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794fe-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="794fe-142">Return value</span></span>

<span data-ttu-id="794fe-143">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="794fe-143">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="794fe-144">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="794fe-144">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="794fe-145">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="794fe-145">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="794fe-146">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="794fe-146">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="794fe-147">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="794fe-147">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-148">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="794fe-148">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="794fe-149">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="794fe-149">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="794fe-150">**hrMissingExpiryToken**</span><span class="sxs-lookup"><span data-stu-id="794fe-150">**hrMissingExpiryToken**</span></span>
</dt> <dd>

<span data-ttu-id="794fe-151">提供給 [**DsRestorePrepare**](dsrestoreprepare.md) 的到期權杖無效。</span><span class="sxs-lookup"><span data-stu-id="794fe-151">The expiry token supplied to [**DsRestorePrepare**](dsrestoreprepare.md) was invalid.</span></span> <span data-ttu-id="794fe-152">此值定義于 Ntdsbmsg 中。</span><span class="sxs-lookup"><span data-stu-id="794fe-152">This value is defined in Ntdsbmsg.h.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="794fe-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="794fe-153">Requirements</span></span>



| <span data-ttu-id="794fe-154">需求</span><span class="sxs-lookup"><span data-stu-id="794fe-154">Requirement</span></span> | <span data-ttu-id="794fe-155">值</span><span class="sxs-lookup"><span data-stu-id="794fe-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="794fe-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="794fe-156">Minimum supported client</span></span><br/> | <span data-ttu-id="794fe-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="794fe-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="794fe-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="794fe-158">Minimum supported server</span></span><br/> | <span data-ttu-id="794fe-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="794fe-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="794fe-160">標頭</span><span class="sxs-lookup"><span data-stu-id="794fe-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="794fe-161"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="794fe-161"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="794fe-162">程式庫</span><span class="sxs-lookup"><span data-stu-id="794fe-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="794fe-163"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="794fe-163"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="794fe-164">DLL</span><span class="sxs-lookup"><span data-stu-id="794fe-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="794fe-165"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="794fe-165"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="794fe-166">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="794fe-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="794fe-167">**DsRestoreRegisterW** (Unicode) 和 **DsRestoreRegisterA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="794fe-167">**DsRestoreRegisterW** (Unicode) and **DsRestoreRegisterA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="794fe-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="794fe-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794fe-169">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="794fe-169">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="794fe-170">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="794fe-170">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="794fe-171">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="794fe-171">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="794fe-172">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="794fe-172">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> <dt>

[<span data-ttu-id="794fe-173">**EDB \_ RSTMAP**</span><span class="sxs-lookup"><span data-stu-id="794fe-173">**EDB\_RSTMAP**</span></span>](edb-rstmap.md)
</dt> <dt>

[<span data-ttu-id="794fe-174">還原 Active Directory</span><span class="sxs-lookup"><span data-stu-id="794fe-174">Restoring Active Directory</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="794fe-175">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="794fe-175">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

