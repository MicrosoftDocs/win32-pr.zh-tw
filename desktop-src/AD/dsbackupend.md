---
title: 'DsBackupEnd 函式 (Ntdsbcli) '
description: 呼叫以終止備份作業。
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- DsBackupEnd 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843451"
---
# <a name="dsbackupend-function"></a><span data-ttu-id="0c4bb-104">DsBackupEnd 函式</span><span class="sxs-lookup"><span data-stu-id="0c4bb-104">DsBackupEnd function</span></span>

<span data-ttu-id="0c4bb-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c4bb-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="0c4bb-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="0c4bb-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="0c4bb-108">呼叫 **DsBackupEnd** 函式以終止備份作業。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-108">The **DsBackupEnd** function is called to terminate a backup operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c4bb-109">語法</span><span class="sxs-lookup"><span data-stu-id="0c4bb-109">Syntax</span></span>


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="0c4bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="0c4bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4bb-111">*hbc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c4bb-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c4bb-112">包含使用 [**DsBackupPrepare**](dsbackupprepare.md) 函數取得的備份內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4bb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c4bb-113">Return value</span></span>

<span data-ttu-id="0c4bb-114">如果函式成功，則傳回 **S \_ OK** ，否則傳回 Win32 或 RPC 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-114">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="0c4bb-115">下列清單列出其他可能的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-115">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="0c4bb-116">**錯誤 \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="0c4bb-116">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="0c4bb-117">*hbc* 無效。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-117">*hbc* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c4bb-118">備註</span><span class="sxs-lookup"><span data-stu-id="0c4bb-118">Remarks</span></span>

<span data-ttu-id="0c4bb-119">**DsBackupEnd** 函式會關閉未完成的系結控制碼，並在成功或失敗的備份嘗試之後執行清除。</span><span class="sxs-lookup"><span data-stu-id="0c4bb-119">The **DsBackupEnd** function closes outstanding binding handles and performs a cleanup after a successful or unsuccessful backup attempt.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4bb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c4bb-120">Requirements</span></span>



| <span data-ttu-id="0c4bb-121">需求</span><span class="sxs-lookup"><span data-stu-id="0c4bb-121">Requirement</span></span> | <span data-ttu-id="0c4bb-122">值</span><span class="sxs-lookup"><span data-stu-id="0c4bb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4bb-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c4bb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4bb-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c4bb-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c4bb-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c4bb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4bb-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c4bb-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c4bb-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0c4bb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c4bb-128"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c4bb-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c4bb-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="0c4bb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c4bb-130"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c4bb-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c4bb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0c4bb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c4bb-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c4bb-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4bb-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c4bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4bb-134">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="0c4bb-134">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="0c4bb-135">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="0c4bb-135">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="0c4bb-136">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="0c4bb-136">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

