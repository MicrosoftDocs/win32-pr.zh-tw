---
title: 'MMIOM_RENAME 訊息 (Mmsystem .h) '
description: MmioRename 函 \_ 式會將 MMIOM 重新命名訊息傳送至 i/o 程式，以要求重新命名指定的檔案。
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466468"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="498a1-104">MMIOM \_ 重新命名訊息</span><span class="sxs-lookup"><span data-stu-id="498a1-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="498a1-105">[**MmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)函式會將 **MMIOM \_ 重新命名** 訊息傳送至 I/o 程式，以要求重新命名指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="498a1-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="498a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="498a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498a1-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span><span class="sxs-lookup"><span data-stu-id="498a1-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="498a1-108">字串的指標，其中包含要重新命名的檔案名。</span><span class="sxs-lookup"><span data-stu-id="498a1-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="498a1-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span><span class="sxs-lookup"><span data-stu-id="498a1-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="498a1-110">包含新檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="498a1-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498a1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="498a1-111">Return Value</span></span>

<span data-ttu-id="498a1-112">如果檔案已成功重新命名，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="498a1-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="498a1-113">如果找不到指定的檔案，則傳回值為 MMIOERR \_ FILENOTFOUND。</span><span class="sxs-lookup"><span data-stu-id="498a1-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="498a1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="498a1-114">Requirements</span></span>



| <span data-ttu-id="498a1-115">需求</span><span class="sxs-lookup"><span data-stu-id="498a1-115">Requirement</span></span> | <span data-ttu-id="498a1-116">值</span><span class="sxs-lookup"><span data-stu-id="498a1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498a1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="498a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="498a1-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="498a1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="498a1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="498a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="498a1-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="498a1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="498a1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="498a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="498a1-122"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="498a1-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

