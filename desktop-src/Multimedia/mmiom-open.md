---
title: 'MMIOM_OPEN 訊息 (Mmsystem .h) '
description: MMIOM \_ 開啟的訊息會由 mmioOpen 函數傳送至 i/o 程式，以要求開啟或刪除檔案。
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972702"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="cb199-104">MMIOM \_ 開啟的訊息</span><span class="sxs-lookup"><span data-stu-id="cb199-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="cb199-105">**MMIOM \_ 開啟** 的訊息會由 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數傳送至 i/o 程式，以要求開啟或刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="cb199-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="cb199-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb199-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb199-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span><span class="sxs-lookup"><span data-stu-id="cb199-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="cb199-108">以 Null 終止的字串，其中包含要開啟的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cb199-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="cb199-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="cb199-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="cb199-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="cb199-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb199-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb199-111">Return Value</span></span>

<span data-ttu-id="cb199-112">如果成功，則會傳回 MMSYSERR \_ >aad-userreadusingalternativesecurityid-noerror，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb199-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="cb199-113">可能的錯誤值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="cb199-113">Possible error values include the following:</span></span>



| <span data-ttu-id="cb199-114">需求</span><span class="sxs-lookup"><span data-stu-id="cb199-114">Requirement</span></span> | <span data-ttu-id="cb199-115">值</span><span class="sxs-lookup"><span data-stu-id="cb199-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="cb199-116">MMIOM \_ CANNOTOPEN</span><span class="sxs-lookup"><span data-stu-id="cb199-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="cb199-117">無法開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="cb199-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="cb199-118">MMIOM \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="cb199-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="cb199-119">記憶體不足，無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="cb199-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cb199-120">備註</span><span class="sxs-lookup"><span data-stu-id="cb199-120">Remarks</span></span>

<span data-ttu-id="cb199-121">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **dwFlags** 成員包含傳遞至 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的旗標。</span><span class="sxs-lookup"><span data-stu-id="cb199-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="cb199-122">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))結構的 **lDiskOffset** 成員會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="cb199-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="cb199-123">如果這個值不正確，i/o 程式必須更正它。</span><span class="sxs-lookup"><span data-stu-id="cb199-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="cb199-124">如果應用程式將 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構傳遞給 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)，則傳回值會在 **wErrorRet** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="cb199-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb199-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb199-125">Requirements</span></span>



| <span data-ttu-id="cb199-126">需求</span><span class="sxs-lookup"><span data-stu-id="cb199-126">Requirement</span></span> | <span data-ttu-id="cb199-127">值</span><span class="sxs-lookup"><span data-stu-id="cb199-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb199-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb199-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb199-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb199-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb199-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb199-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb199-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb199-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb199-132">標頭</span><span class="sxs-lookup"><span data-stu-id="cb199-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb199-133"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cb199-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

