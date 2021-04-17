---
title: 'DsBackupClose 函式 (Ntdsbcli) '
description: 關閉以 DsBackupOpenFile 函數開啟的備份檔案。
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- DsBackupClose 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465069"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="be91b-104">DsBackupClose 函式</span><span class="sxs-lookup"><span data-stu-id="be91b-104">DsBackupClose function</span></span>

<span data-ttu-id="be91b-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="be91b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="be91b-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="be91b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="be91b-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="be91b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="be91b-108">**DsBackupClose** 函式會關閉以 [**DsBackupOpenFile**](dsbackupopenfile.md)函數開啟的備份檔案。</span><span class="sxs-lookup"><span data-stu-id="be91b-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="be91b-109">針對每個備份控制碼，一次只能開啟一個檔案，所以此函式會關閉目前開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="be91b-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="be91b-110">語法</span><span class="sxs-lookup"><span data-stu-id="be91b-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="be91b-111">參數</span><span class="sxs-lookup"><span data-stu-id="be91b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be91b-112">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be91b-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be91b-113">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="be91b-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be91b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="be91b-114">Return value</span></span>

<span data-ttu-id="be91b-115">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="be91b-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="be91b-116">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="be91b-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="be91b-117">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="be91b-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="be91b-118">*hbc* 無效。</span><span class="sxs-lookup"><span data-stu-id="be91b-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="be91b-119">**hrInvalidHandle**</span><span class="sxs-lookup"><span data-stu-id="be91b-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="be91b-120">目前未開啟任何檔案。</span><span class="sxs-lookup"><span data-stu-id="be91b-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be91b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="be91b-121">Requirements</span></span>



| <span data-ttu-id="be91b-122">需求</span><span class="sxs-lookup"><span data-stu-id="be91b-122">Requirement</span></span> | <span data-ttu-id="be91b-123">值</span><span class="sxs-lookup"><span data-stu-id="be91b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be91b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be91b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be91b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be91b-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be91b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be91b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be91b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be91b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be91b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="be91b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be91b-129"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="be91b-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="be91b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="be91b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="be91b-131"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be91b-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="be91b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="be91b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be91b-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be91b-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be91b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be91b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be91b-135">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="be91b-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="be91b-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="be91b-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="be91b-137">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="be91b-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="be91b-138">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="be91b-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

