---
title: 'MMIOM_SEEK 訊息 (Mmsystem .h) '
description: '\_MmioSeek 函數會將 MMIOM 搜尋訊息傳送至 i/o 程式，以要求移動目前的檔案位置。'
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967761"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="56027-104">MMIOM \_ 搜尋訊息</span><span class="sxs-lookup"><span data-stu-id="56027-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="56027-105">[**MmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)函數會將 **MMIOM \_ 搜尋** 訊息傳送至 i/o 程式，以要求移動目前的檔案位置。</span><span class="sxs-lookup"><span data-stu-id="56027-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="56027-106">參數</span><span class="sxs-lookup"><span data-stu-id="56027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56027-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span><span class="sxs-lookup"><span data-stu-id="56027-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="56027-108">新檔案位置。</span><span class="sxs-lookup"><span data-stu-id="56027-108">New file position.</span></span> <span data-ttu-id="56027-109">此值的意義取決於在 **lChangeFlag** 中指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="56027-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="56027-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span><span class="sxs-lookup"><span data-stu-id="56027-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="56027-111">指定檔案位置變更方式的旗標。</span><span class="sxs-lookup"><span data-stu-id="56027-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="56027-112">系統會定義下列值：</span><span class="sxs-lookup"><span data-stu-id="56027-112">The following values are defined:</span></span>



| <span data-ttu-id="56027-113">需求</span><span class="sxs-lookup"><span data-stu-id="56027-113">Requirement</span></span> | <span data-ttu-id="56027-114">值</span><span class="sxs-lookup"><span data-stu-id="56027-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56027-115">搜尋到 \_ 當前</span><span class="sxs-lookup"><span data-stu-id="56027-115">SEEK\_CUR</span></span> | <span data-ttu-id="56027-116">將檔案位置從目前的位置移至 *lNewFilePos* 的位元組。</span><span class="sxs-lookup"><span data-stu-id="56027-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="56027-117">*lNewFilePos* 可以是正數或負數。</span><span class="sxs-lookup"><span data-stu-id="56027-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="56027-118">搜尋 \_ 結束</span><span class="sxs-lookup"><span data-stu-id="56027-118">SEEK\_END</span></span> | <span data-ttu-id="56027-119">將檔案位置從檔案結尾移到 *lNewFilePos* 的位元組。</span><span class="sxs-lookup"><span data-stu-id="56027-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="56027-120">搜尋 \_ 集</span><span class="sxs-lookup"><span data-stu-id="56027-120">SEEK\_SET</span></span> | <span data-ttu-id="56027-121">將檔案位置從檔案的開頭移動到 *lNewFilePos* 的位元組。</span><span class="sxs-lookup"><span data-stu-id="56027-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56027-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="56027-122">Return Value</span></span>

<span data-ttu-id="56027-123">傳回新的檔案位置。</span><span class="sxs-lookup"><span data-stu-id="56027-123">Returns the new file position.</span></span> <span data-ttu-id="56027-124">如果發生錯誤，則傳回值為1。</span><span class="sxs-lookup"><span data-stu-id="56027-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="56027-125">備註</span><span class="sxs-lookup"><span data-stu-id="56027-125">Remarks</span></span>

<span data-ttu-id="56027-126">I/o 程式負責維護 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構之 **lDiskOffset** 成員中的目前檔案位置。</span><span class="sxs-lookup"><span data-stu-id="56027-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="56027-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="56027-127">Requirements</span></span>



| <span data-ttu-id="56027-128">需求</span><span class="sxs-lookup"><span data-stu-id="56027-128">Requirement</span></span> | <span data-ttu-id="56027-129">值</span><span class="sxs-lookup"><span data-stu-id="56027-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56027-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56027-130">Minimum supported client</span></span><br/> | <span data-ttu-id="56027-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56027-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56027-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56027-132">Minimum supported server</span></span><br/> | <span data-ttu-id="56027-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56027-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56027-134">標頭</span><span class="sxs-lookup"><span data-stu-id="56027-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="56027-135"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="56027-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

