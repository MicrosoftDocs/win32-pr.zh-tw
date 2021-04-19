---
description: GetCaptureCommentFromFilename 函式會從 capture 檔案中解壓縮 capture 批註。
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: 'GetCaptureCommentFromFilename 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967087"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="1d6a9-103">GetCaptureCommentFromFilename 函式</span><span class="sxs-lookup"><span data-stu-id="1d6a9-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="1d6a9-104">**GetCaptureCommentFromFilename** 函式會從 [*capture*](c.md)檔案中解壓縮 capture 批註。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d6a9-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="1d6a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d6a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d6a9-107">*lpFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d6a9-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6a9-108">捕捉檔名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="1d6a9-109">*lpComment* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d6a9-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6a9-110">批註的預先配置字串指標。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="1d6a9-111">*BufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d6a9-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6a9-112">字串的大小。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d6a9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d6a9-113">Return value</span></span>

<span data-ttu-id="1d6a9-114">如果函式成功 (也就是，如果找到並複製了批註，或在 capture 檔) 中沒有批註，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1d6a9-115">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="1d6a9-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1d6a9-116">Return code</span></span>                                                                                                 | <span data-ttu-id="1d6a9-117">Description</span><span class="sxs-lookup"><span data-stu-id="1d6a9-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d6a9-118"><dt>**NMERR \_ 檔案 \_ 讀取 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="1d6a9-119">無法讀取 capture 批註。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="1d6a9-120"><dt>**NMERR \_ 不正確 \_ 檔 \_ 格式**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="1d6a9-121">批註框架不是有效的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="1d6a9-122"><dt>**\_ \_ \_ 找不到 NMERR 檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="1d6a9-123">找不到 *lpFilename* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="1d6a9-124"><dt>**NMERR \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="1d6a9-125">其中一個參數指定不正確。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1d6a9-126">備註</span><span class="sxs-lookup"><span data-stu-id="1d6a9-126">Remarks</span></span>

<span data-ttu-id="1d6a9-127">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureCommentFromFilename** 函數。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="1d6a9-128">若要取得即時捕捉的批註，請呼叫 [GetCaptureComment](getcapturecomment.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="1d6a9-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6a9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d6a9-129">Requirements</span></span>



| <span data-ttu-id="1d6a9-130">需求</span><span class="sxs-lookup"><span data-stu-id="1d6a9-130">Requirement</span></span> | <span data-ttu-id="1d6a9-131">值</span><span class="sxs-lookup"><span data-stu-id="1d6a9-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6a9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d6a9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1d6a9-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d6a9-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1d6a9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d6a9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1d6a9-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d6a9-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d6a9-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1d6a9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d6a9-137"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1d6a9-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d6a9-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d6a9-139"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1d6a9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1d6a9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d6a9-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d6a9-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6a9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d6a9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6a9-143">GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="1d6a9-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




