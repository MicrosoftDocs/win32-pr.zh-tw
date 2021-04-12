---
title: 'DsBackupOpenFile 函式 (Ntdsbcli) '
description: 開啟指定的檔案，並執行準備檔案以進行備份所需的用戶端和伺服器作業。
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- DsBackupOpenFile 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104057"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="95004-104">DsBackupOpenFile 函式</span><span class="sxs-lookup"><span data-stu-id="95004-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="95004-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="95004-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="95004-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="95004-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="95004-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="95004-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="95004-108">**DsBackupOpenFile** 函式會開啟指定的檔案，並執行準備檔案以進行備份所需的用戶端和伺服器作業。</span><span class="sxs-lookup"><span data-stu-id="95004-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="95004-109">語法</span><span class="sxs-lookup"><span data-stu-id="95004-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="95004-110">參數</span><span class="sxs-lookup"><span data-stu-id="95004-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95004-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95004-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95004-112">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="95004-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="95004-113">*szAttachmentName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95004-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95004-114">指標，指向以 null 終止的字串，指定要開啟之備份檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="95004-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="95004-115">*cbReadHintSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95004-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95004-116">包含在 [**DsBackupRead**](dsbackupread.md)函數中傳遞為 *pvBuffer* 引數的緩衝區可能大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95004-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="95004-117">備份函式會使用此值作為將網路流量優化的提示。</span><span class="sxs-lookup"><span data-stu-id="95004-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="95004-118">此值必須是8192的倍數，且必須大於或等於24576。</span><span class="sxs-lookup"><span data-stu-id="95004-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="95004-119">*pliFileSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="95004-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95004-120">以位元組為單位的 **大型 \_ 整數** 值的指標，此值會接收備份檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95004-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95004-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="95004-121">Return value</span></span>

<span data-ttu-id="95004-122">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95004-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="95004-123">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="95004-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="95004-124">**\_拒絕存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="95004-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="95004-125">呼叫端沒有適當的存取權限可呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="95004-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="95004-126">[**DsSetAuthIdentity**](dssetauthidentity.md)函式可用來設定用於備份和還原功能的認證。</span><span class="sxs-lookup"><span data-stu-id="95004-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="95004-127">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="95004-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="95004-128">*hbc*、 *szAttachmentName* 或 *pliFileSize* 無效。</span><span class="sxs-lookup"><span data-stu-id="95004-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95004-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="95004-129">Requirements</span></span>



| <span data-ttu-id="95004-130">需求</span><span class="sxs-lookup"><span data-stu-id="95004-130">Requirement</span></span> | <span data-ttu-id="95004-131">值</span><span class="sxs-lookup"><span data-stu-id="95004-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95004-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95004-132">Minimum supported client</span></span><br/> | <span data-ttu-id="95004-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95004-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95004-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95004-134">Minimum supported server</span></span><br/> | <span data-ttu-id="95004-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95004-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95004-136">標頭</span><span class="sxs-lookup"><span data-stu-id="95004-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="95004-137"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="95004-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="95004-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="95004-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="95004-139"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="95004-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="95004-140">DLL</span><span class="sxs-lookup"><span data-stu-id="95004-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95004-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95004-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="95004-142">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="95004-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="95004-143">**DsBackupOpenFileW** (Unicode) 和 **DsBackupOpenFileA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="95004-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="95004-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95004-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95004-145">**DsBackupRead**</span><span class="sxs-lookup"><span data-stu-id="95004-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="95004-146">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="95004-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="95004-147">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="95004-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

