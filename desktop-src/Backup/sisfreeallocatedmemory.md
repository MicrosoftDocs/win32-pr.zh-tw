---
title: 'SisFreeAllocatedMemory 函式 (Sisbkup) '
description: 釋出 SIS API 函數所配置的記憶體。
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- SisFreeAllocatedMemory 函式備份
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843304"
---
# <a name="sisfreeallocatedmemory-function"></a><span data-ttu-id="cfc0c-104">SisFreeAllocatedMemory 函式</span><span class="sxs-lookup"><span data-stu-id="cfc0c-104">SisFreeAllocatedMemory function</span></span>

<span data-ttu-id="cfc0c-105">**SisFreeAllocatedMemory** 函式會釋出 SIS API 函式所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-105">The **SisFreeAllocatedMemory** function frees memory allocated by SIS API functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc0c-106">語法</span><span class="sxs-lookup"><span data-stu-id="cfc0c-106">Syntax</span></span>


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a><span data-ttu-id="cfc0c-107">參數</span><span class="sxs-lookup"><span data-stu-id="cfc0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc0c-108">*allocatedSpace* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cfc0c-108">*allocatedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc0c-109">SIS API 所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-109">Pointer to the memory allocated by the SIS API.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc0c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfc0c-110">Return value</span></span>

<span data-ttu-id="cfc0c-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc0c-112">備註</span><span class="sxs-lookup"><span data-stu-id="cfc0c-112">Remarks</span></span>

<span data-ttu-id="cfc0c-113">呼叫此函式完成之後，呼叫端就無法再存取釋放的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-113">After the call to this function completes, the caller may no longer access the freed memory.</span></span>

<span data-ttu-id="cfc0c-114">此呼叫應該用來解除配置針對 [**SisCreateBackupStructure**](siscreatebackupstructure.md)和 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)所傳回之 *commonStoreRootPathname* 參數字串所配置的記憶體，以及包含從 **SisCreateBackupStructure**、 [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)、 **SisCreateRestoreStructure** 和 [**SisRestoredLink**](sisrestoredlink.md)傳回之一般存放區檔案名的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-114">This call should be used to deallocate the memory allocated for the *commonStoreRootPathname* parameter strings returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md) and [**SisCreateRestoreStructure**](siscreaterestorestructure.md), and the array of strings containing common-store file names returned from **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure**, and [**SisRestoredLink**](sisrestoredlink.md).</span></span> <span data-ttu-id="cfc0c-115">在後者的情況下，也必須藉由呼叫 **SisFreeAllocatedMemory** 來釋放陣列本身。</span><span class="sxs-lookup"><span data-stu-id="cfc0c-115">In the latter case, the array itself also must be freed by calling **SisFreeAllocatedMemory**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc0c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfc0c-116">Requirements</span></span>



| <span data-ttu-id="cfc0c-117">需求</span><span class="sxs-lookup"><span data-stu-id="cfc0c-117">Requirement</span></span> | <span data-ttu-id="cfc0c-118">值</span><span class="sxs-lookup"><span data-stu-id="cfc0c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc0c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfc0c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc0c-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfc0c-120">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cfc0c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfc0c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc0c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfc0c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cfc0c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cfc0c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc0c-124"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc0c-124"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfc0c-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="cfc0c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="cfc0c-126"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfc0c-126"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="cfc0c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc0c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc0c-128"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc0c-128"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc0c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfc0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc0c-130">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="cfc0c-130">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="cfc0c-131">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="cfc0c-131">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="cfc0c-132">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="cfc0c-132">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="cfc0c-133">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="cfc0c-133">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

 





