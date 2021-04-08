---
title: 'SisFreeBackupStructure 函式 (Sisbkup) '
description: 釋出指定的 SIS 備份結構。
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- SisFreeBackupStructure 函式備份
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685706"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="7f0ff-104">SisFreeBackupStructure 函式</span><span class="sxs-lookup"><span data-stu-id="7f0ff-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="7f0ff-105">**SisFreeBackupStructure** 函式會釋出指定的 SIS 備份結構。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="7f0ff-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="7f0ff-107">參數</span><span class="sxs-lookup"><span data-stu-id="7f0ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f0ff-108">*sisBackupStructure* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f0ff-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f0ff-109">從 [**SisCreateBackupStructure**](siscreatebackupstructure.md)傳回之 SIS 備份結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f0ff-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f0ff-110">Return value</span></span>

<span data-ttu-id="7f0ff-111">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="7f0ff-112">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f0ff-113">備註</span><span class="sxs-lookup"><span data-stu-id="7f0ff-113">Remarks</span></span>

<span data-ttu-id="7f0ff-114">當完成 *sisBackupStructure* 參數值所識別之磁片區的備份作業之後，應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="7f0ff-115">請注意，這並不安全地假設它只會解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="7f0ff-116">例如，此函式也可以針對 SIS 架構執行額外的系統管理作業。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="7f0ff-117">因此，即使您的備份作業在之後立即結束，也請呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="7f0ff-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0ff-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f0ff-118">Requirements</span></span>



| <span data-ttu-id="7f0ff-119">需求</span><span class="sxs-lookup"><span data-stu-id="7f0ff-119">Requirement</span></span> | <span data-ttu-id="7f0ff-120">值</span><span class="sxs-lookup"><span data-stu-id="7f0ff-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0ff-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f0ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f0ff-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f0ff-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7f0ff-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f0ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f0ff-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f0ff-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7f0ff-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7f0ff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f0ff-126"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f0ff-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f0ff-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f0ff-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f0ff-128"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f0ff-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="7f0ff-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7f0ff-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f0ff-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f0ff-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f0ff-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f0ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f0ff-132">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="7f0ff-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

