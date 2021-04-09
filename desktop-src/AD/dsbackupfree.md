---
title: 'DsBackupFree 函式 (Ntdsbcli) '
description: 釋放 Active Directory Domain Services backup 和 restore 函數所配置的記憶體。
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- DsBackupFree 函式 Active Directory
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843448"
---
# <a name="dsbackupfree-function"></a><span data-ttu-id="a85db-104">DsBackupFree 函式</span><span class="sxs-lookup"><span data-stu-id="a85db-104">DsBackupFree function</span></span>

<span data-ttu-id="a85db-105">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a85db-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a85db-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a85db-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a85db-107">從 Windows Vista 開始，請改用 [磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="a85db-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="a85db-108">**DsBackupFree** 函式會釋放 Active Directory Domain Services backup 和 restore 函數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a85db-108">The **DsBackupFree** function releases memory allocated by the Active Directory Domain Services backup and restore functions.</span></span> <span data-ttu-id="a85db-109">下列函式會配置必須與 **DsBackupFree** 函式一起發行的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a85db-109">The following functions allocate memory that must be released with the **DsBackupFree** function.</span></span>

-   [<span data-ttu-id="a85db-110">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="a85db-110">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
-   [<span data-ttu-id="a85db-111">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="a85db-111">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
-   [<span data-ttu-id="a85db-112">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="a85db-112">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
-   [<span data-ttu-id="a85db-113">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="a85db-113">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a><span data-ttu-id="a85db-114">語法</span><span class="sxs-lookup"><span data-stu-id="a85db-114">Syntax</span></span>


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a85db-115">參數</span><span class="sxs-lookup"><span data-stu-id="a85db-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85db-116">*pvBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a85db-116">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a85db-117">要釋放之記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a85db-117">Pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85db-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a85db-118">Return value</span></span>

<span data-ttu-id="a85db-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a85db-119">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a85db-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a85db-120">Requirements</span></span>



| <span data-ttu-id="a85db-121">需求</span><span class="sxs-lookup"><span data-stu-id="a85db-121">Requirement</span></span> | <span data-ttu-id="a85db-122">值</span><span class="sxs-lookup"><span data-stu-id="a85db-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a85db-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a85db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a85db-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a85db-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a85db-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a85db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a85db-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a85db-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a85db-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a85db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a85db-128"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="a85db-128"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="a85db-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="a85db-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a85db-130"><dt>Ntdsbcli .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a85db-130"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="a85db-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a85db-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a85db-132"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a85db-132"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85db-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a85db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85db-134">**DsBackupGetBackupLogs**</span><span class="sxs-lookup"><span data-stu-id="a85db-134">**DsBackupGetBackupLogs**</span></span>](dsbackupgetbackuplogs.md)
</dt> <dt>

[<span data-ttu-id="a85db-135">**DsBackupGetDatabaseNames**</span><span class="sxs-lookup"><span data-stu-id="a85db-135">**DsBackupGetDatabaseNames**</span></span>](dsbackupgetdatabasenames.md)
</dt> <dt>

[<span data-ttu-id="a85db-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="a85db-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="a85db-137">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="a85db-137">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="a85db-138">備份 Active Directory 伺服器</span><span class="sxs-lookup"><span data-stu-id="a85db-138">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="a85db-139">目錄備份功能</span><span class="sxs-lookup"><span data-stu-id="a85db-139">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

