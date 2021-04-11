---
title: 'DsRestorePrepare 函式 (Ntdsbcli) '
description: 連接到指定的目錄伺服器，並將它準備好進行還原作業。
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- DsRestorePrepare 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094448"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="067c1-104">DsRestorePrepare 函式</span><span class="sxs-lookup"><span data-stu-id="067c1-104">DsRestorePrepare function</span></span>

<span data-ttu-id="067c1-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="067c1-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="067c1-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="067c1-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="067c1-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="067c1-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="067c1-108">**DsRestorePrepare** 函式會連接到指定的目錄伺服器，並將它準備好進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="067c1-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="067c1-109">語法</span><span class="sxs-lookup"><span data-stu-id="067c1-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="067c1-110">參數</span><span class="sxs-lookup"><span data-stu-id="067c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067c1-111">*szServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="067c1-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067c1-112">以 null 終止的字串指標，其中包含要還原的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="067c1-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="067c1-113">前面的反斜線是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="067c1-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="067c1-114">伺服器必須是呼叫此函式的同一部電腦。</span><span class="sxs-lookup"><span data-stu-id="067c1-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="067c1-115">伺服器名稱不能包含任何底線 (\_) 字元。</span><span class="sxs-lookup"><span data-stu-id="067c1-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="067c1-116">伺服器名稱的範例是「server1」 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="067c1-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="067c1-117">*rtFlag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="067c1-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067c1-118">指定要執行的還原類型。</span><span class="sxs-lookup"><span data-stu-id="067c1-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="067c1-119">這可以是零或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="067c1-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="067c1-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**還原 \_ 類型 \_ 追捕**</span><span class="sxs-lookup"><span data-stu-id="067c1-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="067c1-121">預設值。</span><span class="sxs-lookup"><span data-stu-id="067c1-121">Default.</span></span> <span data-ttu-id="067c1-122">還原的版本會透過標準對帳邏輯進行協調，讓還原的 DIT 可以與其他企業伺服器電腦進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="067c1-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="067c1-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**還原 \_ 類型 \_ AUTHORATATIVE**</span><span class="sxs-lookup"><span data-stu-id="067c1-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="067c1-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="067c1-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="067c1-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**\_線上還原類型 \_**</span><span class="sxs-lookup"><span data-stu-id="067c1-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="067c1-126">不支援。</span><span class="sxs-lookup"><span data-stu-id="067c1-126">Not Supported.</span></span> <span data-ttu-id="067c1-127">當 NTDS 處於線上狀態時，就會執行還原。</span><span class="sxs-lookup"><span data-stu-id="067c1-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="067c1-128">*pvExpiryToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="067c1-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067c1-129">與要還原之備份相關聯的到期權杖指標。</span><span class="sxs-lookup"><span data-stu-id="067c1-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="067c1-130">當備份目錄時，會從 [**DsBackupPrepare**](dsbackupprepare.md) 函式取得此權杖。</span><span class="sxs-lookup"><span data-stu-id="067c1-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="067c1-131">如果此參數為 **Null**，則 *phbc* 中傳回的控制碼只能用來取得具有 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) 函數的還原目錄。</span><span class="sxs-lookup"><span data-stu-id="067c1-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="067c1-132">控制碼無法用於任何其他還原函數。</span><span class="sxs-lookup"><span data-stu-id="067c1-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="067c1-133">*cbExpiryTokenSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="067c1-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067c1-134">包含 *pvExpiryToken* 中到期權杖的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="067c1-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="067c1-135">*phbc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="067c1-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="067c1-136">**HBC** 值的指標，此值會接收還原的控制碼。</span><span class="sxs-lookup"><span data-stu-id="067c1-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="067c1-137">呼叫其他目錄服務還原功能（例如 [**DsBackupOpenFile**](dsbackupopenfile.md) 和 [**DsRestoreEnd**](dsrestoreend.md)）時，會使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="067c1-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067c1-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="067c1-138">Return value</span></span>

<span data-ttu-id="067c1-139">如果成功，則傳回標準 **HRESULT** 代碼;否則，會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="067c1-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="067c1-140">備註</span><span class="sxs-lookup"><span data-stu-id="067c1-140">Remarks</span></span>

<span data-ttu-id="067c1-141">**DsRestorePrepare** 函式要求呼叫端必須是伺服器上 Administrators 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="067c1-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="067c1-142">**DsRestorePrepare** 可搭配或未提供權杖使用。</span><span class="sxs-lookup"><span data-stu-id="067c1-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="067c1-143">如果已提供權杖，則會檢查其是否到期，並允許在傳回的內容上執行所有作業。</span><span class="sxs-lookup"><span data-stu-id="067c1-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="067c1-144">如果未提供權杖，則會限制傳回的內容，而且只能用於 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="067c1-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="067c1-145">它可能不會用於 [**DsRestoreRegister**](dsrestoreregister.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="067c1-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="067c1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="067c1-146">Requirements</span></span>



| <span data-ttu-id="067c1-147">需求</span><span class="sxs-lookup"><span data-stu-id="067c1-147">Requirement</span></span> | <span data-ttu-id="067c1-148">值</span><span class="sxs-lookup"><span data-stu-id="067c1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="067c1-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="067c1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="067c1-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="067c1-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="067c1-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="067c1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="067c1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="067c1-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="067c1-153">標頭</span><span class="sxs-lookup"><span data-stu-id="067c1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="067c1-154"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="067c1-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="067c1-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="067c1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="067c1-156"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="067c1-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="067c1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="067c1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="067c1-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="067c1-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="067c1-159">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="067c1-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="067c1-160">**DsRestorePrepareW** (Unicode) 和 **DsRestorePrepareA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="067c1-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="067c1-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="067c1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067c1-162">還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="067c1-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="067c1-163">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="067c1-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="067c1-164">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="067c1-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="067c1-165">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="067c1-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="067c1-166">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="067c1-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="067c1-167">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="067c1-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 

