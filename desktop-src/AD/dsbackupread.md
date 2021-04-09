---
title: 'DsBackupRead 函式 (Ntdsbcli) '
description: 從目前開啟的檔案將資料區塊讀入緩衝區。
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- DsBackupRead 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934281"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="f4be9-104">DsBackupRead 函式</span><span class="sxs-lookup"><span data-stu-id="f4be9-104">DsBackupRead function</span></span>

<span data-ttu-id="f4be9-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f4be9-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4be9-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f4be9-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f4be9-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f4be9-108">**DsBackupRead** 函式會從目前開啟的檔案，將資料區塊讀入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f4be9-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="f4be9-109">用戶端應用程式預期會重複呼叫這個函式，直到收到整個備份檔案為止。</span><span class="sxs-lookup"><span data-stu-id="f4be9-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="f4be9-110">[**DsBackupOpenFile**](dsbackupopenfile.md)函式會提供備份檔案的整個大小。</span><span class="sxs-lookup"><span data-stu-id="f4be9-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4be9-111">語法</span><span class="sxs-lookup"><span data-stu-id="f4be9-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="f4be9-112">參數</span><span class="sxs-lookup"><span data-stu-id="f4be9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4be9-113">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-114">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="f4be9-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f4be9-115">*pvBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-116">接收資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f4be9-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="f4be9-117">此緩衝區的大小必須至少為 *cbBuffer* 個位元組。</span><span class="sxs-lookup"><span data-stu-id="f4be9-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="f4be9-118">*cbBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-119">包含 *pvBuffer* 的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f4be9-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="f4be9-120">此值必須是8192的倍數，且必須大於或等於24576。</span><span class="sxs-lookup"><span data-stu-id="f4be9-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="f4be9-121">*pcbRead* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f4be9-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-122">**DWORD** 值的指標，此值會接收實際讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f4be9-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="f4be9-123">這可能小於所要求的位元組數目，因為某些傳輸會將傳輸的緩衝區片段化，而不是以資料填滿整個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f4be9-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4be9-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4be9-124">Return value</span></span>

<span data-ttu-id="f4be9-125">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f4be9-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="f4be9-126">可能的錯誤代碼包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f4be9-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="f4be9-127">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="f4be9-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-128">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="f4be9-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f4be9-129">**錯誤 \_ 處理 \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="f4be9-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="f4be9-130">已達到備份檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="f4be9-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4be9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4be9-131">Requirements</span></span>



| <span data-ttu-id="f4be9-132">需求</span><span class="sxs-lookup"><span data-stu-id="f4be9-132">Requirement</span></span> | <span data-ttu-id="f4be9-133">值</span><span class="sxs-lookup"><span data-stu-id="f4be9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4be9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4be9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f4be9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4be9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4be9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4be9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f4be9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4be9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4be9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f4be9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4be9-139"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4be9-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4be9-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="f4be9-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4be9-141"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4be9-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f4be9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f4be9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4be9-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4be9-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4be9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4be9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4be9-145">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="f4be9-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="f4be9-146">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="f4be9-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="f4be9-147">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="f4be9-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="f4be9-148">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="f4be9-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="f4be9-149">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="f4be9-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

