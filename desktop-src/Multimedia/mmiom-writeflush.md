---
title: 'MMIOM_WRITEFLUSH 訊息 (Mmsystem .h) '
description: MmioWrite 函 \_ 式會將 MMIOM WRITEFLUSH 訊息傳送至 i/o 程式，要求將該資料寫入至開啟的檔案，而且 i/o 程式所使用的任何內部緩衝區都會排清至磁片。
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686372"
---
# <a name="mmiom_writeflush-message"></a><span data-ttu-id="515c0-104">MMIOM \_ WRITEFLUSH 訊息</span><span class="sxs-lookup"><span data-stu-id="515c0-104">MMIOM\_WRITEFLUSH message</span></span>

<span data-ttu-id="515c0-105">[**MmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)函式會將 **MMIOM \_ WRITEFLUSH** 訊息傳送至 i/o 程式，要求將該資料寫入至開啟的檔案，而且 i/o 程式所使用的任何內部緩衝區都會排清至磁片。</span><span class="sxs-lookup"><span data-stu-id="515c0-105">The **MMIOM\_WRITEFLUSH** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file and that any internal buffers used by the I/O procedure be flushed to disk.</span></span>


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="515c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="515c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="515c0-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="515c0-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="515c0-108">緩衝區的指標，其中包含要寫入檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="515c0-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="515c0-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="515c0-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="515c0-110">要寫入檔案的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="515c0-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="515c0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="515c0-111">Return Value</span></span>

<span data-ttu-id="515c0-112">傳回實際寫入檔案的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="515c0-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="515c0-113">如果發生錯誤，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="515c0-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="515c0-114">備註</span><span class="sxs-lookup"><span data-stu-id="515c0-114">Remarks</span></span>

<span data-ttu-id="515c0-115">I/o 程式負責更新 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員，以反映寫入作業之後的新檔案位置。</span><span class="sxs-lookup"><span data-stu-id="515c0-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

<span data-ttu-id="515c0-116">這則訊息相當於 [**MMIOM \_ 寫入**](mmiom-write.md) 訊息，不同之處在于它會要求 i/o 程式排清其內部緩衝區（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="515c0-116">This message is equivalent to the [**MMIOM\_WRITE**](mmiom-write.md) message except that it requests that the I/O procedure flush its internal buffers, if any.</span></span> <span data-ttu-id="515c0-117">除非 i/o 程式執行內部緩衝處理，否則此訊息可以像 **MMIOM \_ 寫入** 訊息一樣處理。</span><span class="sxs-lookup"><span data-stu-id="515c0-117">Unless an I/O procedure performs internal buffering, this message can be handled exactly like the **MMIOM\_WRITE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="515c0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="515c0-118">Requirements</span></span>



| <span data-ttu-id="515c0-119">需求</span><span class="sxs-lookup"><span data-stu-id="515c0-119">Requirement</span></span> | <span data-ttu-id="515c0-120">值</span><span class="sxs-lookup"><span data-stu-id="515c0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="515c0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="515c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="515c0-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="515c0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="515c0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="515c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="515c0-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="515c0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="515c0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="515c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="515c0-126"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="515c0-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

