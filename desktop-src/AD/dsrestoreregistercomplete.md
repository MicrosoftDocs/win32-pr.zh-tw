---
title: 'DsRestoreRegisterComplete 函式 (Ntdsbcli) '
description: 在還原作業完成之後呼叫以解除鎖定 Active Directory 伺服器。
ms.assetid: 781cd2ec-d2e2-4f3a-903d-feda4b871de5
ms.tgt_platform: multiple
keywords:
- DsRestoreRegisterComplete 函式 Active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegisterComplete
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5e5e01b29281860dff59fbcd08a3b48ec66c4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025214"
---
# <a name="dsrestoreregistercomplete-function"></a><span data-ttu-id="09b59-104">DsRestoreRegisterComplete 函式</span><span class="sxs-lookup"><span data-stu-id="09b59-104">DsRestoreRegisterComplete function</span></span>

<span data-ttu-id="09b59-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="09b59-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09b59-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="09b59-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="09b59-107">改為使用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="09b59-107">Use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="09b59-108">在還原作業完成之後，會呼叫 **DsRestoreRegisterComplete** 函數來解除鎖定 Active Directory 伺服器。</span><span class="sxs-lookup"><span data-stu-id="09b59-108">The **DsRestoreRegisterComplete** function is called to unlock an Active Directory server after a restore operation is complete.</span></span> <span data-ttu-id="09b59-109">此函數是 [**DsRestoreRegister**](dsrestoreregister.md) 函式的對應函式。</span><span class="sxs-lookup"><span data-stu-id="09b59-109">This function is counterpart to the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b59-110">語法</span><span class="sxs-lookup"><span data-stu-id="09b59-110">Syntax</span></span>


```C++
HRESULT DsRestoreRegisterComplete(
  _In_ HBC     hbc,
  _In_ HRESULT hrRestoreState
);
```



## <a name="parameters"></a><span data-ttu-id="09b59-111">參數</span><span class="sxs-lookup"><span data-stu-id="09b59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09b59-112">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09b59-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09b59-113">包含使用 [**DsRestorePrepare**](dsrestoreprepare.md) 函數取得的還原內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="09b59-113">Contains the restoration context handle obtained with the [**DsRestorePrepare**](dsrestoreprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="09b59-114">*hrRestoreState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09b59-114">*hrRestoreState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09b59-115">包含還原作業的最終狀態。</span><span class="sxs-lookup"><span data-stu-id="09b59-115">Contains the final status of the restore operation.</span></span> <span data-ttu-id="09b59-116">如果還原作業成功，此參數應包含 **S \_ OK** ，否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="09b59-116">This parameter should contain **S\_OK** if the restore operation was successful or an error code otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09b59-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="09b59-117">Return value</span></span>

<span data-ttu-id="09b59-118">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="09b59-118">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="09b59-119">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="09b59-119">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="09b59-120">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="09b59-120">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="09b59-121">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="09b59-121">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="09b59-122">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="09b59-122">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09b59-123">備註</span><span class="sxs-lookup"><span data-stu-id="09b59-123">Remarks</span></span>

<span data-ttu-id="09b59-124">重新開機網域控制站之前，請呼叫此函式以提供還原作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="09b59-124">Before you restart the domain controller, call this function to provide the status of the restore operation.</span></span> <span data-ttu-id="09b59-125">如果狀態不成功，目錄服務將不會啟動，直到還原有效的資料庫為止。</span><span class="sxs-lookup"><span data-stu-id="09b59-125">If the status is not successful, the directory service will not start until a valid database has been restored.</span></span> <span data-ttu-id="09b59-126">此函數會完成還原作業，並允許 Active Directory Domain Services 啟動。</span><span class="sxs-lookup"><span data-stu-id="09b59-126">This function completes the restore operation and allows Active Directory Domain Services to start.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b59-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="09b59-127">Requirements</span></span>



| <span data-ttu-id="09b59-128">需求</span><span class="sxs-lookup"><span data-stu-id="09b59-128">Requirement</span></span> | <span data-ttu-id="09b59-129">值</span><span class="sxs-lookup"><span data-stu-id="09b59-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09b59-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09b59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="09b59-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="09b59-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="09b59-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09b59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="09b59-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="09b59-133">None supported</span></span><br/>                                                               |
| <span data-ttu-id="09b59-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="09b59-134">End of client support</span></span><br/>    | <span data-ttu-id="09b59-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="09b59-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="09b59-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="09b59-136">End of server support</span></span><br/>    | <span data-ttu-id="09b59-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="09b59-137">None supported</span></span><br/>                                                               |
| <span data-ttu-id="09b59-138">標頭</span><span class="sxs-lookup"><span data-stu-id="09b59-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="09b59-139"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="09b59-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="09b59-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="09b59-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="09b59-141"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="09b59-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="09b59-142">DLL</span><span class="sxs-lookup"><span data-stu-id="09b59-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09b59-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09b59-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b59-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09b59-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b59-145">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="09b59-145">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="09b59-146">**DsRestorePrepare**</span><span class="sxs-lookup"><span data-stu-id="09b59-146">**DsRestorePrepare**</span></span>](dsrestoreprepare.md)
</dt> <dt>

[<span data-ttu-id="09b59-147">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="09b59-147">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="09b59-148">還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="09b59-148">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="09b59-149">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="09b59-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

