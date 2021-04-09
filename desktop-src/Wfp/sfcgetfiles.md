---
description: 列出受保護的檔案。
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: 'SfcGetFiles 函式 (Sfcfiles) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849860"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="af530-103">SfcGetFiles 函式</span><span class="sxs-lookup"><span data-stu-id="af530-103">SfcGetFiles function</span></span>

<span data-ttu-id="af530-104">\[此函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="af530-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af530-105">這項功能的支援已在 Windows Vista 和 Windows Server 2008 中移除。</span><span class="sxs-lookup"><span data-stu-id="af530-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="af530-106">請改用 [WRP](wfp-functions.md) 函式中所列的支援函數。\]</span><span class="sxs-lookup"><span data-stu-id="af530-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="af530-107">列出受保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="af530-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="af530-108">語法</span><span class="sxs-lookup"><span data-stu-id="af530-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="af530-109">參數</span><span class="sxs-lookup"><span data-stu-id="af530-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af530-110">*ProtFileData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af530-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af530-111">[**PPROTECT 檔案 \_ \_ 專案**](pprotect-file-entry.md)結構的指標，其中包含受保護的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="af530-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="af530-112">*FileCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af530-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af530-113">包含受保護檔案數目之 ULONG 值的位置指標。</span><span class="sxs-lookup"><span data-stu-id="af530-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af530-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="af530-114">Return value</span></span>

<span data-ttu-id="af530-115">如果函式成功，則傳回值為「狀態 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="af530-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="af530-116">如果函式失敗，則會傳回適當的 NTSTATUS 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="af530-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af530-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="af530-117">Requirements</span></span>



| <span data-ttu-id="af530-118">需求</span><span class="sxs-lookup"><span data-stu-id="af530-118">Requirement</span></span> | <span data-ttu-id="af530-119">值</span><span class="sxs-lookup"><span data-stu-id="af530-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af530-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af530-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af530-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af530-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af530-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af530-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af530-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af530-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af530-124">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="af530-124">End of client support</span></span><br/>    | <span data-ttu-id="af530-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af530-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af530-126">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="af530-126">End of server support</span></span><br/>    | <span data-ttu-id="af530-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af530-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af530-128">標頭</span><span class="sxs-lookup"><span data-stu-id="af530-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af530-129"><dt>Sfcfiles。h</dt></span><span class="sxs-lookup"><span data-stu-id="af530-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="af530-130">DLL</span><span class="sxs-lookup"><span data-stu-id="af530-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af530-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af530-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af530-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af530-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af530-133">**PPROTECT \_ 檔案 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="af530-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




