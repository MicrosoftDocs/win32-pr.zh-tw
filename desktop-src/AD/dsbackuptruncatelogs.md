---
title: 'DsBackupTruncateLogs 函式 (Ntdsbcli) '
description: 截斷先前讀取的備份記錄。
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- DsBackupTruncateLogs 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508500"
---
# <a name="dsbackuptruncatelogs-function"></a><span data-ttu-id="65f91-104">DsBackupTruncateLogs 函式</span><span class="sxs-lookup"><span data-stu-id="65f91-104">DsBackupTruncateLogs function</span></span>

<span data-ttu-id="65f91-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="65f91-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65f91-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="65f91-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="65f91-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="65f91-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="65f91-108">**DsBackupTruncateLogs** 函式會截斷先前讀取的備份記錄。</span><span class="sxs-lookup"><span data-stu-id="65f91-108">The **DsBackupTruncateLogs** function truncates the previously read backup logs.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f91-109">語法</span><span class="sxs-lookup"><span data-stu-id="65f91-109">Syntax</span></span>


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="65f91-110">參數</span><span class="sxs-lookup"><span data-stu-id="65f91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f91-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65f91-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f91-112">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="65f91-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f91-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="65f91-113">Return value</span></span>

<span data-ttu-id="65f91-114">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65f91-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="65f91-115">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="65f91-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="65f91-116">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="65f91-116">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="65f91-117">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="65f91-117">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="65f91-118">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="65f91-118">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="65f91-119">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="65f91-119">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="65f91-120">*hbc* 無效。</span><span class="sxs-lookup"><span data-stu-id="65f91-120">*hbc* is invalid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65f91-121">備註</span><span class="sxs-lookup"><span data-stu-id="65f91-121">Remarks</span></span>

<span data-ttu-id="65f91-122">當完整或增量備份順利完成時，請使用 **DsBackupTruncateLogs** 函數。</span><span class="sxs-lookup"><span data-stu-id="65f91-122">Use the **DsBackupTruncateLogs** function when a full or incremental backup has completed successfully.</span></span>

> [!Caution]  
> <span data-ttu-id="65f91-123">如果在差異備份之後呼叫這個函式，將會遺失所有增量備份資訊。</span><span class="sxs-lookup"><span data-stu-id="65f91-123">If this function is called after a differential backup, all of the incremental backup information will be lost.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65f91-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="65f91-124">Requirements</span></span>



| <span data-ttu-id="65f91-125">需求</span><span class="sxs-lookup"><span data-stu-id="65f91-125">Requirement</span></span> | <span data-ttu-id="65f91-126">值</span><span class="sxs-lookup"><span data-stu-id="65f91-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65f91-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65f91-127">Minimum supported client</span></span><br/> | <span data-ttu-id="65f91-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65f91-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65f91-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65f91-129">Minimum supported server</span></span><br/> | <span data-ttu-id="65f91-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f91-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65f91-131">標頭</span><span class="sxs-lookup"><span data-stu-id="65f91-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="65f91-132"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="65f91-132"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="65f91-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="65f91-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="65f91-134"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="65f91-134"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="65f91-135">DLL</span><span class="sxs-lookup"><span data-stu-id="65f91-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f91-136"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f91-136"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f91-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65f91-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f91-138">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="65f91-138">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="65f91-139">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="65f91-139">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="65f91-140">**DsSetCurrentBackupLog**</span><span class="sxs-lookup"><span data-stu-id="65f91-140">**DsSetCurrentBackupLog**</span></span>](dssetcurrentbackuplog.md)
</dt> <dt>

[<span data-ttu-id="65f91-141">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="65f91-141">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="65f91-142">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="65f91-142">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

