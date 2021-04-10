---
title: 'MMIOM_WRITE 訊息 (Mmsystem .h) '
description: MmioWrite 函 \_ 式會將 MMIOM 寫入訊息傳送至 i/o 程式，以要求將資料寫入至開啟的檔案。
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934993"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="6d3b5-104">MMIOM \_ 寫入訊息</span><span class="sxs-lookup"><span data-stu-id="6d3b5-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="6d3b5-105">[**MmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)函式會將 **MMIOM \_ 寫入** 訊息傳送至 i/o 程式，以要求將資料寫入至開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="6d3b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d3b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3b5-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="6d3b5-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6d3b5-108">緩衝區的指標，其中包含要寫入檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="6d3b5-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="6d3b5-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="6d3b5-110">要寫入檔案的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3b5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d3b5-111">Return Value</span></span>

<span data-ttu-id="6d3b5-112">傳回實際寫入檔案的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="6d3b5-113">如果發生錯誤，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3b5-114">備註</span><span class="sxs-lookup"><span data-stu-id="6d3b5-114">Remarks</span></span>

<span data-ttu-id="6d3b5-115">I/o 程式負責更新 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員，以反映寫入作業之後的新檔案位置。</span><span class="sxs-lookup"><span data-stu-id="6d3b5-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3b5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d3b5-116">Requirements</span></span>



| <span data-ttu-id="6d3b5-117">需求</span><span class="sxs-lookup"><span data-stu-id="6d3b5-117">Requirement</span></span> | <span data-ttu-id="6d3b5-118">值</span><span class="sxs-lookup"><span data-stu-id="6d3b5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3b5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d3b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d3b5-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3b5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6d3b5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d3b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d3b5-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d3b5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d3b5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6d3b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d3b5-124"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6d3b5-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

