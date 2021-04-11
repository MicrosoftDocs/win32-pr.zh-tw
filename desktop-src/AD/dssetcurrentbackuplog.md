---
title: 'DsSetCurrentBackupLog 函式 (Ntdsbcli) '
description: 設定成功還原後的目前備份記錄檔編號。
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- DsSetCurrentBackupLog 函式 Active Directory
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843828"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="41b4f-104">DsSetCurrentBackupLog 函式</span><span class="sxs-lookup"><span data-stu-id="41b4f-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="41b4f-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="41b4f-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="41b4f-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="41b4f-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="41b4f-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="41b4f-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="41b4f-108">**DsSetCurrentBackupLog** 函式會在成功還原之後設定目前的備份記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="41b4f-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="41b4f-109">由於 Active Directory Domain Services 僅支援迴圈記錄，因此通常不會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="41b4f-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b4f-110">語法</span><span class="sxs-lookup"><span data-stu-id="41b4f-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="41b4f-111">參數</span><span class="sxs-lookup"><span data-stu-id="41b4f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b4f-112">*szServerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41b4f-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41b4f-113">以 null 結束的字串指標，其中包含要設定備份記錄檔編號的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="41b4f-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="41b4f-114">前面的反斜線是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="41b4f-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="41b4f-115">伺服器必須是呼叫此函式的同一部電腦。</span><span class="sxs-lookup"><span data-stu-id="41b4f-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="41b4f-116">伺服器名稱不能包含任何底線 (\_) 字元。</span><span class="sxs-lookup"><span data-stu-id="41b4f-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="41b4f-117">伺服器名稱的範例是「server1」 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="41b4f-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="41b4f-118">*dwCurrentLog* \[在\]</span><span class="sxs-lookup"><span data-stu-id="41b4f-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41b4f-119">包含要設定的備份記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="41b4f-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b4f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="41b4f-120">Return value</span></span>

<span data-ttu-id="41b4f-121">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="41b4f-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="41b4f-122">下列清單列出可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="41b4f-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="41b4f-123">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="41b4f-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="41b4f-124">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="41b4f-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="41b4f-125">**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="41b4f-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="41b4f-126">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="41b4f-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41b4f-127">備註</span><span class="sxs-lookup"><span data-stu-id="41b4f-127">Remarks</span></span>

<span data-ttu-id="41b4f-128">通常不需要呼叫 **DsSetCurrentBackupLog** 函數。</span><span class="sxs-lookup"><span data-stu-id="41b4f-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="41b4f-129">備份功能會自動判斷並設定最後備份的記錄檔編號。</span><span class="sxs-lookup"><span data-stu-id="41b4f-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="41b4f-130">您可以使用 **DsSetCurrentBackupLog** 來防止另一個增量備份在執行完整備份之前進行。</span><span class="sxs-lookup"><span data-stu-id="41b4f-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b4f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b4f-131">Requirements</span></span>



| <span data-ttu-id="41b4f-132">需求</span><span class="sxs-lookup"><span data-stu-id="41b4f-132">Requirement</span></span> | <span data-ttu-id="41b4f-133">值</span><span class="sxs-lookup"><span data-stu-id="41b4f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41b4f-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41b4f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="41b4f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41b4f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41b4f-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41b4f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="41b4f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41b4f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41b4f-138">標頭</span><span class="sxs-lookup"><span data-stu-id="41b4f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b4f-139"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="41b4f-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="41b4f-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="41b4f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="41b4f-141"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="41b4f-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="41b4f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="41b4f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b4f-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b4f-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="41b4f-144">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="41b4f-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41b4f-145">**DsSetCurrentBackupLogW** (Unicode) 和 **DsSetCurrentBackupLogA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="41b4f-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="41b4f-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41b4f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b4f-147">備份與還原 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="41b4f-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="41b4f-148">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="41b4f-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

