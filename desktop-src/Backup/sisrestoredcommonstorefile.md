---
title: 'SisRestoredCommonStoreFile 函式 (Sisbkup) '
description: 報告已寫入一般存放區檔案的 SIS 架構。
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- SisRestoredCommonStoreFile 函式備份
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934104"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="7ac36-104">SisRestoredCommonStoreFile 函式</span><span class="sxs-lookup"><span data-stu-id="7ac36-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="7ac36-105">**SisRestoredCommonStoreFile** 函式會向已寫入一般存放區檔案的 SIS 架構報告。</span><span class="sxs-lookup"><span data-stu-id="7ac36-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac36-106">語法</span><span class="sxs-lookup"><span data-stu-id="7ac36-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="7ac36-107">參數</span><span class="sxs-lookup"><span data-stu-id="7ac36-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac36-108">*sisRestoreStructure* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ac36-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac36-109">從 [**SisCreateRestoreStructure**](siscreaterestorestructure.md)傳回的 SIS 還原結構指標。</span><span class="sxs-lookup"><span data-stu-id="7ac36-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ac36-110">*commonStoreFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ac36-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ac36-111">已還原之一般存放區檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac36-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac36-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ac36-112">Return value</span></span>

<span data-ttu-id="7ac36-113">如果成功完成，則此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7ac36-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="7ac36-114">呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得呼叫失敗原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7ac36-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac36-115">備註</span><span class="sxs-lookup"><span data-stu-id="7ac36-115">Remarks</span></span>

<span data-ttu-id="7ac36-116">當您還原一般存放區檔案之後，應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="7ac36-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="7ac36-117">它會通知 SIS 架構已撰寫新的一般存放區檔案，以便 SIS 架構可以執行內部維護工作，例如初始化其內部資料結構或修正一般存放區檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="7ac36-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="7ac36-118">您的還原作業應該只還原 [**SisRestoredLink**](sisrestoredlink.md)所報告的一般存放區檔案，即使備份媒體上有其他一般存放區檔案也一樣。</span><span class="sxs-lookup"><span data-stu-id="7ac36-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="7ac36-119">您的還原作業可以依所選的任何順序還原 SIS 連結和一般存放區檔案;不過，它必須在還原任何連結之後呼叫 **SisRestoredLink** ，而且它必須在還原任何一般存放區檔案之後呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="7ac36-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="7ac36-120">由於還原作業無法識別將會還原的一般存放區檔案，直到將檔案名回報給它，因為還原連結之後，您的還原作業將一律會還原一般存放區檔案，但至少有一個連結指向它會還原。</span><span class="sxs-lookup"><span data-stu-id="7ac36-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="7ac36-121">不過，您可以接著還原指向該一般存放區檔案的其他 SIS 連結。</span><span class="sxs-lookup"><span data-stu-id="7ac36-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac36-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ac36-122">Requirements</span></span>



| <span data-ttu-id="7ac36-123">需求</span><span class="sxs-lookup"><span data-stu-id="7ac36-123">Requirement</span></span> | <span data-ttu-id="7ac36-124">值</span><span class="sxs-lookup"><span data-stu-id="7ac36-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac36-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ac36-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac36-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ac36-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7ac36-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ac36-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac36-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ac36-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7ac36-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7ac36-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ac36-130"><dt>Sisbkup。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ac36-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ac36-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ac36-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ac36-132"><dt>Sisbkup .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ac36-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ac36-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac36-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ac36-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac36-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac36-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ac36-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac36-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="7ac36-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="7ac36-137">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="7ac36-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

