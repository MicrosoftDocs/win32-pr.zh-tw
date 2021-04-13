---
title: 'SisFreeRestoreStructure 函式 (Sisbkup) '
description: 釋出配置給指定之 SIS 還原結構的記憶體，並執行工作來準備 SIS 篩選器，以正確地設定在還原作業期間建立的連結。
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- SisFreeRestoreStructure 函式備份
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466649"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="42044-104">SisFreeRestoreStructure 函式</span><span class="sxs-lookup"><span data-stu-id="42044-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="42044-105">**SisFreeRestoreStructure** 函式會釋出配置給指定之 SIS 還原結構的記憶體，並執行工作來準備 SIS 篩選器，以正確地設定在還原作業期間所建立的連結。</span><span class="sxs-lookup"><span data-stu-id="42044-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="42044-106">語法</span><span class="sxs-lookup"><span data-stu-id="42044-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="42044-107">參數</span><span class="sxs-lookup"><span data-stu-id="42044-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42044-108">*sisRestoreStructure* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42044-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42044-109">從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。</span><span class="sxs-lookup"><span data-stu-id="42044-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42044-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="42044-110">Return value</span></span>

<span data-ttu-id="42044-111">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="42044-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="42044-112">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="42044-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="42044-113">備註</span><span class="sxs-lookup"><span data-stu-id="42044-113">Remarks</span></span>

<span data-ttu-id="42044-114">在呼叫此函式完成之前存取 SIS 連結，可能會導致磁片區檢查或部分的連結內容讀取。</span><span class="sxs-lookup"><span data-stu-id="42044-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="42044-115">請注意，這並不安全地假設它只會解除配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="42044-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="42044-116">例如，此函式也可以針對 SIS 架構執行額外的系統管理作業。</span><span class="sxs-lookup"><span data-stu-id="42044-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="42044-117">因此，即使您的還原作業之後會立即結束，也請呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="42044-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="42044-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="42044-118">Requirements</span></span>



| <span data-ttu-id="42044-119">需求</span><span class="sxs-lookup"><span data-stu-id="42044-119">Requirement</span></span> | <span data-ttu-id="42044-120">值</span><span class="sxs-lookup"><span data-stu-id="42044-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42044-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42044-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42044-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42044-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="42044-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42044-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42044-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42044-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="42044-125">標頭</span><span class="sxs-lookup"><span data-stu-id="42044-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="42044-126"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="42044-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="42044-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="42044-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="42044-128"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42044-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="42044-129">DLL</span><span class="sxs-lookup"><span data-stu-id="42044-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42044-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42044-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42044-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42044-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42044-132">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="42044-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

