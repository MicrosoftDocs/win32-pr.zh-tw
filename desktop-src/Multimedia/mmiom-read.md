---
title: 'MMIOM_READ 訊息 (Mmsystem .h) '
description: MmioRead 函 \_ 式會將 MMIOM 讀取訊息傳送至 i/o 程式，以要求從開啟的檔案讀取指定的位元組數目。
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467080"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="e29c0-104">MMIOM \_ 讀取訊息</span><span class="sxs-lookup"><span data-stu-id="e29c0-104">MMIOM\_READ message</span></span>

<span data-ttu-id="e29c0-105">[**MmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)函式會將 **MMIOM \_ 讀取** 訊息傳送至 i/o 程式，以要求從開啟的檔案讀取指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e29c0-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="e29c0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e29c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e29c0-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span><span class="sxs-lookup"><span data-stu-id="e29c0-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="e29c0-108">要填入從檔案讀取之資料的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="e29c0-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="e29c0-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span><span class="sxs-lookup"><span data-stu-id="e29c0-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="e29c0-110">要從檔案讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e29c0-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e29c0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e29c0-111">Return Value</span></span>

<span data-ttu-id="e29c0-112">傳回實際從檔案讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="e29c0-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="e29c0-113">如果沒有更多的位元組可以讀取，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="e29c0-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="e29c0-114">如果發生錯誤，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="e29c0-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e29c0-115">備註</span><span class="sxs-lookup"><span data-stu-id="e29c0-115">Remarks</span></span>

<span data-ttu-id="e29c0-116">I/o 程式負責更新 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員，以反映讀取作業之後的新檔案位置。</span><span class="sxs-lookup"><span data-stu-id="e29c0-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e29c0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e29c0-117">Requirements</span></span>



| <span data-ttu-id="e29c0-118">需求</span><span class="sxs-lookup"><span data-stu-id="e29c0-118">Requirement</span></span> | <span data-ttu-id="e29c0-119">值</span><span class="sxs-lookup"><span data-stu-id="e29c0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e29c0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e29c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e29c0-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e29c0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e29c0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e29c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e29c0-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e29c0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e29c0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e29c0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e29c0-125"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e29c0-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

